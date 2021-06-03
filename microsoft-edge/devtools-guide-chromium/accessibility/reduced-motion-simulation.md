---
description: Simulez un mouvement réduit à l’aide des outils de développement.
title: Simuler un mouvement réduit à l’aide des outils de développement (CSS préfère le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397866"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="cfa98-104">Simulation de mouvement réduit</span><span class="sxs-lookup"><span data-stu-id="cfa98-104">Reduced motion simulation</span></span>  

<span data-ttu-id="cfa98-105">L’animation dans les produits web peut être un problème d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="cfa98-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="cfa98-106">Les systèmes d’exploitation traitent le problème en incluant une option pour désactiver les animations afin d’éviter toute confusion chez l’utilisateur et d’éventuels problèmes liés à l’état, tels que le déclenchement de crises.</span><span class="sxs-lookup"><span data-stu-id="cfa98-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="cfa98-107">Sur le web, vous pouvez utiliser la requête multimédia CSS à mouvement réduit pour détecter si les [utilisateurs][MDNPrefersReducedMotion] préfèrent ne pas exécuter ou afficher d’animations.</span><span class="sxs-lookup"><span data-stu-id="cfa98-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not run or display any animations.</span></span>  <span data-ttu-id="cfa98-108">Dans votre produit, vous pouvez encapsuler votre code d’animation dans un test afin d’éviter que des animations ne s’affichent pour les utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="cfa98-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="cfa98-109">À [l’Microsoft Edge DevTools,][DevtoolsIndex]vous pouvez simuler ce paramètre de mouvement réduit sans avoir à modifier votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cfa98-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="cfa98-110">Ouvrez **le menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="cfa98-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="cfa98-111">Sélectionnez `Control` + `Shift` + `P` sur Windows/Linux `Command` + `Shift` + `P` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="cfa98-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="cfa98-113">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="cfa98-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="cfa98-114">Tapez `reduced` , pour activer et désactiver la simulation.</span><span class="sxs-lookup"><span data-stu-id="cfa98-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="cfa98-115">Choisissez l’option et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cfa98-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de mouvement réduit préféré à partir du menu Commande" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="cfa98-117">Activer ou désactiver le paramètre de mouvement **réduit préféré** à partir du **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="cfa98-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cfa98-118">Actualisez la page actuelle pour tester si vos animations sont désactivées ou visibles.</span><span class="sxs-lookup"><span data-stu-id="cfa98-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
