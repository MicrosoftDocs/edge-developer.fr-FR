---
title: Simulez un mouvement réduit grâce aux outils de développement (CSS est le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f1bf90de4ac1832fff07e9ac963c26f92adeea2c
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843983"
---
# <span data-ttu-id="8842d-103">Simulation de mouvement réduite</span><span class="sxs-lookup"><span data-stu-id="8842d-103">Reduced Motion Simulation</span></span>  

<span data-ttu-id="8842d-104">Une animation dans des produits Web est susceptible de résoudre un problème d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="8842d-104">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="8842d-105">Les systèmes d’exploitation traitent le problème en incluant une option de désactivation des animations pour éviter toute confusion et risque de problèmes liés à la santé tels que les crises de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="8842d-105">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="8842d-106">Sur le Web, vous pouvez utiliser la requête de média CSS [-Reduced-Motion][MDNPrefersReducedMotion] pour détecter si les utilisateurs préfèrent ne voir aucune animation.</span><span class="sxs-lookup"><span data-stu-id="8842d-106">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="8842d-107">Dans votre produit, vous pouvez encapsuler votre code d’animation dans un test pour éviter d’avoir des animations destinées aux utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="8842d-107">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="8842d-108">À l’aide de [Microsoft Edge devtools][DevtoolsGuideChromiumMain], vous pouvez simuler ce paramètre de mouvement réduit sans avoir à modifier votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8842d-108">Using the [Microsoft Edge DevTools][DevtoolsGuideChromiumMain], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="8842d-109">Ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="8842d-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="8842d-110">Appuyez `Control` + `Shift` + `P` sur Windows ou `Command` + `Shift` + `P` sur MacOS.</span><span class="sxs-lookup"><span data-stu-id="8842d-110">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="8842d-112">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="8842d-112">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="8842d-113">Tapez `reduced` pour activer ou désactiver la simulation.</span><span class="sxs-lookup"><span data-stu-id="8842d-113">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="8842d-114">Sélectionnez l’option et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="8842d-114">Select the option and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de réduction du mouvement de votre choix dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="8842d-116">Activer ou désactiver le paramètre de **réduction du mouvement** de votre choix dans le menu de **commandes**</span><span class="sxs-lookup"><span data-stu-id="8842d-116">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8842d-117">Actualisez la page active pour tester si vos animations sont désactivées ou visibles.</span><span class="sxs-lookup"><span data-stu-id="8842d-117">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Figure 1: menu de commandes"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Figure 2: basculer la réduction de la vidéo à partir de la palette de commandes"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) Microsoft | Documents Microsoft"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "préféré-réduction du mouvement | MDN"  
