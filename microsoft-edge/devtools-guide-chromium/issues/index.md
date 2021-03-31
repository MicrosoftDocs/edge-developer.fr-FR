---
description: Utilisez l’outil Problèmes pour rechercher et résoudre les problèmes liés à votre site web.
title: Rechercher et résoudre les problèmes liés à l’outil Problèmes DevTools de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: e16bd926ea5bae35ad82f54ac5d1ae2028e3c59d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398972"
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

# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a><span data-ttu-id="b0763-104">Rechercher et résoudre les problèmes liés à l’outil Problèmes DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b0763-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="b0763-105">**L’outil Problèmes** dans Microsoft Edge DevTools réduit la fatigue et l’encombrement des notifications de la **console.**</span><span class="sxs-lookup"><span data-stu-id="b0763-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="b0763-106">Utilisez-le pour rechercher des solutions aux problèmes détectés par le navigateur, tels que les problèmes de cookie et le contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="b0763-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="b0763-107">Dans Microsoft Edge 84, l’outil **Problèmes** prend en charge trois types de problèmes :</span><span class="sxs-lookup"><span data-stu-id="b0763-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="b0763-108">Problèmes liés aux cookies</span><span class="sxs-lookup"><span data-stu-id="b0763-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="b0763-109">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="b0763-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="b0763-110">Problèmes coEP</span><span class="sxs-lookup"><span data-stu-id="b0763-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="b0763-111">L’équipe Microsoft Edge DevTools prévoit de prendre en charge d’autres types de problèmes dans les futures versions de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b0763-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="b0763-112">Ouvrir l’outil Problèmes dans le caisse de DevTools</span><span class="sxs-lookup"><span data-stu-id="b0763-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="b0763-113">Accédez à une page web, telle que [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], qui contient des problèmes à résoudre.</span><span class="sxs-lookup"><span data-stu-id="b0763-113">Navigate to a webpage, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="b0763-114">[Ouvrez DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="b0763-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="b0763-115">Sélectionnez **le bouton Aller aux problèmes** dans la barre d’avertissement jaune.</span><span class="sxs-lookup"><span data-stu-id="b0763-115">Choose the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Go to Issues button in yellow warning bar when Issues are detected" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="b0763-117">Bouton **Go to Issues** (Aller aux problèmes) dans la barre d’avertissement jaune lorsque des problèmes sont détectés.</span><span class="sxs-lookup"><span data-stu-id="b0763-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="b0763-118">Vous pouvez également choisir **Problèmes dans** le menu **Plus d’outils.**</span><span class="sxs-lookup"><span data-stu-id="b0763-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Outil Problèmes dans le menu Plus d’outils" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="b0763-120">**Outil Problèmes dans** le menu **Plus d’outils**</span><span class="sxs-lookup"><span data-stu-id="b0763-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="b0763-121">Choisissez le **bouton Recharger la page,** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b0763-121">Choose the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Outil Problèmes dans le caisse DevTools avec le bouton Recharger la page" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="b0763-123">**Outil Problèmes dans** le caisse DevTools avec **le bouton Recharger la page**</span><span class="sxs-lookup"><span data-stu-id="b0763-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="b0763-124">Les problèmes signalés dans la **console** sont assez difficiles à comprendre, tels que les avertissements de cookie dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="b0763-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="b0763-125">En fonction des problèmes signalés, vous ne savez peut-être pas clairement ce que vous devez faire.</span><span class="sxs-lookup"><span data-stu-id="b0763-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Outil Problèmes dans le caisse DevTools avec trois problèmes de cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="b0763-127">**Outil Problèmes dans** le caisse DevTools avec trois problèmes de cookie</span><span class="sxs-lookup"><span data-stu-id="b0763-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a><span data-ttu-id="b0763-128">Afficher les éléments dans l’outil Problèmes</span><span class="sxs-lookup"><span data-stu-id="b0763-128">View items in the Issues tool</span></span>  

<span data-ttu-id="b0763-129">**L’outil Problèmes** du panneau DevTools présente des avertissements de manière structurée, agrégée et actionnable.</span><span class="sxs-lookup"><span data-stu-id="b0763-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="b0763-130">Choisissez un élément dans l’outil Problèmes pour obtenir des **conseils** sur la façon de résoudre le problème et de rechercher les ressources affectées.</span><span class="sxs-lookup"><span data-stu-id="b0763-130">Choose an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marquer les cookies entre sites comme problème sécurisé ouvert dans l’outil Problèmes" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="b0763-132">**Marquer les cookies entre sites comme problème** sécurisé ouvert dans **l’outil** Problèmes</span><span class="sxs-lookup"><span data-stu-id="b0763-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b0763-133">Chaque élément possède quatre composants :</span><span class="sxs-lookup"><span data-stu-id="b0763-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="b0763-134">Titre décrivant le problème.</span><span class="sxs-lookup"><span data-stu-id="b0763-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="b0763-135">Description fournissant le contexte et la solution.</span><span class="sxs-lookup"><span data-stu-id="b0763-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="b0763-136">Section **RESSOURCES AFFECTÉEs** qui fait lien vers des ressources dans le contexte DevTools approprié tel que le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="b0763-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="b0763-137">Liens vers des instructions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b0763-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="b0763-138">Choisissez des éléments dans **RESSOURCES AFFECTÉEs** pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="b0763-138">Choose items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="b0763-139">Dans l’exemple suivant, le problème marquer les **cookies** entre sites comme étant sécurisés affecte un cookie et deux demandes.</span><span class="sxs-lookup"><span data-stu-id="b0763-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Ressources affectées ouvertes dans l’outil Problèmes" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="b0763-141">Ressources affectées **ouvertes dans l’outil Problèmes** dans le caisse DevTools</span><span class="sxs-lookup"><span data-stu-id="b0763-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a><span data-ttu-id="b0763-142">Afficher les problèmes en contexte</span><span class="sxs-lookup"><span data-stu-id="b0763-142">View issues in context</span></span>  

1.  <span data-ttu-id="b0763-143">Choisissez un lien de ressource pour afficher l’élément dans le contexte approprié dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0763-143">Choose a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="b0763-144">Dans l’exemple suivant, choisissez `samesite-sandbox.glitch.me` sous **Demandes** pour afficher les cookies joints à cette demande.</span><span class="sxs-lookup"><span data-stu-id="b0763-144">In the following example, choose `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Afficher le cookie affecté dans l’outil Réseau DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="b0763-146">Afficher le cookie affecté dans l’outil Réseau DevTools </span><span class="sxs-lookup"><span data-stu-id="b0763-146">View the affected cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="b0763-147">Faites défiler pour afficher l’élément qui pose problème : pour l’exemple suivant, le `ck02` cookie.</span><span class="sxs-lookup"><span data-stu-id="b0763-147">Scroll to view the item with a problem:  for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="b0763-148">Pointez sur **la colonne SameSite** pour passer en revue la `None` valeur détectée par le problème.</span><span class="sxs-lookup"><span data-stu-id="b0763-148">Hover on the **SameSite** column to review the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Aucune valeur dans la colonne SameSite pour le cookie ck02 dans l’outil Réseau DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="b0763-150">dans la **colonne SameSite** pour le cookie dans l’outil `ck02` Réseau  DevTools</span><span class="sxs-lookup"><span data-stu-id="b0763-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b0763-151">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="b0763-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Tests de cookie SameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenu mixte | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Stratégie d’incorporation d’origine croisée | Groupe communautaire Web"  

> [!NOTE]
> <span data-ttu-id="b0763-157">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0763-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b0763-158">La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/issues/index) et est cochée par [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="b0763-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b0763-160">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0763-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
