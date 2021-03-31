---
description: Avec les outils de développement F12, découvrez comment déboguer le script d’arrière-plan, les scripts de contenu et les pages d’extension d’une extension.
title: Débogage | Extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, javascript, développeur, débogage, débogage
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399364"
---
# <a name="debugging-extensions"></a><span data-ttu-id="c2180-104">Extensions de débogage</span><span class="sxs-lookup"><span data-stu-id="c2180-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="c2180-105">Vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide des outils de développement F12.</span><span class="sxs-lookup"><span data-stu-id="c2180-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>  

<span data-ttu-id="c2180-106">La vidéo suivante montre une extension Microsoft Edge difficile, en parant chaque scénario de débogage et en le corrigeant tout au long du chemin.</span><span class="sxs-lookup"><span data-stu-id="c2180-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span>  <span data-ttu-id="c2180-107">Pour plus d’informations, voir les instructions détaillées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c2180-107">See the step-by-step instructions below for more info.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> <span data-ttu-id="c2180-108">Pour tirer parti du débogage des extensions avec F12, vous devez d’abord activer les fonctionnalités de développement dans about:flags.</span><span class="sxs-lookup"><span data-stu-id="c2180-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span>  <span data-ttu-id="c2180-109">Voir [Ajout et suppression d’extensions](./adding-and-removing-extensions.md) pour plus d’informations sur la façon de le faire.</span><span class="sxs-lookup"><span data-stu-id="c2180-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>  

## <a name="background-script-debugging"></a><span data-ttu-id="c2180-110">Débogage de script en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="c2180-110">Background script debugging</span></span>  

<span data-ttu-id="c2180-111">Pour commencer à déboguer le script en arrière-plan de votre extension :</span><span class="sxs-lookup"><span data-stu-id="c2180-111">To start debugging the background script of your extension:</span></span>  

1.  <span data-ttu-id="c2180-112">Cliquez sur **Plus (...)** suivi **des extensions** pour aller dans le volet d’extensions.</span><span class="sxs-lookup"><span data-stu-id="c2180-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
    
    ![Bouton plus](../media/morebutton.png)  
    
1.  <span data-ttu-id="c2180-114">Cliquez sur l’extension à déboguer.</span><span class="sxs-lookup"><span data-stu-id="c2180-114">Click on the extension that you want to debug.</span></span>  
1.  <span data-ttu-id="c2180-115">Cliquez sur le lien de la page d’arrière-plan pour faire monter la F12 pour le processus en arrière-plan. </span><span class="sxs-lookup"><span data-stu-id="c2180-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
    
    ![vue d’extension sélectionnée des options avec le lien Inspecter](../media/debug-inspect.png)  
    
1.  <span data-ttu-id="c2180-117">Sélectionnez **l’onglet Débogger** dans F12.</span><span class="sxs-lookup"><span data-stu-id="c2180-117">Select the **Debugger** tab in F12.</span></span>  
1.  <span data-ttu-id="c2180-118">Accédez au script en arrière-plan de votre extension et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="c2180-118">Navigate to and select your extension's background script.</span></span>  
1.  <span data-ttu-id="c2180-119">Placez les points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.</span><span class="sxs-lookup"><span data-stu-id="c2180-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![Console f12 affichant un script en arrière-plan avec des points d’coupure](../media/debug-f12-background.png)  
    
1.  <span data-ttu-id="c2180-121">Sélectionnez **l’onglet Console** et exécutez la `location.reload()` commande.</span><span class="sxs-lookup"><span data-stu-id="c2180-121">Select the **Console** tab and execute the `location.reload()` command.</span></span>  <span data-ttu-id="c2180-122">Cela réexécute le script en arrière-plan, ce qui vous permet d’exécuter pas à pas votre code.</span><span class="sxs-lookup"><span data-stu-id="c2180-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
    
    ![console avec location.reload entrée](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a><span data-ttu-id="c2180-124">Débogage de script de contenu</span><span class="sxs-lookup"><span data-stu-id="c2180-124">Content script debugging</span></span>  

<span data-ttu-id="c2180-125">Pour commencer à déboguer le script de contenu de votre extension :</span><span class="sxs-lookup"><span data-stu-id="c2180-125">To start debugging the content script of your extension:</span></span>  

1.  <span data-ttu-id="c2180-126">Lancez F12 en naviguant vers le bouton **Plus (...)** et en sélectionnant Outils de **développement F12** ou en appuyant `F12` sur votre clavier.</span><span class="sxs-lookup"><span data-stu-id="c2180-126">Launch F12 by either navigating to the **More (...)** button and selecting **F12 Developer Tools** or by pressing `F12` on your keyboard.</span></span>  
1.  <span data-ttu-id="c2180-127">Accédez au script de contenu de votre extension et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="c2180-127">Navigate to and select your extension's content script.</span></span>  <span data-ttu-id="c2180-128">Les scripts de contenu pour les extensions en cours d’exécution sont représentés par un dossier différent pour chaque extension.</span><span class="sxs-lookup"><span data-stu-id="c2180-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c2180-129">Seuls les scripts de contenu en cours d’exécution s’affichent.</span><span class="sxs-lookup"><span data-stu-id="c2180-129">Only running content scripts will appear.</span></span>  
    
1.  <span data-ttu-id="c2180-130">Placez les points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.</span><span class="sxs-lookup"><span data-stu-id="c2180-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![f12 avec le script de contenu déboyé](../media/debug-content-f12.png)  
    
1.  <span data-ttu-id="c2180-132">Actualisez l’onglet du navigateur pour commencer pas à pas dans votre code.</span><span class="sxs-lookup"><span data-stu-id="c2180-132">Refresh the browser tab to begin stepping though your code.</span></span>  
    
## <a name="extension-page-debugging"></a><span data-ttu-id="c2180-133">Débogage de page d’extension</span><span class="sxs-lookup"><span data-stu-id="c2180-133">Extension page debugging</span></span>  

<span data-ttu-id="c2180-134">Deux méthodes peuvent être utilisées pour accéder au code source de votre page d’extension pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="c2180-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span>  <span data-ttu-id="c2180-135">Une méthode s’applique à une variété de pages, tandis que l’autre fonctionne uniquement pour les pages popup.</span><span class="sxs-lookup"><span data-stu-id="c2180-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>  

### <a name="debugging-any-extension-page"></a><span data-ttu-id="c2180-136">Débogage d’une page d’extension</span><span class="sxs-lookup"><span data-stu-id="c2180-136">Debugging any extension page</span></span>  

<span data-ttu-id="c2180-137">La méthode suivante fonctionne pour toutes les pages d’extension, telles que la page d’options et les fenêtres popup :</span><span class="sxs-lookup"><span data-stu-id="c2180-137">The following method works for all extension pages like the options page and popups:</span></span>  

1.  <span data-ttu-id="c2180-138">Cliquez avec le bouton droit sur l’arrière-plan de votre page.</span><span class="sxs-lookup"><span data-stu-id="c2180-138">Right-click on the background of your page.</span></span>  
1.  <span data-ttu-id="c2180-139">Sélectionnez **Afficher la source.**</span><span class="sxs-lookup"><span data-stu-id="c2180-139">Select **View source**.</span></span>  
    
    ![Ouvrir le débogage de fenêtres popup avec f12](../media/debug-popup-select.png)  
    
1.  <span data-ttu-id="c2180-141">Une fois la F12 ouverte, placez les points d’arrêt dans le fichier que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="c2180-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>  
    
    ![débogage popup avec f12](../media/debug-popup-f12.png)  
    
1.  <span data-ttu-id="c2180-143">Sélectionnez **l’onglet Console** et exécutez la `location.reload()` commande.</span><span class="sxs-lookup"><span data-stu-id="c2180-143">Select the **Console** tab and execute the command `location.reload()`.</span></span>  <span data-ttu-id="c2180-144">Cela réexécute le script de page, ce qui vous permet d’exécuter pas à pas votre code.</span><span class="sxs-lookup"><span data-stu-id="c2180-144">This will re-execute the page script, allowing you to step through your code.</span></span>  
    
    ![console avec location.reload entrée](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a><span data-ttu-id="c2180-146">Débogage d’une page d’extension popup</span><span class="sxs-lookup"><span data-stu-id="c2180-146">Debugging a popup extension page</span></span>  

<span data-ttu-id="c2180-147">Bien que la méthode de débogage des pages d’extension s’applique également aux pages d’extension de fenêtre popup, les étapes suivantes décrivent une autre façon de déboguer votre fenêtre popup :</span><span class="sxs-lookup"><span data-stu-id="c2180-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>  

1.  <span data-ttu-id="c2180-148">Cliquez avec le bouton droit sur l’icône de votre extension.</span><span class="sxs-lookup"><span data-stu-id="c2180-148">Right-click your extension's icon.</span></span>  
1.  <span data-ttu-id="c2180-149">Sélectionnez **Inspecter la fenêtre pop-up**.</span><span class="sxs-lookup"><span data-stu-id="c2180-149">Select **Inspect popup**.</span></span>  
    
    ![inspection du débogage popup](../media/debug-popup-inspect.png)  
    
1.  <span data-ttu-id="c2180-151">Suivez les étapes 3 et 4 ci-dessus pour placer des points d’arrêt et recharger la fenêtre popup.</span><span class="sxs-lookup"><span data-stu-id="c2180-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>  
    