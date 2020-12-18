---
Description: Forcez Microsoft Edge DevTools en mode d’aperçu du jeu de couleurs.
title: Forcez Microsoft Edge DevTools en mode d’aperçu du jeu de couleurs (CSS préfère le modèle de couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 29b0121a616a037fa11b61799efeffd201eb1821
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230795"
---
# <span data-ttu-id="6a8ae-104">Simulation de jeu de couleurs sombre ou léger</span><span class="sxs-lookup"><span data-stu-id="6a8ae-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="6a8ae-105">Les systèmes d’exploitation peuvent afficher n’importe quelle application en couleurs plus sombres ou plus claires.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="6a8ae-106">Le fait de disposer d’un produit Web comportant un thème clair dans un système d’exploitation en mode foncé est un réseau qui peut être un problème d’accessibilité pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="6a8ae-107">Sur le Web, vous pouvez utiliser la requête de médias CSS de [jeu de couleurs][MDNPrefersColorScheme] pour détecter si les utilisateurs préfèrent voir votre produit dans le cadre d’un jeu de couleurs plus sombre ou plus clair.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="6a8ae-108">Utilisez [Microsoft Edge devtools][DevtoolsGuideChromiumMain] pour simuler une modification du mode sombre au mode clair sans avoir à modifier l’intégralité du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-108">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="6a8ae-109">Ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="6a8ae-110">Sélectionnez `Control` + `Shift` + `P` Windows/Linux ou `Command` + `Shift` + `P` MacOS.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-110">Select `Control`+`Shift`+`P`  on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="6a8ae-112">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="6a8ae-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="6a8ae-113">Tapez `emulate color` , choisissez l’option **émuler les feuilles CSS préférée-couleur-jeu: Dark** ou **émuler des feuilles de style CSS préférée-couleur: clair** et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="6a8ae-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Option de jeu de couleurs dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="6a8ae-115">Option de jeu de couleurs dans le menu de **commandes**</span><span class="sxs-lookup"><span data-stu-id="6a8ae-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="6a8ae-116">Il suffit de taper `dark` ou de `light` ne pas afficher l’outil approprié, car il existe également un moyen de [choisir un thème pour devtools][DevtoolsGuideChromiumCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="6a8ae-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="6a8ae-117">Si vous vous demandez ce qu’il faut choisir, assurez-vous de choisir un élément de menu de **rendu** , et non un élément de menu d' **apparence** .</span><span class="sxs-lookup"><span data-stu-id="6a8ae-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="6a8ae-118">Après avoir choisi un modèle de couleurs, rechargez le document actuel pour afficher le mode simulé.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-118">After you choose a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode Light simulé dans Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="6a8ae-120">Mode Light simulé dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6a8ae-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="6a8ae-121">Affichez et modifiez votre CSS comme n’importe quelle autre page Web.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="6a8ae-122">Pour plus d’informations, voir [commencer à afficher et modifier des feuilles CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="6a8ae-122">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Activer un thème foncé dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "préférence-jeu de couleurs | MDN"  
