---
title: Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: cd6123f235af4ccb87338e1d4db12c03a93a9eaa
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684792"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="4fe3f-103">Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4fe3f-103">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>   



<span data-ttu-id="4fe3f-104">L’outil **problèmes** dans Microsoft Edge devtools réduit la fatigue et l’encombrement de la **console**.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-104">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="4fe3f-105">Utilisez-le pour trouver des solutions aux problèmes détectés par le navigateur, tels que les problèmes liés aux cookies et au contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-105">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="4fe3f-106">Dans Microsoft Edge 84, l’outil **problèmes** prend en charge trois types de problème:</span><span class="sxs-lookup"><span data-stu-id="4fe3f-106">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="4fe3f-107">Problèmes de cookie</span><span class="sxs-lookup"><span data-stu-id="4fe3f-107">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="4fe3f-108">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="4fe3f-108">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="4fe3f-109">Problèmes COEP</span><span class="sxs-lookup"><span data-stu-id="4fe3f-109">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="4fe3f-110">L’équipe Microsoft Edge DevTools envisage de prendre en charge davantage de types de problèmes dans les futures versions de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-110">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="4fe3f-111">Ouvrir l’outil de problèmes dans le tiroir DevTools</span><span class="sxs-lookup"><span data-stu-id="4fe3f-111">Open the Issues tool in the DevTools drawer</span></span>   

1.  <span data-ttu-id="4fe3f-112">Rendez-vous sur une page telle que [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], qui comporte des problèmes de correction.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-112">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="4fe3f-113">[Ouvrez devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="4fe3f-113">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="4fe3f-114">Cliquez sur le bouton **accéder aux problèmes** dans la barre d’avertissement jaune.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-114">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Accéder au bouton problèmes dans la barre d’avertissement jaune lorsque des problèmes sont détectés" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="4fe3f-116">Figure1.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-116">Figure 1.</span></span>  <span data-ttu-id="4fe3f-117">Dans la barre d’avertissement jaune, **accédez au bouton accéder aux problèmes** pour détecter des problèmes.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="4fe3f-118">Vous pouvez également sélectionner **problèmes** dans le menu **autres outils** .</span><span class="sxs-lookup"><span data-stu-id="4fe3f-118">Alternatively, select **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Outil problèmes dans le menu plus d’outils" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="4fe3f-120">Figure2.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-120">Figure 2.</span></span>  <span data-ttu-id="4fe3f-121">Outil **problèmes** dans le menu **plus d’outils**</span><span class="sxs-lookup"><span data-stu-id="4fe3f-121">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="4fe3f-122">Cliquez sur le bouton **recharger la page** , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-122">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Outil problèmes dans le tiroir DevTools avec le bouton recharger la page" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="4fe3f-124">Figure3.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-124">Figure 3.</span></span>  <span data-ttu-id="4fe3f-125">Outil **problèmes** dans le tiroir devtools avec le bouton **recharger la page**</span><span class="sxs-lookup"><span data-stu-id="4fe3f-125">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="4fe3f-126">Les problèmes signalés dans la **console** sont relativement difficiles à comprendre, tels que les avertissements de cookie dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-126">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="4fe3f-127">En fonction des problèmes signalés, il est possible que vous n’ayez pas besoin d’effacer ce que vous devez faire.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-127">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Outil problèmes dans le tiroir DevTools avec trois problèmes de cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="4fe3f-129">Figure4.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-129">Figure 4.</span></span>  <span data-ttu-id="4fe3f-130">Outil **problèmes** dans le tiroir devtools avec trois problèmes de cookie</span><span class="sxs-lookup"><span data-stu-id="4fe3f-130">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4fe3f-131">Afficher les éléments dans l’outil Erreurs</span><span class="sxs-lookup"><span data-stu-id="4fe3f-131">View items in the Issues tool</span></span>   

<span data-ttu-id="4fe3f-132">L’outil de **problèmes** du tiroir devtools présente des avertissements de manière structurée, agrégée et exploitable.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-132">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="4fe3f-133">Pour obtenir des instructions sur la façon de résoudre le problème et de trouver les ressources affectées, sélectionnez un élément dans l’outil **problèmes** .</span><span class="sxs-lookup"><span data-stu-id="4fe3f-133">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marquer des cookies intersites comme un problème de sécurité ouvrir dans l’outil problèmes" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="4fe3f-135">Figure5.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-135">Figure 5.</span></span>  <span data-ttu-id="4fe3f-136">**Marquer des cookies intersites comme** un problème de sécurité ouvrir dans l’outil **problèmes**</span><span class="sxs-lookup"><span data-stu-id="4fe3f-136">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="4fe3f-137">Chaque article comporte quatre composants:</span><span class="sxs-lookup"><span data-stu-id="4fe3f-137">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="4fe3f-138">Titre décrivant le problème.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-138">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="4fe3f-139">Une description fournissant le contexte et la solution.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-139">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="4fe3f-140">Section **ressources affectées** qui comporte des liens vers des ressources au sein du contexte devtools approprié, tel que le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-140">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="4fe3f-141">Des liens vers des conseils supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-141">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="4fe3f-142">Sélectionnez les éléments des **ressources affectées** pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-142">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="4fe3f-143">Dans l’exemple suivant, l' **option marquer les cookies intersites comme problème sécurisé** affecte un cookie et deux requêtes.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-143">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Les ressources affectées sont ouvertes dans l’onglet tiroir de problèmes" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="4fe3f-145">Figure6.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-145">Figure 6.</span></span>  <span data-ttu-id="4fe3f-146">Ressources concernées ouvertes dans l’outil **problèmes** du tiroir-devtools</span><span class="sxs-lookup"><span data-stu-id="4fe3f-146">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4fe3f-147">Afficher les problèmes en contexte</span><span class="sxs-lookup"><span data-stu-id="4fe3f-147">View issues in context</span></span>   

1.  <span data-ttu-id="4fe3f-148">Sélectionnez un lien vers une ressource pour afficher l’élément dans le contexte approprié dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-148">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="4fe3f-149">Dans l’exemple suivant, sélectionnez `samesite-sandbox.glitch.me` sous **demandes** pour afficher les cookies joints à cette demande.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-149">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Afficher le cookie affecté dans le volet réseau de DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="4fe3f-151">Figure7.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-151">Figure 7.</span></span>  <span data-ttu-id="4fe3f-152">Afficher le cookie affecté dans le volet réseau de DevTools</span><span class="sxs-lookup"><span data-stu-id="4fe3f-152">View the affected cookie in the DevTools Network panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="4fe3f-153">Faites défiler pour afficher l’élément présentant un problème: pour l’exemple suivant, le `ck02` cookie.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-153">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="4fe3f-154">Positionnez le pointeur sur la colonne **SameSite** pour afficher la `None` valeur du problème détecté.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-154">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Valeur None dans la colonne SameSite pour le cookie ck02 dans le panneau réseau d’DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       <span data-ttu-id="4fe3f-156">Figure8.</span><span class="sxs-lookup"><span data-stu-id="4fe3f-156">Figure 8.</span></span>  `None` <span data-ttu-id="4fe3f-157">la valeur de la colonne **SameSite** pour le `ck02` cookie dans le volet **réseau** devtools</span><span class="sxs-lookup"><span data-stu-id="4fe3f-157">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

<!--## Feedback  -->  



<!-- image links -->  

<!-- links -->  

[DevtoolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Tests de cookies SameSite | Problème"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenu mixte | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Stratégie d’intégration d’une origination Groupe de communauté d’incubateur Web"  

> [!NOTE]
> <span data-ttu-id="4fe3f-163">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4fe3f-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4fe3f-164">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/issues/index) et est créée par [Sam Dutton][SamDutton] \ (défenseur du développeur \).</span><span class="sxs-lookup"><span data-stu-id="4fe3f-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="4fe3f-166">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4fe3f-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
