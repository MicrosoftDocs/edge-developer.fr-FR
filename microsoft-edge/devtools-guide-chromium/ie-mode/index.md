---
description: Mode IE et Microsoft Edge (Chromium) DevTools
title: Mode Internet Explorer et DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, ie11, internet explorer 11, mode ie
ms.openlocfilehash: e65869cd88b449dcde0aec25c77df27f99b78f8d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398601"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="8e195-104">Mode Internet Explorer et DevTools</span><span class="sxs-lookup"><span data-stu-id="8e195-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="8e195-105">Cet article explique comment le mode Internet Explorer \(IE mode\) s’intègre à Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e195-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="8e195-106">Comprendre le mode IE</span><span class="sxs-lookup"><span data-stu-id="8e195-106">Understanding IE mode</span></span>  

<span data-ttu-id="8e195-107">Le mode IE permet aux entreprises de spécifier une liste de sites web qui fonctionnent uniquement dans Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="8e195-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="8e195-108">Lorsque vous accédez à ces sites web dans Microsoft Edge \(Chromium\), une instance d’Internet Explorer 11 s’exécute et restituer le site dans un onglet.  Cette fonctionnalité permet aux entreprises de gérer la compatibilité avec les technologies qui ne sont actuellement pas compatibles avec les navigateurs web modernes.</span><span class="sxs-lookup"><span data-stu-id="8e195-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="8e195-109">La prise en charge des technologies suivantes est incluse en mode IE.</span><span class="sxs-lookup"><span data-stu-id="8e195-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="8e195-110">Modes de document d’IE</span><span class="sxs-lookup"><span data-stu-id="8e195-110">IE document modes</span></span>  
*   <span data-ttu-id="8e195-111">contrôles ActiveX;</span><span class="sxs-lookup"><span data-stu-id="8e195-111">ActiveX controls</span></span>  
*   <span data-ttu-id="8e195-112">autres composants hérités</span><span class="sxs-lookup"><span data-stu-id="8e195-112">other legacy components</span></span>  

<span data-ttu-id="8e195-113">En mode IE, le processus de rendu est basé sur Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="8e195-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="8e195-114">Le gestionnaire de processus Microsoft Edge \(Chromium\) gère la durée de vie du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="8e195-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="8e195-115">Il est limité à la durée de vie de l’onglet pour un site spécifique \(ou une application\).</span><span class="sxs-lookup"><span data-stu-id="8e195-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="8e195-116">Lorsqu’un onglet s’affiche en mode IE, un badge apparaît dans la barre d’adresses de l’onglet spécifique.</span><span class="sxs-lookup"><span data-stu-id="8e195-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Badge du mode IE dans la barre d’adresses" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="8e195-118">Badge du mode IE dans la barre d’adresses</span><span class="sxs-lookup"><span data-stu-id="8e195-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="8e195-119">Le mode IE est actuellement disponible sur Windows 10 Version 1903 \(Mise à jour de mai 2019\), mais il sera bientôt disponible sur toutes les plateformes Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8e195-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="8e195-120">Lancement de DevTools sur un onglet en mode IE</span><span class="sxs-lookup"><span data-stu-id="8e195-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="8e195-121">Si vous essayez d’afficher le mode document d’un site web en mode IE, choisissez le badge dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8e195-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Afficher le mode document à l’aide du badge du mode IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="8e195-123">Afficher le mode document à l’aide du badge du mode IE</span><span class="sxs-lookup"><span data-stu-id="8e195-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="8e195-124">Si un onglet utilise le mode IE, devTools ne fonctionne pas et les conditions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="8e195-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="8e195-125">Si vous sélectionnez ou sélectionnez, une instance vide de `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools est lancée et affiche le message suivant.</span><span class="sxs-lookup"><span data-stu-id="8e195-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="8e195-126">Si vous ouvrez un menu contextuel \(clic droit\) et choisissez **Afficher la source,** le Bloc-notes est lancé.</span><span class="sxs-lookup"><span data-stu-id="8e195-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="8e195-127">Si vous ouvrez un menu contextuel \(clic droit\), **l’élément Inspect n’est** pas visible.</span><span class="sxs-lookup"><span data-stu-id="8e195-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="8e195-128">La raison pour laquelle un certain nombre d’outils \*\*\*\* au \*\*\*\* sein de DevTools \(comme les outils réseau et performance\) ne fonctionnent pas est que le moteur de rendu passe de Chromium à Internet Explorer 11 en mode IE.</span><span class="sxs-lookup"><span data-stu-id="8e195-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="8e195-129">Pour fournir des commentaires, accédez à La mise en contact avec l’équipe [Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="8e195-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools lancé en mode IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="8e195-131">DevTools lancé en mode IE</span><span class="sxs-lookup"><span data-stu-id="8e195-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="8e195-132">Pour tester votre site web Internet Explorer 11 \(ou application\) en mode Internet Explorer 11 et Internet Explorer, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e195-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="8e195-133">Ouvrez Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="8e195-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="8e195-134">Sur Windows 10, recherchez le raccourci pour Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="8e195-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="8e195-135">**Menu Démarrer**  >  **Accessoires Windows**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="8e195-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="8e195-136">Sur Windows 7, recherchez Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="8e195-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="8e195-137">**Menu Démarrer**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="8e195-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="8e195-138">Dans Internet Explorer 11, ouvrez la même page web.</span><span class="sxs-lookup"><span data-stu-id="8e195-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="8e195-139">Lancez Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e195-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="8e195-140">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="8e195-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="8e195-141">Pointez n’importe où, ouvrez un menu contextuel \(clic droit\), puis choisissez **l’élément Inspect**.</span><span class="sxs-lookup"><span data-stu-id="8e195-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="8e195-142">Pour plus d’informations sur l’utilisation de ces outils, accédez à Utiliser les outils de [développement F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]</span><span class="sxs-lookup"><span data-stu-id="8e195-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="8e195-143">Débogage à distance et mode IE</span><span class="sxs-lookup"><span data-stu-id="8e195-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="8e195-144">Lancez Microsoft Edge \(Chromium\) avec le débogage à distance sur l’interface de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8e195-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="8e195-145">Microsoft Visual Studio, Microsoft Visual Studio Code et d’autres outils de développement exécutent généralement une commande pour lancer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8e195-145">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="8e195-146">La commande suivante lance Microsoft Edge avec le port de débogage à distance sur `9222` .</span><span class="sxs-lookup"><span data-stu-id="8e195-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="8e195-147">Après avoir lancé Microsoft Edge \(Chromium\) à l’aide d’un argument de ligne de commande, le mode IE n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="8e195-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="8e195-148">Vous pouvez toujours accéder aux sites web \(ou applications\) qui sont affichés en mode IE.</span><span class="sxs-lookup"><span data-stu-id="8e195-148">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="8e195-149">Le contenu du site web \(ou application\) est restituer à l’aide de Chromium, et non d’Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="8e195-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="8e195-150">Attendez-vous à ce que les parties des pages web qui reposent sur IE11, telles que ActiveX contrôles, ne s’restituer pas correctement.</span><span class="sxs-lookup"><span data-stu-id="8e195-150">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="8e195-151">Le badge du mode IE n’apparaît pas dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8e195-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="8e195-152">Le mode IE reste indisponible tant que vous n’avez pas complètement fermé et redémarré Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="8e195-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8e195-153">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="8e195-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Utilisation des outils de développement F12 | Documents Microsoft"  
