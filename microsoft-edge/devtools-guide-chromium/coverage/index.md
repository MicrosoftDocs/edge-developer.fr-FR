---
title: Rechercher du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601718"
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





# <span data-ttu-id="3f96c-103">Rechercher du code JavaScript et CSS inutilisé avec l’onglet couverture dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3f96c-103">Find Unused JavaScript And CSS Code With The Coverage Tab In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="3f96c-104">L’onglet couverture dans Microsoft Edge DevTools vous permet de rechercher du code JavaScript et CSS inutilisé.</span><span class="sxs-lookup"><span data-stu-id="3f96c-104">The Coverage tab in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="3f96c-105">La suppression du code inutilisé risque d’accélérer le chargement de la page et d’enregistrer les données cellulaires de vos utilisateurs mobiles.</span><span class="sxs-lookup"><span data-stu-id="3f96c-105">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

> ##### <span data-ttu-id="3f96c-106">Figure1</span><span class="sxs-lookup"><span data-stu-id="3f96c-106">Figure 1</span></span>  
> <span data-ttu-id="3f96c-107">Analyser la couverture du code</span><span class="sxs-lookup"><span data-stu-id="3f96c-107">Analyzing code coverage</span></span>  
> ![Analyser la couverture du code][ImageExample]  

> [!WARNING]
> <span data-ttu-id="3f96c-109">La recherche de code inutilisé est relativement simple.</span><span class="sxs-lookup"><span data-stu-id="3f96c-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="3f96c-110">Toutefois, la refactorisation d’un code base de telle sorte que chaque page expédie uniquement les scripts JavaScript et CSS dont il a besoin risque d’être difficile.</span><span class="sxs-lookup"><span data-stu-id="3f96c-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="3f96c-111">Ce guide ne traite pas de la refactorisation d’un code base pour éviter le code inutilisé, car ces derniers dépendent fortement de votre pile de technologie.</span><span class="sxs-lookup"><span data-stu-id="3f96c-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <span data-ttu-id="3f96c-112">Présentation</span><span class="sxs-lookup"><span data-stu-id="3f96c-112">Overview</span></span>   

<span data-ttu-id="3f96c-113">L’expédition de code JavaScript ou CSS inutilisé est un problème courant du développement Web.</span><span class="sxs-lookup"><span data-stu-id="3f96c-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="3f96c-114">Par exemple, supposons que vous vouliez utiliser le [composant de bouton amorce][BootstrapButtons] sur votre page.</span><span class="sxs-lookup"><span data-stu-id="3f96c-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="3f96c-115">Pour utiliser le composant Button, vous devez ajouter un lien vers la feuille de style bootstrap dans votre code HTML, comme suit:</span><span class="sxs-lookup"><span data-stu-id="3f96c-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="3f96c-116">Cette feuille de style n’inclut pas uniquement le code du composant Button.</span><span class="sxs-lookup"><span data-stu-id="3f96c-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="3f96c-117">Il contient la feuille de style en cascade (CSS) pour **tous** les composants d’amorce.</span><span class="sxs-lookup"><span data-stu-id="3f96c-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="3f96c-118">Mais vous n’utilisez pas les autres composants d’amorce.</span><span class="sxs-lookup"><span data-stu-id="3f96c-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="3f96c-119">C’est pourquoi votre page télécharge un ensemble de feuilles CSS dont il n’a pas besoin.</span><span class="sxs-lookup"><span data-stu-id="3f96c-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="3f96c-120">Ce code CSS supplémentaire est un problème pour les raisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f96c-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="3f96c-121">Le code supplémentaire ralentira le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="3f96c-121">The extra code slows down your page load.</span></span>  <!--See [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="3f96c-122">Si un utilisateur accède à la page sur un appareil mobile, le code supplémentaire utilise ses données cellulaires.</span><span class="sxs-lookup"><span data-stu-id="3f96c-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <span data-ttu-id="3f96c-123">Ouvrir l’onglet couverture</span><span class="sxs-lookup"><span data-stu-id="3f96c-123">Open the Coverage tab</span></span>   

1.  <span data-ttu-id="3f96c-124">[Ouvrir le menu de commandes][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="3f96c-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="3f96c-125">Commencez `coverage` à taper, sélectionnez la commande **afficher la couverture** , puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="3f96c-125">Start typing `coverage`, select the **Show Coverage** command, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="3f96c-126">L’onglet **couverture** s’ouvre dans le **tiroir**.</span><span class="sxs-lookup"><span data-stu-id="3f96c-126">The **Coverage** tab opens in the **Drawer**.</span></span>  

    > ##### <span data-ttu-id="3f96c-127">Figure 2</span><span class="sxs-lookup"><span data-stu-id="3f96c-127">Figure 2</span></span>  
    > <span data-ttu-id="3f96c-128">Onglet **couverture**</span><span class="sxs-lookup"><span data-stu-id="3f96c-128">The **Coverage** tab</span></span>  
    > ![Onglet couverture][ImageCoverage]  

## <span data-ttu-id="3f96c-130">Enregistrer la couverture du code</span><span class="sxs-lookup"><span data-stu-id="3f96c-130">Record code coverage</span></span>   

1.  <span data-ttu-id="3f96c-131">Cliquez sur l’un des boutons suivants sous l’onglet **couverture** .</span><span class="sxs-lookup"><span data-stu-id="3f96c-131">Click one of the following buttons in the **Coverage** tab:</span></span>  
    *   <span data-ttu-id="3f96c-132">Cliquez sur **Démarrer la couverture d’instrumentation et rechargez** ![ la couverture d’instrumentation de page et rechargez ][ImageReloadIcon] la page si vous voulez voir le code nécessaire au chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="3f96c-132">Click **Start Instrumenting Coverage And Reload Page** ![Start Instrumenting Coverage And Reload Page][ImageReloadIcon] if you want to see what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="3f96c-133">Cliquez **sur couverture instrumentation** ![ instrumentation ][ImageRecordIcon] si vous voulez voir le code utilisé après l’interaction avec la page.</span><span class="sxs-lookup"><span data-stu-id="3f96c-133">Click **Instrument Coverage** ![Instrument Coverage][ImageRecordIcon] if you want to see what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="3f96c-134">Cliquez sur **arrêter l’instrumentation et afficher les résultats** ![ arrêter la couverture de l’instrumentation et afficher les résultats ][ImageStopIcon] lorsque vous voulez arrêter l’enregistrement de la couverture du code.</span><span class="sxs-lookup"><span data-stu-id="3f96c-134">Click **Stop Instrumenting Coverage And Show Results** ![Stop Instrumenting Coverage And Show Results][ImageStopIcon] when you want to stop recording code coverage.</span></span>  

## <span data-ttu-id="3f96c-135">Analyser la couverture du code</span><span class="sxs-lookup"><span data-stu-id="3f96c-135">Analyze code coverage</span></span>   

<span data-ttu-id="3f96c-136">La table dans l’onglet **couverture** vous indique les ressources qui ont été analysées et le code utilisé dans chaque ressource.</span><span class="sxs-lookup"><span data-stu-id="3f96c-136">The table in the **Coverage** tab shows you what resources were analyzed, and how much code is used within each resource.</span></span> <span data-ttu-id="3f96c-137">Cliquez sur une ligne pour ouvrir cette ressource dans le volet **sources** et observez une répartition ligne par ligne du code utilisé et du code inutilisé.</span><span class="sxs-lookup"><span data-stu-id="3f96c-137">Click a row to open that resource in the **Sources** panel and see a line-by-line breakdown of used code and unused code.</span></span>  

> ##### <span data-ttu-id="3f96c-138">Figure3</span><span class="sxs-lookup"><span data-stu-id="3f96c-138">Figure 3</span></span>  
> <span data-ttu-id="3f96c-139">Rapport de couverture du code</span><span class="sxs-lookup"><span data-stu-id="3f96c-139">A code coverage report</span></span>  
> ![Rapport de couverture du code][ImageExample]  

*   <span data-ttu-id="3f96c-141">La colonne **URL** correspond à l’URL de la ressource qui a été analysée.</span><span class="sxs-lookup"><span data-stu-id="3f96c-141">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="3f96c-142">La colonne **type** indique si la ressource contient des éléments CSS ou JavaScript, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="3f96c-142">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="3f96c-143">La colonne **Total octets** correspond à la taille totale de la ressource en octets.</span><span class="sxs-lookup"><span data-stu-id="3f96c-143">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="3f96c-144">La colonne **octets inutilisés** correspond au nombre d’octets qui n’ont pas été utilisés.</span><span class="sxs-lookup"><span data-stu-id="3f96c-144">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="3f96c-145">La dernière colonne sans nom est une visualisation des colonnes **nombre total d’octets** et **octets inutilisés** .</span><span class="sxs-lookup"><span data-stu-id="3f96c-145">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="3f96c-146">La section rouge de la barre est des octets inutilisés.</span><span class="sxs-lookup"><span data-stu-id="3f96c-146">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="3f96c-147">La section verte est utilisée en octets.</span><span class="sxs-lookup"><span data-stu-id="3f96c-147">The green section is used bytes.</span></span>  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Figure 1: analyse de la couverture du code"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Figure 2: onglet couverture"  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Figure 3: rapport de couverture du code"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Boutons-démarrage"  

> [!NOTE]
> <span data-ttu-id="3f96c-153">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f96c-153">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3f96c-154">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/coverage/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="3f96c-154">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="3f96c-156">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f96c-156">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  