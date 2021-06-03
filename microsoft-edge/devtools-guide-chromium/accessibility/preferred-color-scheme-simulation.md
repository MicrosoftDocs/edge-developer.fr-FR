---
description: Forcez Microsoft Edge DevTools en mode Aperçu du jeu de couleurs.
title: Forcer Microsoft Edge DevTools en mode Aperçu du jeu de couleurs (CSS Prefers Color Scheme)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1cdc9601e9e6fea1f6921c6cc40a1ed8232a0da8
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519148"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="ade60-104">Simulation de jeu de couleurs foncées ou claires</span><span class="sxs-lookup"><span data-stu-id="ade60-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="ade60-105">Les systèmes d’exploitation peuvent afficher n’importe quelle application dans des couleurs plus foncées ou plus claires.</span><span class="sxs-lookup"><span data-stu-id="ade60-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="ade60-106">Le fait de disposer d’un produit web avec un thème clair dans un système d’exploitation en mode sombre constitue un problème d’accessibilité pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ade60-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="ade60-107">Sur le web, vous pouvez utiliser la requête multimédia CSS [prefers-color-scheme][MDNPrefersColorScheme] pour détecter si les utilisateurs préfèrent afficher votre produit dans un schéma de couleurs plus sombre ou plus claire.</span><span class="sxs-lookup"><span data-stu-id="ade60-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to display your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="ade60-108">Utilisez [Microsoft Edge DevTools][DevtoolsIndex] pour simuler un changement du mode sombre au mode clair sans avoir à modifier l’intégralité du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ade60-108">Use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="ade60-109">Ouvrez **le menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="ade60-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="ade60-110">Sélectionnez `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ade60-110">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu Commande" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="ade60-112">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="ade60-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="ade60-113">Type `emulate color` , choose either Emulate **CSS prefers-color-scheme: dark** or Emulate **CSS prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ade60-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Option de modèle de couleurs du menu Commande" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="ade60-115">Option de modèle de **couleurs** du menu Commande</span><span class="sxs-lookup"><span data-stu-id="ade60-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="ade60-116">Il suffit de taper ou de ne pas révéler l’outil qui vous permet de le faire, car il existe également un moyen de choisir un thème pour `dark` `light` [DevTools.][DevtoolsCustomizeDarkTheme]</span><span class="sxs-lookup"><span data-stu-id="ade60-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="ade60-117">Si vous vous demandez ce qu’il faut choisir, assurez-vous que vous choisissez un élément de **menu** de rendu, et non un **élément de** menu Apparence.</span><span class="sxs-lookup"><span data-stu-id="ade60-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="ade60-118">Après avoir choisi un jeu de couleurs, actualisez le document actuel pour afficher le mode simulé.</span><span class="sxs-lookup"><span data-stu-id="ade60-118">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode lumière simulé à l’intérieur Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="ade60-120">Mode lumière simulé à l’intérieur Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ade60-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ade60-121">Affichez et modifiez votre CSS comme n’importe quelle autre page web.</span><span class="sxs-lookup"><span data-stu-id="ade60-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="ade60-122">Pour plus d’informations, [accédez à Prise en main avec l’affichage et la modification de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="ade60-122">For more information, navigate to [Get Started With Viewing And Changing CSS][DevtoolsCssIndex].</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Activer le thème foncé dans Microsoft Edge devTools | Documents Microsoft"
[DevtoolsCssIndex]: ../css/index.md "Prise en main Avec l’affichage et la modification des | Documents Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
