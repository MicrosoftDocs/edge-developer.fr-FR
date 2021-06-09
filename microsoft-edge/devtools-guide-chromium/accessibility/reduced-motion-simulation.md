---
description: Simulez un mouvement réduit à l’aide des outils de développement.
title: Simuler un mouvement réduit à l’aide des outils de développement (CSS préfère le mouvement réduit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7244c2e80bbf9070214b6abd02583792c785953c
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597055"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="7f697-104">Simulation de mouvement réduit</span><span class="sxs-lookup"><span data-stu-id="7f697-104">Reduced motion simulation</span></span>  

<span data-ttu-id="7f697-105">L’animation dans les produits web peut être un problème d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="7f697-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="7f697-106">Les systèmes d’exploitation traitent ce problème en incluant une option pour désactiver les animations afin d’éviter toute confusion chez l’utilisateur et d’éventuels problèmes de santé, tels que le déclenchement de crises.</span><span class="sxs-lookup"><span data-stu-id="7f697-106">Operating systems deal with this problem by including an option to turn off animations to avoid user confusion and potential health-related problems, such as triggering seizures.</span></span>  

<span data-ttu-id="7f697-107">Sur une page web, [][MDNPrefersReducedMotion] vous pouvez utiliser la requête multimédia CSS à mouvement réduit par préférence pour détecter si l’utilisateur préfère afficher des animations.</span><span class="sxs-lookup"><span data-stu-id="7f697-107">On a webpage, you can use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS media query to detect whether the user prefers to display any animations.</span></span>  <span data-ttu-id="7f697-108">Encapsulez ensuite votre code d’animation dans un test, pour exécuter des animations de manière conditionnable.</span><span class="sxs-lookup"><span data-stu-id="7f697-108">Then wrap your animation code in a test, to conditionally run animations.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="7f697-109">Ensuite, testez votre code, comme suit.</span><span class="sxs-lookup"><span data-stu-id="7f697-109">Then test your code, as follows.</span></span>

<span data-ttu-id="7f697-110">Pour simuler le paramètre de mouvement réduit du système d’exploitation, sans avoir à modifier le paramètre de votre système d’exploitation :</span><span class="sxs-lookup"><span data-stu-id="7f697-110">To simulate the operating system's reduced motion setting, without having to change your operating system setting:</span></span>

1.  <span data-ttu-id="7f697-111">Ouvrez **le menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="7f697-111">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="7f697-112">Sélectionnez `Control` + `Shift` + `P` sur Windows/Linux `Command` + `Shift` + `P` ou sur macOS.</span><span class="sxs-lookup"><span data-stu-id="7f697-112">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="7f697-114">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="7f697-114">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="7f697-115">Tapez `reduced` , pour activer et désactiver la simulation.</span><span class="sxs-lookup"><span data-stu-id="7f697-115">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="7f697-116">Choisissez l’option et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7f697-116">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activer ou désactiver le paramètre de mouvement réduit préféré à partir du menu Commande" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="7f697-118">Activer ou désactiver le paramètre de mouvement **réduit préféré** à partir du **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="7f697-118">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7f697-119">Actualisez la page web et vérifiez si vos animations s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="7f697-119">Refresh the webpage and check whether your animations run.</span></span>


## <a name="see-also"></a><span data-ttu-id="7f697-120">Articles associés</span><span class="sxs-lookup"><span data-stu-id="7f697-120">See also</span></span>

* <span data-ttu-id="7f697-121">[Vérifiez que la page est utilisable](test-reduced-ui-motion.md) avec l’animation de l’interface utilisateur désactivée : une démonstration à l’aide d’une page de démonstration, avec des explications.</span><span class="sxs-lookup"><span data-stu-id="7f697-121">[Verify that the page is usable with UI animation turned off](test-reduced-ui-motion.md) - A walkthrough using a demo page, with explanations.</span></span>

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
