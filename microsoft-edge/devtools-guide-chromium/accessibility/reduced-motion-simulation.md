---
description: Simulez un mouvement réduit grâce aux outils de développement.
title: Simulez un mouvement réduit grâce aux outils de développement (CSS est le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230788"
---
# <span data-ttu-id="29ecf-104">Simulation de mouvement réduite</span><span class="sxs-lookup"><span data-stu-id="29ecf-104">Reduced Motion Simulation</span></span>  

<span data-ttu-id="29ecf-105">Une animation dans des produits Web est susceptible de résoudre un problème d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="29ecf-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="29ecf-106">Les systèmes d’exploitation traitent le problème en incluant une option de désactivation des animations pour éviter toute confusion et risque de problèmes liés à la santé tels que les crises de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="29ecf-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="29ecf-107">Sur le Web, vous pouvez utiliser la requête de média CSS [-Reduced-Motion][MDNPrefersReducedMotion] pour détecter si les utilisateurs préfèrent ne voir aucune animation.</span><span class="sxs-lookup"><span data-stu-id="29ecf-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="29ecf-108">Dans votre produit, vous pouvez encapsuler votre code d’animation dans un test pour éviter d’avoir des animations destinées aux utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="29ecf-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="29ecf-109">À l’aide de [Microsoft Edge devtools][DevtoolsIndex], vous pouvez simuler ce paramètre de mouvement réduit sans avoir à modifier votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="29ecf-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="29ecf-110">Ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="29ecf-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="29ecf-111">Sélectionnez `Control` + `Shift` + `P` Windows/Linux ou `Command` + `Shift` + `P` MacOS.</span><span class="sxs-lookup"><span data-stu-id="29ecf-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="29ecf-113">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="29ecf-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="29ecf-114">Tapez `reduced` pour activer ou désactiver la simulation.</span><span class="sxs-lookup"><span data-stu-id="29ecf-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="29ecf-115">Sélectionnez l’option et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="29ecf-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de réduction du mouvement de votre choix dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="29ecf-117">Activer ou désactiver le paramètre de **réduction du mouvement** de votre choix dans le menu de **commandes**</span><span class="sxs-lookup"><span data-stu-id="29ecf-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="29ecf-118">Actualisez la page active pour tester si vos animations sont désactivées ou visibles.</span><span class="sxs-lookup"><span data-stu-id="29ecf-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "préféré-réduction du mouvement | MDN"  
