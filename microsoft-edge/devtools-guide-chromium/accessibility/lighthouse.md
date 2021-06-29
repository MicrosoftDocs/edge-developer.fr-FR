---
description: Test de l’accessibilité à l’aide de l’outil DevTools.
title: Tester l’accessibilité à l’aide de Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 822c25240ba30df31416ca783bf48d6d9ba52ed2
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624632"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a><span data-ttu-id="dac94-104">Tester l’accessibilité à l’aide de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="dac94-104">Test accessibility using Lighthouse</span></span>

<span data-ttu-id="dac94-105">Vous pouvez utiliser l’aide de DevTools à partir de DevTools pour auditer l’accessibilité d’une page et générer un rapport.</span><span class="sxs-lookup"><span data-stu-id="dac94-105">You can use Lighthouse from within DevTools to audit the accessibility of a page and generate a report.</span></span> <span data-ttu-id="dac94-106">Vous pouvez utiliser l’outil Contrôle d’accès pour déterminer :</span><span class="sxs-lookup"><span data-stu-id="dac94-106">You can use the Lighthouse tool to determine:</span></span>

*   <span data-ttu-id="dac94-107">Si une page est correctement marquée pour les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="dac94-107">Whether a page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="dac94-108">Si les éléments de texte d’une page ont des coefficients de contraste suffisants à l’aide du s sélectionneur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="dac94-108">Whether the text elements on a page have sufficient contrast ratios using the Color Picker.</span></span> <span data-ttu-id="dac94-109">Pour plus d’informations, accédez à Tester le contraste de couleur du texte à [l’aide du s sélectionneur de couleurs.](color-picker.md)</span><span class="sxs-lookup"><span data-stu-id="dac94-109">For more information, navigate to [Test text-color contrast using the Color Picker](color-picker.md).</span></span>   

> [!NOTE]
> <span data-ttu-id="dac94-110">**L’outil Îles** fournit des liens vers du contenu hébergé sur des sites web tiers.</span><span class="sxs-lookup"><span data-stu-id="dac94-110">The **Lighthouse** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="dac94-111">Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et les données qui peuvent être collectées.</span><span class="sxs-lookup"><span data-stu-id="dac94-111">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="dac94-112">Pour auditer une page à l’aide de l’outil Contrôle d’accès, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="dac94-112">To audit a page using the Lighthouse tool, perform the following steps.</span></span>

1.  <span data-ttu-id="dac94-113">Accédez à l’URL que vous souhaitez auditer.</span><span class="sxs-lookup"><span data-stu-id="dac94-113">Navigate to the URL that you want to audit.</span></span>
1.  <span data-ttu-id="dac94-114">Dans DevTools, sélectionnez **l’outil** DevTools.</span><span class="sxs-lookup"><span data-stu-id="dac94-114">In DevTools, select the **Lighthouse** tool.</span></span>  <span data-ttu-id="dac94-115">Les options de configuration s’affichent.</span><span class="sxs-lookup"><span data-stu-id="dac94-115">Configuration options are displayed.</span></span>
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Options de configuration de l’ordinateur" lightbox="../media/accessibility-lighthouse.msft.png":::
       <span data-ttu-id="dac94-117">Options de configuration de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="dac94-117">Lighthouse configuration options</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="dac94-118">Pour **l’appareil,** **sélectionnez Mobile** si vous souhaitez simuler un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="dac94-118">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="dac94-119">Cette option modifie la chaîne de votre agent utilisateur et resize laport d’affichage.</span><span class="sxs-lookup"><span data-stu-id="dac94-119">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="dac94-120">Cette option peut affecter les résultats de l’audit.</span><span class="sxs-lookup"><span data-stu-id="dac94-120">This option can affect the audit results.</span></span>
1.  <span data-ttu-id="dac94-121">Dans la section **Catégories,** sélectionnez **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="dac94-121">In the **Categories** section, select **Accessibility**.</span></span>
1.  <span data-ttu-id="dac94-122">Sélectionnez **Générer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="dac94-122">Select **Generate report**.</span></span> <span data-ttu-id="dac94-123">Après 10 à 30 secondes, DevTools affiche un rapport.</span><span class="sxs-lookup"><span data-stu-id="dac94-123">After 10 to 30 seconds, DevTools displays a report.</span></span>  <span data-ttu-id="dac94-124">Le rapport fournit des conseils sur la façon d’améliorer l’accessibilité de la page.</span><span class="sxs-lookup"><span data-stu-id="dac94-124">The report gives tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Un rapport de classe pour la catégorie Accessibilité" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       <span data-ttu-id="dac94-126">Un rapport de classe pour la **catégorie Accessibilité**</span><span class="sxs-lookup"><span data-stu-id="dac94-126">A Lighthouse report for the **Accessibility** category</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="dac94-127">Sélectionnez un élément dans le rapport pour en savoir plus à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="dac94-127">Select an item in the report to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Un problème développé dans un rapport Dente" lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       <span data-ttu-id="dac94-129">Un problème développé dans un rapport Dente</span><span class="sxs-lookup"><span data-stu-id="dac94-129">An expanded issue in a Lighthouse report</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="dac94-130">Sélectionnez **le lien En savoir** plus pour afficher la documentation du problème.</span><span class="sxs-lookup"><span data-stu-id="dac94-130">Select the **Learn more** link to view the documentation of the issue.</span></span>
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Afficher la documentation d’un problème" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="dac94-132">Afficher la documentation d’un problème</span><span class="sxs-lookup"><span data-stu-id="dac94-132">View the documentation of an issue</span></span>
    :::image-end:::  

1.  <span data-ttu-id="dac94-133">Pour revenir aux options de configuration, dans DevTools, **sélectionnez Effectuer un audit** ( `+` ).</span><span class="sxs-lookup"><span data-stu-id="dac94-133">To return to the configuration options, in DevTools, select **Perform an audit** (`+`).</span></span>    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="dac94-134">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="dac94-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="dac94-135">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dac94-135">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dac94-136">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="dac94-136">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="dac94-138">Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dac94-138">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd "axe - Test d’accessibilité web - Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
