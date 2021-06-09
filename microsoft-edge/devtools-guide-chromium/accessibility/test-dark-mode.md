---
description: Recherchez les problèmes de contraste avec le thème foncé et le thème clair (pour le mode sombre et le mode clair) à l’aide de la liste de listes de listes listes dans l’outil de rendu « Émuler la fonctionnalité multimédia CSS prefers-color-scheme\ ».
title: Vérifier les problèmes de contraste avec le thème foncé et le thème clair
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 052c75b610ec872329f387e46819867f299a8ca9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597366"
---
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a><span data-ttu-id="c0e66-104">Vérifier les problèmes de contraste avec le thème foncé et le thème clair</span><span class="sxs-lookup"><span data-stu-id="c0e66-104">Check for contrast issues with dark theme and light theme</span></span>

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

<span data-ttu-id="c0e66-105">Lorsque vous testez l’accessibilité des couleurs, il peut y avoir différents thèmes de couleur d’affichage que vous devez tester pour les problèmes de contraste.</span><span class="sxs-lookup"><span data-stu-id="c0e66-105">When testing color accessibility, there could be different display color themes that you need to test for contrast issues.</span></span>

<span data-ttu-id="c0e66-106">La plupart des systèmes d’exploitation sont en mode sombre et clair.</span><span class="sxs-lookup"><span data-stu-id="c0e66-106">Most operating systems come with a dark mode and a light mode.</span></span>  <span data-ttu-id="c0e66-107">Votre page web peut réagir à ce paramètre de système d’exploitation à l’aide d’une requête multimédia CSS.</span><span class="sxs-lookup"><span data-stu-id="c0e66-107">Your webpage can react to this operating system setting, by using a CSS media query.</span></span>  <span data-ttu-id="c0e66-108">Vous pouvez tester ces thèmes et tester votre requête multimédia CSS sans avoir à modifier le paramètre de votre système d’exploitation, à l’aide des options CSS de l’outil `prefers-color-scheme` **de** rendu.</span><span class="sxs-lookup"><span data-stu-id="c0e66-108">You can test these themes and test your CSS media query without having to change your operating system setting, by using the `prefers-color-scheme` CSS options in the **Rendering** tool.</span></span>

<span data-ttu-id="c0e66-109">Par exemple, la page de démonstration des tests d’accessibilité inclut un thème clair et un thème foncé.</span><span class="sxs-lookup"><span data-stu-id="c0e66-109">As an example, the accessibility-testing demo page includes a light theme and a dark theme.</span></span>  <span data-ttu-id="c0e66-110">La page de démonstration hérite du paramètre de thème foncé ou clair du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c0e66-110">The demo page inherits the dark or light theme setting from the operating system.</span></span>  <span data-ttu-id="c0e66-111">Si nous utilisons DevTools pour simuler la mise en place d’un \*\*\*\* schéma lumineux pour le système d’exploitation, puis actualiser la page web de démonstration, l’outil Problèmes montre six problèmes de contraste de couleur au lieu de deux.</span><span class="sxs-lookup"><span data-stu-id="c0e66-111">If we use DevTools to simulate the operating system being set to a light scheme and then refresh the demo webpage, the **Issues** tool shows six color-contrast problems instead of two.</span></span>  <span data-ttu-id="c0e66-112">(Vous pouvez voir des nombres différents.)</span><span class="sxs-lookup"><span data-stu-id="c0e66-112">(You might see different numbers.)</span></span>


<span data-ttu-id="c0e66-113">Pour émuler la sélection d’un thème de couleur préféré par un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c0e66-113">To emulate a user's selection of preferred color theme:</span></span>

1.  <span data-ttu-id="c0e66-114">Ouvrez la [page web][DevToolsA11yErrorsDemopage] de démonstration des tests d’accessibilité dans un nouvel onglet du navigateur, puis sélectionnez **F12** pour ouvrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0e66-114">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="c0e66-115">Sélectionnez **Échap** pour ouvrir le caisse en bas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0e66-115">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="c0e66-116">Sélectionnez l’icône en haut du caisse pour voir la liste des outils, puis **+** sélectionnez **Rendu.**</span><span class="sxs-lookup"><span data-stu-id="c0e66-116">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  <span data-ttu-id="c0e66-117">L’outil de rendu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c0e66-117">The Rendering tool appears.</span></span>

1.  <span data-ttu-id="c0e66-118">Dans la **fonctionnalité émuler CSS media prefers-color-scheme** dropdown list, select **prefers-color-scheme: light**.</span><span class="sxs-lookup"><span data-stu-id="c0e66-118">In the **Emulate CSS media feature prefers-color-scheme** dropdown list, select **prefers-color-scheme: light**.</span></span>      <span data-ttu-id="c0e66-119">La page web est restituer à l’aide `light-theme.css` de .</span><span class="sxs-lookup"><span data-stu-id="c0e66-119">The webpage is re-rendered using `light-theme.css`.</span></span>


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Utilisation de l’outil de rendu pour simuler un mode clair et déclencher l’autre thème du document" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        <span data-ttu-id="c0e66-121">Utilisation de l’outil de rendu pour simuler un mode clair et déclencher l’autre thème du document</span><span class="sxs-lookup"><span data-stu-id="c0e66-121">Using the Rendering tool to simulate a light mode and triggering the other theme of the document</span></span>
    :::image-end:::


1.  <span data-ttu-id="c0e66-122">Sélectionnez **l’outil Problèmes,** puis développez la section **Accessibilité.**</span><span class="sxs-lookup"><span data-stu-id="c0e66-122">Select the **Issues** tool, and then expand the **Accessibility** section.</span></span>  <span data-ttu-id="c0e66-123">En fonction de différents facteurs, vous pouvez obtenir `Insufficient color contrast` des avertissements.</span><span class="sxs-lookup"><span data-stu-id="c0e66-123">Depending on various factors, you might get `Insufficient color contrast` warnings.</span></span> <span data-ttu-id="c0e66-124">Notez que **dans RESSOURCES AFFECTÉEs,** il existe 6 éléments avec un contraste de couleur insuffisant.</span><span class="sxs-lookup"><span data-stu-id="c0e66-124">Notice in **AFFECTED RESOURCES** there are 6 elements with insufficient color contrast.</span></span>
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Nouveaux problèmes de contraste détectés en raison de la modification du thème clair" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        <span data-ttu-id="c0e66-126">Nouveaux problèmes de contraste détectés en raison de la modification du thème clair</span><span class="sxs-lookup"><span data-stu-id="c0e66-126">New contrast issues detected because of the change to light theme</span></span>
    :::image-end:::
    
    <span data-ttu-id="c0e66-127">Dans notre page de démonstration, la section **Sur** l’état du don de la page est illisible en mode clair et doit changer.</span><span class="sxs-lookup"><span data-stu-id="c0e66-127">On our demo page, the **Donation status** section of the page is unreadable in light mode, and needs to change.</span></span> 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="La section État du don présente des problèmes de contraste en mode clair" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        <span data-ttu-id="c0e66-129">La section **État du** don présente des problèmes de contraste en mode clair</span><span class="sxs-lookup"><span data-stu-id="c0e66-129">The **Donation Status** section has contrast issues in light mode</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="c0e66-130">Dans DevTools, sélectionnez l’outil **Elements,** puis **Ctrl+F** sur Windows/Linux ou **Command+F** sur macOS.</span><span class="sxs-lookup"><span data-stu-id="c0e66-130">In DevTools, select the **Elements** tool, and then select **Ctrl+F** on Windows/Linux or **Command+F** on macOS.</span></span>  <span data-ttu-id="c0e66-131">La **zone de** texte Rechercher s’affiche pour effectuer une recherche dans l’arborescence DOM HTML.</span><span class="sxs-lookup"><span data-stu-id="c0e66-131">The **Find** textbox appears, to search within the HTML DOM tree.</span></span>
 
1.  <span data-ttu-id="c0e66-132">Entrez `scheme` .</span><span class="sxs-lookup"><span data-stu-id="c0e66-132">Enter `scheme`.</span></span>  <span data-ttu-id="c0e66-133">Les requêtes multimédias CSS suivantes sont trouvées et les fichiers CSS correspondants peuvent maintenant être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c0e66-133">The following CSS media queries are found, and the corresponding CSS files can now be updated.</span></span>

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a><span data-ttu-id="c0e66-134">Articles associés</span><span class="sxs-lookup"><span data-stu-id="c0e66-134">See also</span></span>

*  [<span data-ttu-id="c0e66-135">Simulation de jeu de couleurs sombres ou claires</span><span class="sxs-lookup"><span data-stu-id="c0e66-135">Dark or light color scheme simulation</span></span>][DevToolsColorSchemeSimulation]
*  [<span data-ttu-id="c0e66-136">Vue d’ensemble des tests d’accessibilité à l’aide de DevTools</span><span class="sxs-lookup"><span data-stu-id="c0e66-136">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c0e66-137">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="c0e66-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Modèle de simulation de jeu de couleurs sombres ou claires | Documents Microsoft"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Page web de démonstration de test d’accessibilité | GitHub"
