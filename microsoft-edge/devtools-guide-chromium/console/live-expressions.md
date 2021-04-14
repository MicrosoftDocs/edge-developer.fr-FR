---
description: Si vous vous trouvez en train de taper les mêmes expressions JavaScript dans la console à plusieurs reprises, essayez plutôt Expressions live.
title: Regardez les valeurs des expressions JavaScript en temps réel avec des expressions en direct
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483127"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a><span data-ttu-id="2adf5-104">Surveiller les modifications dans JavaScript à l'aide d'expressions live</span><span class="sxs-lookup"><span data-stu-id="2adf5-104">Monitor changes in JavaScript using Live Expressions</span></span>  

<span data-ttu-id="2adf5-105">**Les expressions live** sont un excellent moyen de surveiller les expressions JavaScript qui changent beaucoup.</span><span class="sxs-lookup"><span data-stu-id="2adf5-105">**Live Expressions** are an excellent way to monitor JavaScript expressions that change a lot.</span></span>    <span data-ttu-id="2adf5-106">Au lieu d'avoir de nombreux messages de console à lire et à naviguer, vous pouvez épingler vos expressions JavaScript spécifiques en haut de la **console.**</span><span class="sxs-lookup"><span data-stu-id="2adf5-106">Instead of having many Console messages to read and navigate, you may pin your specific JavaScript expressions to the top of the **Console**.</span></span>  

## <a name="add-a-new-live-expression"></a><span data-ttu-id="2adf5-107">Ajouter une nouvelle expression live</span><span class="sxs-lookup"><span data-stu-id="2adf5-107">Add a new live expression</span></span>  

<span data-ttu-id="2adf5-108">Pour commencer, sélectionnez le bouton Créer **une expression live** \(œil\) en regard de la **boîte** de texte Filtre.</span><span class="sxs-lookup"><span data-stu-id="2adf5-108">To start, choose the **Create live expression** \(eye\) button next to the **Filter** textbox.</span></span>  <span data-ttu-id="2adf5-109">Une fois que vous l'avez choisi, une boîte de texte s'affiche pour que vous y insérez votre nouvelle expression.</span><span class="sxs-lookup"><span data-stu-id="2adf5-109">After you choose it, a textbox is displayed for you to enter your new expression in it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Sélectionnez le bouton Nouvelle expression en direct pour ouvrir une boîte de texte pour taper une expression" lightbox="../media/console-live-expressions-new.msft.png":::
    <span data-ttu-id="2adf5-111">Choisissez le `New live expression` bouton pour ouvrir une boîte de texte pour taper une expression</span><span class="sxs-lookup"><span data-stu-id="2adf5-111">Choose the `New live expression` button to open a textbox to type an expression</span></span>  
:::image-end:::  

<span data-ttu-id="2adf5-112">**Les expressions live** peuvent être n'importe quelle expression JavaScript valide.</span><span class="sxs-lookup"><span data-stu-id="2adf5-112">**Live Expressions** may be any valid JavaScript expression.</span></span>  <span data-ttu-id="2adf5-113">Pour l'essayer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2adf5-113">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="2adf5-114">Ouvrez la **boîte de texte Expression** live.</span><span class="sxs-lookup"><span data-stu-id="2adf5-114">Open the **Live Expression** textbox.</span></span>  
1.  <span data-ttu-id="2adf5-115">Tapez `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="2adf5-115">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="2adf5-116">Pour enregistrer l'expression, effectuer l'une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2adf5-116">To save the expression, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="2adf5-117">Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2adf5-117">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    *   <span data-ttu-id="2adf5-118">Choisissez en dehors de **la boîte de texte Expression** live.</span><span class="sxs-lookup"><span data-stu-id="2adf5-118">Choose outside the **Live Expression** textbox.</span></span>  
        
<span data-ttu-id="2adf5-119">L'expression est maintenant en direct et `body` s'affiche en tant que résultat.</span><span class="sxs-lookup"><span data-stu-id="2adf5-119">The expression is now live and displays `body` as the result.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="Expression dynamique pour document.activeElement affiche le corps en tant que résultat" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    <span data-ttu-id="2adf5-121">Expression live pour `document.activeElement` afficher le corps en tant que résultat</span><span class="sxs-lookup"><span data-stu-id="2adf5-121">Live expression for `document.activeElement` displays body as the result</span></span>  
:::image-end:::  

<span data-ttu-id="2adf5-122">Si vous naviguez dans la page web, la valeur change.</span><span class="sxs-lookup"><span data-stu-id="2adf5-122">If you navigate around the webpage, the value changes.</span></span>  <span data-ttu-id="2adf5-123">Par exemple, dans la figure suivante, vous ouvrez le menu de recherche dans la page web et l'expression s'affiche maintenant `button.nav-bar-button.focus-visible` en tant que valeur.</span><span class="sxs-lookup"><span data-stu-id="2adf5-123">For example, in the following figure you open the search menu in the webpage and the expression now displays `button.nav-bar-button.focus-visible` as the value.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Pour modifier la valeur de l'expression live, interagissez avec différents éléments sur la page web" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    <span data-ttu-id="2adf5-125">Pour modifier la valeur de **l'expression live,** interagissez avec différents éléments sur la page web</span><span class="sxs-lookup"><span data-stu-id="2adf5-125">To change the value of the **Live Expression**, interact with different elements on the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="2adf5-126">Pour modifier à nouveau la valeur, ouvrez et choisissez la zone de texte Rechercher sur la page web.</span><span class="sxs-lookup"><span data-stu-id="2adf5-126">To change the value again, open and choose the Search textbox on the webpage.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Accédez à un autre élément dans la page web pour mettre à jour l'expression live" lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    <span data-ttu-id="2adf5-128">Accédez à un autre élément dans la page web pour mettre à jour **l'expression live**</span><span class="sxs-lookup"><span data-stu-id="2adf5-128">Navigate to a different element in the webpage to update the **Live Expression**</span></span>  
:::image-end:::  

## <a name="remove-live-expressions"></a><span data-ttu-id="2adf5-129">Supprimer des expressions live</span><span class="sxs-lookup"><span data-stu-id="2adf5-129">Remove Live Expressions</span></span>  

<span data-ttu-id="2adf5-130">Une **expression dynamique** est disponible tant que vous la conservez active.</span><span class="sxs-lookup"><span data-stu-id="2adf5-130">A **Live Expression** is available as long as you keep it active.</span></span>  <span data-ttu-id="2adf5-131">Pour vous débarrasser d'une **expression live,** choisissez la `x` suivante.</span><span class="sxs-lookup"><span data-stu-id="2adf5-131">To get rid of a **Live Expression**, choose the `x` next to it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Pour supprimer des expressions en direct, choisissez le x à côté de celui-ci" lightbox="../media/console-live-expressions-remove.msft.png":::
    <span data-ttu-id="2adf5-133">Pour supprimer **des expressions live,** choisissez le `x` suivant</span><span class="sxs-lookup"><span data-stu-id="2adf5-133">To remove **Live Expressions**, choose the `x` next to it</span></span>  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a><span data-ttu-id="2adf5-134">Remplacer la journalisation de la console par des expressions en direct</span><span class="sxs-lookup"><span data-stu-id="2adf5-134">Replace Console logging with Live Expressions</span></span>  

<span data-ttu-id="2adf5-135">Vous pouvez créer autant d'expressions que vous le souhaitez et les faire persister entre les sessions de navigateur et les fenêtres.</span><span class="sxs-lookup"><span data-stu-id="2adf5-135">You may create as many expressions as you want and persist each across browser sessions and windows.</span></span>  <span data-ttu-id="2adf5-136">**Les expressions live** sont un moyen de réduire le bruit dans votre flux de travail de débogage.</span><span class="sxs-lookup"><span data-stu-id="2adf5-136">**Live Expressions** are a way to cut down on noise in your debugging workflow.</span></span>  

<span data-ttu-id="2adf5-137">Par exemple, vous souhaitez surveiller le mouvement de la souris dans la page web actuelle.</span><span class="sxs-lookup"><span data-stu-id="2adf5-137">For example, you want to monitor the mouse movement in the current webpage.</span></span>  <span data-ttu-id="2adf5-138">Accédez à [la démonstration de journalisation][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]du mouvement de la souris, ouvrez la **console**et déplacez votre souris pour afficher les journaux avec un grand nombre d'informations.</span><span class="sxs-lookup"><span data-stu-id="2adf5-138">Navigate to [Logging Mouse Movement demo][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml], open the **Console**, and move your mouse around to display the logs with a lot of information.</span></span>  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="La console affiche beaucoup d'informations sur la position de la souris" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    <span data-ttu-id="2adf5-140">**La console** affiche beaucoup d'informations sur la position de la souris</span><span class="sxs-lookup"><span data-stu-id="2adf5-140">**Console** displays much information on mouse position</span></span>  
:::image-end:::  

<span data-ttu-id="2adf5-141">La grande quantité d'informations ralentit non seulement votre processus de débogage, mais facilite également l'accès aux modifications que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="2adf5-141">The large amount of information not only slows your debug process, but also makes it easy to miss the changes you want to review.</span></span>  <span data-ttu-id="2adf5-142">À mesure **que la console** affiche davantage de messages et que vous déplacez votre souris, les valeurs que vous souhaitez consulter défilent hors de l'écran.</span><span class="sxs-lookup"><span data-stu-id="2adf5-142">As the **Console** displays more messages and you move your mouse, the values you want to review scroll off the screen.</span></span>  

<span data-ttu-id="2adf5-143">Pour essayer **les expressions live comme** alternative, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2adf5-143">To try **Live Expressions** as an alternative, complete the following actions.</span></span>  

1.  <span data-ttu-id="2adf5-144">Accédez au mouvement [de souris sans démonstration de journalisation.][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]</span><span class="sxs-lookup"><span data-stu-id="2adf5-144">Navigate to the [Mouse movement without logging demo][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].</span></span>  
1.  <span data-ttu-id="2adf5-145">Créer **des expressions en direct** pour et `x` `y` .</span><span class="sxs-lookup"><span data-stu-id="2adf5-145">Create **Live Expressions** for `x` and `y`.</span></span>  
    
<span data-ttu-id="2adf5-146">Lorsque vous utilisez **des expressions**live, vous obtenez toujours les informations sur la même partie de votre écran et conservez les journaux de la **console** pour les valeurs qui ne changent pas autant.</span><span class="sxs-lookup"><span data-stu-id="2adf5-146">When you use **Live Expressions**, you always get the information on the same part of your screen and keep **Console** logs for values that don't change as much.</span></span>

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Afficher la position x et y de la souris en tant qu'expressions en direct" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    <span data-ttu-id="2adf5-148">Affichage de `x` la souris et de sa position en tant `y` **qu'expressions en direct**</span><span class="sxs-lookup"><span data-stu-id="2adf5-148">Display the `x` and `y` position of the mouse as **Live Expressions**</span></span>  
:::image-end:::  

<span data-ttu-id="2adf5-149">**Les expressions live** s'exécutent exclusivement sur votre ordinateur et vous n'avez rien à modifier dans votre code pour l'afficher.</span><span class="sxs-lookup"><span data-stu-id="2adf5-149">**Live Expressions** run exclusively on your computer and you don't need to change anything in your code to display.</span></span>  <span data-ttu-id="2adf5-150">**Les expressions live** sont un excellent moyen de vous assurer que vous affichez uniquement les informations que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="2adf5-150">**Live Expressions** are a great way to ensure that you only display the information you want to debug.</span></span>  <span data-ttu-id="2adf5-151">En outre, **les expressions live** vous aident à limiter le bruit sur les ordinateurs de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2adf5-151">Also, **Live Expressions** help you limit the noise on your users' computers.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2adf5-152">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2adf5-152">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Exemples de messages de console : utilisation du tableau | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Mouvement de la souris sans journalisation | GitHub"  
