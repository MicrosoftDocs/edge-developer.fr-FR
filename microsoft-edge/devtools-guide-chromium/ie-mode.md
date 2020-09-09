---
description: Mode IE et Microsoft Edge (chrome) DevTools
title: Le mode Internet Explorer et le DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, ie11, Internet Explorer 11, mode IE
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003963"
---
# <span data-ttu-id="3be43-104">Le mode Internet Explorer et le DevTools</span><span class="sxs-lookup"><span data-stu-id="3be43-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="3be43-105">Cet article décrit comment le mode d’affichage d’Internet Explorer \ (mode IE \) est intégré à Microsoft Edge \ (chrome \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3be43-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <span data-ttu-id="3be43-106">Présentation du mode IE</span><span class="sxs-lookup"><span data-stu-id="3be43-106">Understanding IE mode</span></span>  

<span data-ttu-id="3be43-107">Le mode IE permet aux entreprises de spécifier une liste de sites Web qui fonctionnent uniquement dans Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="3be43-108">Lorsque vous accédez à ces sites Web dans Microsoft Edge \ (chrome \), une instance d’Internet Explorer 11 s’exécute et affiche le site dans un onglet.  Cette fonctionnalité permet aux entreprises de gérer la compatibilité avec des technologies qui ne sont actuellement pas compatibles avec les navigateurs Web modernes.</span><span class="sxs-lookup"><span data-stu-id="3be43-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="3be43-109">La prise en charge des technologies suivantes est incluse dans le mode IE.</span><span class="sxs-lookup"><span data-stu-id="3be43-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="3be43-110">Modes de document IE</span><span class="sxs-lookup"><span data-stu-id="3be43-110">IE document modes</span></span>  
*   <span data-ttu-id="3be43-111">contrôles ActiveX;</span><span class="sxs-lookup"><span data-stu-id="3be43-111">ActiveX controls</span></span>  
*   <span data-ttu-id="3be43-112">autres composants hérités</span><span class="sxs-lookup"><span data-stu-id="3be43-112">other legacy components</span></span>  

<span data-ttu-id="3be43-113">Dans le mode IE, le processus de rendu est basé sur Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="3be43-114">Le gestionnaire de processus Microsoft Edge \ (chrome \) gère la durée de vie du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="3be43-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="3be43-115">Il est limité à la durée de vie de l’onglet pour un site (ou une application) spécifique.</span><span class="sxs-lookup"><span data-stu-id="3be43-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="3be43-116">Lorsqu’un onglet est restitué dans le mode IE, un badge s’affiche dans la barre d’adresses de l’onglet spécifique.</span><span class="sxs-lookup"><span data-stu-id="3be43-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="Badge du mode IE dans la barre d’adresses" lightbox="./media/ie-mode-badge.msft.png":::
   <span data-ttu-id="3be43-118">Badge du mode IE dans la barre d’adresses</span><span class="sxs-lookup"><span data-stu-id="3be43-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="3be43-119">Le mode IE est actuellement disponible sur Windows 10 version 1903 \ (2019 mise à jour \), mais bientôt disponible sur toutes les plateformes Windows prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3be43-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <span data-ttu-id="3be43-120">Lancement de DevTools sur un onglet du mode IE</span><span class="sxs-lookup"><span data-stu-id="3be43-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="3be43-121">Si vous essayez d’afficher le mode document d’un site Web dans le mode IE, sélectionnez le badge dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3be43-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Afficher le mode document à l’aide du badge du mode IE" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="3be43-123">Afficher le mode document à l’aide du badge du mode IE</span><span class="sxs-lookup"><span data-stu-id="3be43-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="3be43-124">Si un onglet utilise le mode IE, le DevTools ne fonctionne pas et les conditions suivantes se produisent.</span><span class="sxs-lookup"><span data-stu-id="3be43-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="3be43-125">Si vous sélectionnez `F12` ou sélectionnez `Ctrl` + `Shift` + `I` , une instance vide de Microsoft Edge \ (chrome \) devtools est lancée, le message suivant s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3be43-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="3be43-126">Si vous ouvrez un menu contextuel \ (cliquez avec le bouton droit sur \) et sélectionnez **afficher la source**, le bloc-notes est lancé.</span><span class="sxs-lookup"><span data-stu-id="3be43-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="3be43-127">Si vous ouvrez un menu contextuel \ (cliquez avec le bouton droit sur \), l' **élément Inspect** n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="3be43-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="3be43-128">La raison pour laquelle un certain nombre d’outils à l’intérieur du DevTools \ (comme les outils **réseau** et de **performance** \) ne fonctionne pas, c’est le moteur de rendu qui bascule du chrome vers Internet Explorer 11 en mode IE.</span><span class="sxs-lookup"><span data-stu-id="3be43-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="3be43-129">Pour fournir des commentaires, accédez à [l’équipe Microsoft Edge devtools](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="3be43-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="DevTools lancée en mode IE" lightbox="./media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="3be43-131">DevTools lancée en mode IE</span><span class="sxs-lookup"><span data-stu-id="3be43-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="3be43-132">Pour tester votre site Web Internet Explorer 11 (ou l’application \) en mode Internet Explorer 11 et IE, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3be43-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="3be43-133">Ouvrez Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="3be43-134">Sur Windows 10, recherchez le raccourci vers Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="3be43-135">**Menu Démarrer**  >  **Accessoires Windows**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="3be43-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="3be43-136">Sur Windows 7, recherchez Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="3be43-137">**Menu Démarrer**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="3be43-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="3be43-138">Ouvrez la même page Web dans Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="3be43-139">Lancez Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="3be43-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="3be43-140">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="3be43-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="3be43-141">Positionnez le curseur n’importe où, ouvrez un menu contextuel, puis sélectionnez **inspecter l’élément**.</span><span class="sxs-lookup"><span data-stu-id="3be43-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="3be43-142">Pour plus d’informations sur l’utilisation de ces outils, accédez à l' [utilisation des outils de développement F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="3be43-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <span data-ttu-id="3be43-143">Débogage à distance et mode IE</span><span class="sxs-lookup"><span data-stu-id="3be43-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="3be43-144">Pour lancer le débogage à distance à partir de l’interface de ligne de commande, lancez Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="3be43-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="3be43-145">Dans Visual Studio, le code Visual Studio et d’autres outils de développement, vous pouvez généralement exécuter une commande pour lancer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3be43-145">Visual Studio, Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="3be43-146">La commande suivante lance Microsoft Edge avec le port de débogage distant défini sur `9222` .</span><span class="sxs-lookup"><span data-stu-id="3be43-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="3be43-147">Après avoir lancé Microsoft Edge \ (chrome \) à l’aide d’un argument de ligne de commande, le mode IE n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="3be43-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="3be43-148">Il est possible que vous deviez accéder à des sites Web \ (ou applications \) qui s’affichaient normalement dans le mode IE.</span><span class="sxs-lookup"><span data-stu-id="3be43-148">You may still navigate to websites \(or apps\) that would otherwise display in IE mode.</span></span> <span data-ttu-id="3be43-149">Le contenu du site Web (ou de l’application \) est restitué à l’aide de chrome, et non d’Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="3be43-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="3be43-150">Attendez-vous à ce que les parties des pages qui s’appuient sur IE11, comme les contrôles ActiveX, ne s’affichent pas correctement.</span><span class="sxs-lookup"><span data-stu-id="3be43-150">Expect the parts of the pages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="3be43-151">Le badge du mode IE n’apparaît pas dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3be43-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="3be43-152">Le mode IE reste indisponible tant que vous n’avez pas complètement fermé et redémarré Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="3be43-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="3be43-153">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="3be43-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Utiliser les outils de développement F12 | Documents Microsoft"  