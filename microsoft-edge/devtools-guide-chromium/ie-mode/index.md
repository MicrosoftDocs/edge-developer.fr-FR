---
description: Le mode IE et Microsoft Edge (Chromium) DevTools
title: Mode Internet Explorer et DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, ie11, internet explorer 11, mode ie
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643234"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="7b2f8-104">Mode Internet Explorer et DevTools</span><span class="sxs-lookup"><span data-stu-id="7b2f8-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="7b2f8-105">Cet article explique comment le mode Internet Explorer \(IE mode\) s’intègre à l’Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="7b2f8-106">Comprendre le mode IE</span><span class="sxs-lookup"><span data-stu-id="7b2f8-106">Understanding IE mode</span></span>  

<span data-ttu-id="7b2f8-107">Le mode IE permet aux entreprises de spécifier une liste de sites web qui fonctionnent uniquement dans Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="7b2f8-108">Lorsque vous accédez à ces sites web dans Microsoft Edge \(Chromium\), une instance d’Internet Explorer 11 s’exécute et restituer le site dans un onglet.  Cette fonctionnalité permet aux entreprises de gérer la compatibilité avec les technologies qui ne sont actuellement compatibles avec aucun navigateur web moderne.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="7b2f8-109">La prise en charge des technologies suivantes est incluse en mode IE.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="7b2f8-110">Modes de document d’IE</span><span class="sxs-lookup"><span data-stu-id="7b2f8-110">IE document modes</span></span>  
*   <span data-ttu-id="7b2f8-111">contrôles ActiveX ;</span><span class="sxs-lookup"><span data-stu-id="7b2f8-111">ActiveX controls</span></span>  
*   <span data-ttu-id="7b2f8-112">autres composants hérités</span><span class="sxs-lookup"><span data-stu-id="7b2f8-112">other legacy components</span></span>  

<span data-ttu-id="7b2f8-113">En mode IE, le processus de rendu est basé sur Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="7b2f8-114">Le Microsoft Edge de processus \(Chromium\) gère la durée de vie du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="7b2f8-115">Il est limité à la durée de vie de l’onglet pour un site spécifique \(ou une application\).</span><span class="sxs-lookup"><span data-stu-id="7b2f8-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="7b2f8-116">Lorsqu’un onglet s’affiche en mode IE, un badge apparaît dans la barre d’adresses de l’onglet spécifique.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Badge du mode IE dans la barre d’adresses" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="7b2f8-118">Badge du mode IE dans la barre d’adresses</span><span class="sxs-lookup"><span data-stu-id="7b2f8-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="7b2f8-119">Le mode IE est actuellement disponible sur Windows 10 version 1903 \(mise à jour de mai 2019\), mais il sera bientôt disponible pour toutes les plateformes Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="7b2f8-120">Lancement de DevTools sur un onglet en mode IE</span><span class="sxs-lookup"><span data-stu-id="7b2f8-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="7b2f8-121">Si vous essayez d’afficher le mode document d’un site web en mode IE, choisissez le badge dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Afficher le mode document à l’aide du badge du mode IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="7b2f8-123">Afficher le mode document à l’aide du badge du mode IE</span><span class="sxs-lookup"><span data-stu-id="7b2f8-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="7b2f8-124">Si un onglet utilise le mode IE, les DevTools ne fonctionnent pas et les conditions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="7b2f8-125">Si vous sélectionnez ou sélectionnez, une instance vide de l’Microsoft Edge `F12` `Ctrl` + `Shift` + `I` \(Chromium\) DevTools est lancée et affiche le message suivant.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="7b2f8-126">Si vous ouvrez un menu contextuel \(clic droit\) et choisissez **Afficher la source,** Bloc-notes est lancée.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="7b2f8-127">Si vous ouvrez un menu contextuel \(clic droit\), **l’élément Inspect n’est** pas visible.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="7b2f8-128">La raison pour laquelle un certain nombre d’outils \*\*\*\* au \*\*\*\* sein de DevTools \(comme les outils réseau et performance\) ne fonctionnent pas est que le moteur de rendu passe de Chromium à Internet Explorer 11 en mode IE.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="7b2f8-129">Pour fournir des commentaires, accédez à La mise en [contact avec l Microsoft Edge devTools.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="7b2f8-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools lancé en mode IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="7b2f8-131">DevTools lancé en mode IE</span><span class="sxs-lookup"><span data-stu-id="7b2f8-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="7b2f8-132">Pour tester votre site web Internet Explorer 11 \(ou application\) en mode Internet Explorer 11 et Internet Explorer, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="7b2f8-133">Ouvrez Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="7b2f8-134">Sur Windows 10, recherchez le raccourci pour Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="7b2f8-135">**Menu Démarrer**  >  **Windows accessoires**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="7b2f8-136">Sur Windows 7, recherchez Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="7b2f8-137">**Menu Démarrer**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="7b2f8-138">Dans Internet Explorer 11, ouvrez la même page web.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="7b2f8-139">Lancez Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="7b2f8-140">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="7b2f8-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="7b2f8-141">Pointez n’importe où, ouvrez un menu contextuel \(clic droit\), puis choisissez **l’élément Inspect**.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="7b2f8-142">Pour plus d’informations sur l’utilisation de ces outils, accédez à Utiliser les outils de [développement F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]</span><span class="sxs-lookup"><span data-stu-id="7b2f8-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

<span data-ttu-id="7b2f8-143">Si Internet Explorer 11 n’est pas disponible, comme sur Windows 11, vous pouvez utiliser IEChooser pour lancer Internet Explorer DevTools pour déboguer le contenu de vos onglets en mode IE.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-143">If Internet Explorer 11 is not available, such as on Windows 11, you can use IEChooser to launch the Internet Explorer DevTools to debug the content of your IE mode tabs.</span></span> <span data-ttu-id="7b2f8-144">Pour utiliser IEChooser, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-144">To use IEChooser, perform the following steps.</span></span>

1.  <span data-ttu-id="7b2f8-145">Ouvrez IEChooser.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-145">Open IEChooser.</span></span>
    1. <span data-ttu-id="7b2f8-146">Ouvre la boîte de dialogue Exécuter.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-146">Open the Run dialog box.</span></span> <span data-ttu-id="7b2f8-147">Par exemple, appuyez sur `Windows logo key`  +  `R` le .</span><span class="sxs-lookup"><span data-stu-id="7b2f8-147">For example, press the `Windows logo key` + `R`.</span></span>
    2. <span data-ttu-id="7b2f8-148">Entrez, `%systemroot%\system32\f12\IEChooser.exe` puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="7b2f8-148">Enter `%systemroot%\system32\f12\IEChooser.exe`, and then select **Ok**.</span></span>
2.  <span data-ttu-id="7b2f8-149">Dans IEChooser, sélectionnez l’entrée de l’onglet mode IE.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-149">In IEChooser, select the entry for the IE mode tab.</span></span>


## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="7b2f8-150">Débogage à distance et mode IE</span><span class="sxs-lookup"><span data-stu-id="7b2f8-150">Remote debugging and IE mode</span></span>  

<span data-ttu-id="7b2f8-151">Lancez Microsoft Edge \(Chromium\) avec débogage à distance allumé à partir de l’interface de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-151">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="7b2f8-152">Microsoft Visual Studio, Microsoft Visual Studio Code et d’autres outils de développement exécutent généralement une commande pour lancer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-152">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="7b2f8-153">La commande suivante lance Microsoft Edge port de débogage `9222` distant.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-153">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="7b2f8-154">Après avoir lancé Microsoft Edge \(Chromium\) à l’aide d’un argument de ligne de commande, le mode IE n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-154">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="7b2f8-155">Vous pouvez toujours accéder aux sites web \(ou applications\) qui sont affichés en mode IE.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-155">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="7b2f8-156">Le contenu du site web \(ou application\) s’Chromium, et non d’Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-156">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="7b2f8-157">Attendez-vous à ce que les parties des pages web qui reposent sur IE11, telles que ActiveX contrôles, ne s’restituer pas correctement.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-157">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="7b2f8-158">Le badge du mode IE n’apparaît pas dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7b2f8-158">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="7b2f8-159">Le mode IE reste indisponible tant que vous n’avez pas complètement fermé et redémarré Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7b2f8-159">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7b2f8-160">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7b2f8-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Utilisation des outils de développement F12 | Documents Microsoft"  
