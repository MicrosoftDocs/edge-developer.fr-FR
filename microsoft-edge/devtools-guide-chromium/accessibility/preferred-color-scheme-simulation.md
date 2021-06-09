---
description: Forcez Microsoft Edge DevTools en mode Aperçu du jeu de couleurs.
title: Forcer Microsoft Edge DevTools en mode Aperçu du jeu de couleurs (CSS Prefers Color Scheme)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597065"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="0d4b0-104">Simulation de jeu de couleurs foncées ou claires</span><span class="sxs-lookup"><span data-stu-id="0d4b0-104">Dark or light color scheme simulation</span></span>  

<span data-ttu-id="0d4b0-105">De nombreux systèmes d’exploitation ont un moyen d’afficher n’importe quelle application dans des couleurs plus foncées ou plus claires.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-105">Many operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="0d4b0-106">Le fait de disposer d’un produit web avec un thème clair dans un système d’exploitation en mode sombre constitue un problème d’accessibilité pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-106">Having a web product that has a light theme in a dark-mode operating system is grating and can be an accessibility issue for some users.</span></span>  

<span data-ttu-id="0d4b0-107">Pour une page web, vous pouvez utiliser la requête multimédia CSS [prefers-color-scheme][MDNPrefersColorScheme] pour détecter si l’utilisateur préfère afficher votre produit dans un schéma de couleurs plus sombre ou plus clair.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-107">For a webpage, you can use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect whether the user prefers to display your product in a darker or lighter color scheme.</span></span>  <span data-ttu-id="0d4b0-108">Ensuite, pour tester le résultat, utilisez [Microsoft Edge DevTools][DevtoolsIndex] pour simuler un changement de mode sombre en mode clair, sans avoir à modifier le paramètre pour l’ensemble de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-108">Then to test the result, use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode, without having to change the setting for your entire operating system.</span></span>  

**<span data-ttu-id="0d4b0-109">Pour émuler un thème foncé ou clair :</span><span class="sxs-lookup"><span data-stu-id="0d4b0-109">To emulate dark or light theme:</span></span>**

1.  <span data-ttu-id="0d4b0-110">Ouvrez **le menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="0d4b0-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="0d4b0-111">Sélectionnez `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="0d4b0-111">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="0d4b0-113">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="0d4b0-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="0d4b0-114">Type `emulate color` , choose either Emulate **CSS prefers-color-scheme: dark** or Emulate **CSS prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="0d4b0-114">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Option de modèle de couleurs du menu Commande" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="0d4b0-116">Option de modèle de **couleurs** du menu Commande</span><span class="sxs-lookup"><span data-stu-id="0d4b0-116">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="0d4b0-117">Il suffit de taper ou de ne pas révéler l’outil qui vous permet de le faire, car il existe également un moyen de choisir un thème pour `dark` `light` [DevTools.][DevtoolsCustomizeDarkTheme]</span><span class="sxs-lookup"><span data-stu-id="0d4b0-117">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="0d4b0-118">Si vous vous demandez ce qu’il faut choisir, assurez-vous que vous choisissez un élément de **menu** de rendu, et non un **élément de** menu Apparence.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-118">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="0d4b0-119">Après avoir choisi un jeu de couleurs, actualisez le document actuel pour afficher le mode simulé.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-119">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode lumière simulé à l’intérieur Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="0d4b0-121">Mode lumière simulé à l’intérieur Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0d4b0-121">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0d4b0-122">Affichez et modifiez votre CSS comme n’importe quelle autre page web.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-122">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="0d4b0-123">Pour plus d’informations, [accédez à Commencer à afficher et modifier les CSS.][DevtoolsCssIndex]</span><span class="sxs-lookup"><span data-stu-id="0d4b0-123">For more information, navigate to [Get started with viewing and changing CSS][DevtoolsCssIndex].</span></span>  


## <a name="see-also"></a><span data-ttu-id="0d4b0-124">Articles associés</span><span class="sxs-lookup"><span data-stu-id="0d4b0-124">See also</span></span>

* [<span data-ttu-id="0d4b0-125">Vérifier les problèmes de contraste avec le thème foncé et le thème clair</span><span class="sxs-lookup"><span data-stu-id="0d4b0-125">Check for contrast issues with dark theme and light theme</span></span>](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Activer le thème foncé dans Microsoft Edge devTools | Documents Microsoft"
[DevtoolsCssIndex]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
