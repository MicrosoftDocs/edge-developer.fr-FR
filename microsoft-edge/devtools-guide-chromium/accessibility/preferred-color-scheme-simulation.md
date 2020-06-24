---
title: Forcez Microsoft Edge DevTools en mode d’aperçu du jeu de couleurs (CSS préfère le modèle de couleurs)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758081"
---
# <span data-ttu-id="e62c5-103">Simulation de jeu de couleurs sombre ou léger</span><span class="sxs-lookup"><span data-stu-id="e62c5-103">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="e62c5-104">Les systèmes d’exploitation peuvent afficher n’importe quelle application en couleurs plus sombres ou plus claires.</span><span class="sxs-lookup"><span data-stu-id="e62c5-104">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="e62c5-105">Le fait de disposer d’un produit Web comportant un thème clair dans un système d’exploitation en mode foncé est un réseau qui peut être un problème d’accessibilité pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e62c5-105">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="e62c5-106">Sur le Web, vous pouvez utiliser la requête de médias CSS de [jeu de couleurs][MDNPrefersColorScheme] pour détecter si les utilisateurs préfèrent voir votre produit dans le cadre d’un jeu de couleurs plus sombre ou plus clair.</span><span class="sxs-lookup"><span data-stu-id="e62c5-106">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="e62c5-107">Utilisez [Microsoft Edge devtools][DevtoolsGuideChromiumMain] pour simuler une modification du mode sombre au mode clair sans avoir à modifier l’intégralité du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e62c5-107">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="e62c5-108">Ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-108">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="e62c5-109">Appuyez `Control` + `Shift` + `P` sur Windows ou `Command` + `Shift` + `P` sur MacOS.</span><span class="sxs-lookup"><span data-stu-id="e62c5-109">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="e62c5-111">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="e62c5-111">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="e62c5-112">Tapez `emulate color` , sélectionnez **émuler des feuilles de style CSS préféré-jeu de couleurs: Dark** ou **émuler des feuilles de style CSS préféré-couleur: clair** , puis appuyer `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e62c5-112">Type `emulate color`, select either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light**  and then press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Sélection des jeux de couleurs dans le menu de commandes" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="e62c5-114">Sélection des jeux de couleurs dans le menu de **commandes**</span><span class="sxs-lookup"><span data-stu-id="e62c5-114">Color scheme selection from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="e62c5-115">Il suffit de taper `dark` ou de `light` ne pas afficher l’outil approprié, car il existe également un moyen de [choisir un thème pour devtools][DevtoolsGuideChromiumCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="e62c5-115">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="e62c5-116">Si vous vous demandez ce qu’il faut choisir, assurez-vous de sélectionner un élément de menu de **rendu** , et non un élément de menu **apparence** .</span><span class="sxs-lookup"><span data-stu-id="e62c5-116">If you are wondering what to choose, make sure that you are selecting a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="e62c5-117">Après avoir sélectionné un modèle de couleurs, rechargez le document actuel pour afficher le mode simulé.</span><span class="sxs-lookup"><span data-stu-id="e62c5-117">After you select a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Mode Light simulé dans Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="e62c5-119">Mode Light simulé dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e62c5-119">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e62c5-120">Affichez et modifiez votre CSS comme n’importe quelle autre page Web.</span><span class="sxs-lookup"><span data-stu-id="e62c5-120">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="e62c5-121">Pour plus d’informations, voir [commencer à afficher et modifier des feuilles CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="e62c5-121">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) Microsoft | Documents Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Activer un thème foncé dans Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "préférence-jeu de couleurs | MDN"  
