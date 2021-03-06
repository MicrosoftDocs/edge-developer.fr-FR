---
description: Découvrez comment rechercher et analyser du code JavaScript et CSS inutilisé dans Microsoft Edge DevTools.
title: Rechercher du code JavaScript et CSS inutilisé avec le panneau Couverture dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398762"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a><span data-ttu-id="7e958-104">Rechercher du code JavaScript et CSS inutilisé avec le panneau Couverture dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7e958-104">Find unused JavaScript and CSS code with the Coverage panel in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7e958-105">Le **panneau** Couverture de Microsoft Edge DevTools vous permet de trouver du code JavaScript et CSS inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7e958-105">The **Coverage** panel in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="7e958-106">La suppression du code inutilisé peut accélérer le chargement de votre page et enregistrer les données cellulaires de vos utilisateurs mobiles.</span><span class="sxs-lookup"><span data-stu-id="7e958-106">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analyse de la couverture du code" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   <span data-ttu-id="7e958-108">Analyse de la couverture du code</span><span class="sxs-lookup"><span data-stu-id="7e958-108">Analyzing code coverage</span></span>  
:::image-end:::  

> [!WARNING]
> <span data-ttu-id="7e958-109">Il est relativement facile de trouver du code inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7e958-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="7e958-110">Toutefois, il peut être difficile de refactoriser une base de code pour que chaque page n’expédie que les fichiers JavaScript et CSS dont elle a besoin.</span><span class="sxs-lookup"><span data-stu-id="7e958-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="7e958-111">Ce guide ne couvre pas la refactoriser une base de code pour éviter le code inutilisé, car ces refactoriseurs dépendent fortement de votre pile technologique.</span><span class="sxs-lookup"><span data-stu-id="7e958-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <a name="overview"></a><span data-ttu-id="7e958-112">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="7e958-112">Overview</span></span>  

<span data-ttu-id="7e958-113">La livraison de fichiers JavaScript ou CSS inutilisés est un problème courant dans le développement web.</span><span class="sxs-lookup"><span data-stu-id="7e958-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="7e958-114">Par exemple, supposons que vous souhaitez utiliser le composant bouton [Bootstrap][BootstrapButtons] sur votre page.</span><span class="sxs-lookup"><span data-stu-id="7e958-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="7e958-115">Pour utiliser le composant de bouton, vous devez ajouter un lien vers la feuille de style Bootstrap dans votre code HTML, comme ceci :</span><span class="sxs-lookup"><span data-stu-id="7e958-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="7e958-116">Cette feuille de style n’inclut pas uniquement le code du composant de bouton.</span><span class="sxs-lookup"><span data-stu-id="7e958-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="7e958-117">Il contient le CSS pour **tous les** composants Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="7e958-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="7e958-118">Mais vous n’utilisez aucun des autres composants Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="7e958-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="7e958-119">Votre page télécharge donc une série de fichiers CSS dont elle n’a pas besoin.</span><span class="sxs-lookup"><span data-stu-id="7e958-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="7e958-120">Cette CSS supplémentaire est un problème pour les raisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e958-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="7e958-121">Le code supplémentaire ralentit le chargement de votre page.</span><span class="sxs-lookup"><span data-stu-id="7e958-121">The extra code slows down your page load.</span></span>  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="7e958-122">Si un utilisateur accède à la page sur un appareil mobile, le code supplémentaire utilise ses données cellulaires.</span><span class="sxs-lookup"><span data-stu-id="7e958-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a><span data-ttu-id="7e958-123">Ouvrir le panneau Couverture</span><span class="sxs-lookup"><span data-stu-id="7e958-123">Open the Coverage panel</span></span>  

1.  <span data-ttu-id="7e958-124">[Ouvrez le menu Commande.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="7e958-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="7e958-125">Commencez à `coverage` taper, sélectionnez **la commande Afficher la** couverture, puis `Enter` sélectionnez pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="7e958-125">Start typing `coverage`, select the **Show Coverage** command, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="7e958-126">Le **panneau** Couverture s’ouvre dans le **panneau .**</span><span class="sxs-lookup"><span data-stu-id="7e958-126">The **Coverage** panel opens in the **Drawer**.</span></span>  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Panneau Couverture" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       <span data-ttu-id="7e958-128">Panneau **Couverture**</span><span class="sxs-lookup"><span data-stu-id="7e958-128">The **Coverage** panel</span></span>  
    :::image-end:::  
    
## <a name="record-code-coverage"></a><span data-ttu-id="7e958-129">Couverture du code d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="7e958-129">Record code coverage</span></span>  

1.  <span data-ttu-id="7e958-130">Choisissez l’un des boutons suivants dans le **panneau Couverture.**</span><span class="sxs-lookup"><span data-stu-id="7e958-130">Choose one of the following buttons in the **Coverage** panel.</span></span>  
    *   <span data-ttu-id="7e958-131">Choose **Start Instrumenting Coverage and Reload Page** \( Start ![ Instrumenting Coverage and Reload Page ][ImageReloadIcon] \) if you want to review what code is needed to load the page.</span><span class="sxs-lookup"><span data-stu-id="7e958-131">Choose **Start Instrumenting Coverage And Reload Page** \(![Start Instrumenting Coverage And Reload Page][ImageReloadIcon]\) if you want to review what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="7e958-132">Choisissez **Instrument Coverage** \( Instrument Coverage \) si vous souhaitez passer en revue le code utilisé après avoir ![ ][ImageRecordIcon] interagi avec la page.</span><span class="sxs-lookup"><span data-stu-id="7e958-132">Choose **Instrument Coverage** \(![Instrument Coverage][ImageRecordIcon]\) if you want to review what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="7e958-133">Choisissez **Arrêter l’instrumentage de la couverture et afficher les résultats** \( Arrêter l’instrumentage de la couverture et afficher les résultats \) lorsque vous souhaitez arrêter l’enregistrement de ![ la couverture de ][ImageStopIcon] code.</span><span class="sxs-lookup"><span data-stu-id="7e958-133">Choose **Stop Instrumenting Coverage And Show Results** \(![Stop Instrumenting Coverage And Show Results][ImageStopIcon]\) when you want to stop recording code coverage.</span></span>  
    
## <a name="analyze-code-coverage"></a><span data-ttu-id="7e958-134">Analyser la couverture du code</span><span class="sxs-lookup"><span data-stu-id="7e958-134">Analyze code coverage</span></span>  

<span data-ttu-id="7e958-135">Le tableau du panneau **Couverture** affiche les ressources qui ont été analysées et la quantité de code utilisée dans chaque ressource.</span><span class="sxs-lookup"><span data-stu-id="7e958-135">The table in the **Coverage** panel displays the resources that were analyzed, and how much code is used within each resource.</span></span>  <span data-ttu-id="7e958-136">Choisissez une ligne pour ouvrir cette ressource dans le panneau **Sources** et examiner une répartition ligne par ligne du code utilisé et du code inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7e958-136">Choose a row to open that resource in the **Sources** panel and review a line-by-line breakdown of used code and unused code.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Un rapport de couverture de code" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   <span data-ttu-id="7e958-138">Un rapport de couverture de code</span><span class="sxs-lookup"><span data-stu-id="7e958-138">A code coverage report</span></span>  
:::image-end:::  

*   <span data-ttu-id="7e958-139">La **colonne URL** est l’URL de la ressource qui a été analysée.</span><span class="sxs-lookup"><span data-stu-id="7e958-139">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="7e958-140">La **colonne Type** indique si la ressource contient CSS, JavaScript ou les deux.</span><span class="sxs-lookup"><span data-stu-id="7e958-140">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="7e958-141">La **colonne Nombre total d’octets** est la taille totale de la ressource en octets.</span><span class="sxs-lookup"><span data-stu-id="7e958-141">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="7e958-142">La **colonne Octets inutilisés** est le nombre d’octets qui n’ont pas été utilisés.</span><span class="sxs-lookup"><span data-stu-id="7e958-142">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="7e958-143">La dernière colonne sans nom est une visualisation des colonnes **Octets** totaux et **Octets inutilisés.**</span><span class="sxs-lookup"><span data-stu-id="7e958-143">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="7e958-144">La section rouge de la barre est des octets inutilisés.</span><span class="sxs-lookup"><span data-stu-id="7e958-144">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="7e958-145">La section verte est utilisée en octets.</span><span class="sxs-lookup"><span data-stu-id="7e958-145">The green section is used bytes.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7e958-146">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7e958-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu DevTools Command de Microsoft Edge | Documents Microsoft"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Boutons - Bootstrap"  

> [!NOTE]
> <span data-ttu-id="7e958-149">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e958-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7e958-150">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/coverage/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="7e958-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="7e958-152">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e958-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
