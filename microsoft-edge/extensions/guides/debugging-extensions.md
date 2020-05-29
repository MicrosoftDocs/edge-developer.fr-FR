---
description: Avec les outils de développement F12, Découvrez comment déboguer le script en arrière-plan, les scripts de contenu et les pages d’extension d’une extension.
title: Extensions-débogage
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, JavaScript, développeur, débogage et débogage
ms.custom: seodec18
ms.openlocfilehash: 34488870cb4e4a92a9d57859509ce7d1176cf284
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565368"
---
# <span data-ttu-id="385a3-104">Extensions de débogage</span><span class="sxs-lookup"><span data-stu-id="385a3-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="385a3-105">Vous pouvez déboguer vos extensions dans Microsoft Edge à l’aide des outils de développement F12.</span><span class="sxs-lookup"><span data-stu-id="385a3-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>

<span data-ttu-id="385a3-106">La vidéo suivante présente une extension Microsoft Edge de Microsoft, en passant par chaque scénario de débogage et en le fixant.</span><span class="sxs-lookup"><span data-stu-id="385a3-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span> <span data-ttu-id="385a3-107">Pour plus d’informations, consultez les instructions pas à pas ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="385a3-107">See the step-by-step instructions below for more info.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> <span data-ttu-id="385a3-108">Pour tirer parti du débogage par extension avec la fonction F12, vous devez d’abord activer les fonctionnalités de développement dans à propos de: indicateurs.</span><span class="sxs-lookup"><span data-stu-id="385a3-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span> <span data-ttu-id="385a3-109">Pour plus d’informations sur la façon de procéder [, voir Ajout et suppression d’extensions](./adding-and-removing-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="385a3-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>


## <span data-ttu-id="385a3-110">Débogage de script en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="385a3-110">Background script debugging</span></span>
<span data-ttu-id="385a3-111">Pour démarrer le débogage du script en arrière-plan de votre extension:</span><span class="sxs-lookup"><span data-stu-id="385a3-111">To start debugging the background script of your extension:</span></span>

1. <span data-ttu-id="385a3-112">Cliquez sur **plus (...),** puis sur **Extensions** pour accéder au volet extension.</span><span class="sxs-lookup"><span data-stu-id="385a3-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
 ![bouton plus](./../media/morebutton.png)
2. <span data-ttu-id="385a3-114">Cliquez sur l’extension que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="385a3-114">Click on the extension that you want to debug.</span></span>
3. <span data-ttu-id="385a3-115">Cliquez sur le lien de la **page d’arrière-plan** pour afficher la touche F12 du processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="385a3-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
 ![affichage extensions sélectionnés des options avec le lien inspecter](./../media/debug-inspect.png)
4. <span data-ttu-id="385a3-117">Sélectionnez l’onglet **débogueur** dans F12.</span><span class="sxs-lookup"><span data-stu-id="385a3-117">Select the **Debugger** tab in F12.</span></span>
5. <span data-ttu-id="385a3-118">Naviguez jusqu’au script en arrière-plan de votre extension et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="385a3-118">Navigate to and select your extension's background script.</span></span>
6. <span data-ttu-id="385a3-119">Placez des points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.</span><span class="sxs-lookup"><span data-stu-id="385a3-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![Console F12 montrant le script en arrière-plan avec des points d’arrêt](./../media/debug-f12-background.png)
7. <span data-ttu-id="385a3-121">Sélectionnez l’onglet **console** et exécutez la commande « `location.reload()` ».</span><span class="sxs-lookup"><span data-stu-id="385a3-121">Select the **Console** tab and execute the command "`location.reload()`".</span></span> <span data-ttu-id="385a3-122">Cette opération permet de réexécuter le script en arrière-plan, ce qui vous permet de parcourir votre code.</span><span class="sxs-lookup"><span data-stu-id="385a3-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
 ![console avec emplacement. recharger entré](./../media/debug-f12-background-console.png)


## <span data-ttu-id="385a3-124">Débogage de script de contenu</span><span class="sxs-lookup"><span data-stu-id="385a3-124">Content script debugging</span></span>
<span data-ttu-id="385a3-125">Pour démarrer le débogage du script de contenu de votre extension:</span><span class="sxs-lookup"><span data-stu-id="385a3-125">To start debugging the content script of your extension:</span></span>

1. <span data-ttu-id="385a3-126">Lancez la version F12 en accédant au bouton **autres (...)** et en sélectionnant **«F12 outils de développement»** ou en appuyant sur la touche F12 de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="385a3-126">Launch F12 by either navigating to the **More (...)** button and selecting **"F12 Developer Tools"** or by pressing F12 on your keyboard.</span></span>
2. <span data-ttu-id="385a3-127">Recherchez et sélectionnez le script de contenu de votre extension.</span><span class="sxs-lookup"><span data-stu-id="385a3-127">Navigate to and select your extension's content script.</span></span> <span data-ttu-id="385a3-128">Les scripts de contenu pour les extensions actuellement en cours d’exécution seront représentés par un dossier différent pour chaque extension.</span><span class="sxs-lookup"><span data-stu-id="385a3-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>

    > [!NOTE]
    > <span data-ttu-id="385a3-129">Seuls les scripts de contenu doivent s’afficher.</span><span class="sxs-lookup"><span data-stu-id="385a3-129">Only running content scripts will appear.</span></span>

3. <span data-ttu-id="385a3-130">Placez des points d’arrêt pour le débogage en cliquant à gauche du numéro de ligne de code source.</span><span class="sxs-lookup"><span data-stu-id="385a3-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![F12 avec le débogage de script de contenu](./../media/debug-content-f12.png)
4. <span data-ttu-id="385a3-132">Actualisez l’onglet du navigateur pour commencer à exécuter votre code.</span><span class="sxs-lookup"><span data-stu-id="385a3-132">Refresh the browser tab to begin stepping though your code.</span></span>




## <span data-ttu-id="385a3-133">Débogage de page d’extension</span><span class="sxs-lookup"><span data-stu-id="385a3-133">Extension page debugging</span></span>

<span data-ttu-id="385a3-134">Il existe deux méthodes qui peuvent être utilisées pour accéder au code source de la page de votre extension pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="385a3-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span> <span data-ttu-id="385a3-135">Une méthode s’applique à un large éventail de pages tandis que l’autre fonctionne uniquement pour les pages contextuelles.</span><span class="sxs-lookup"><span data-stu-id="385a3-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>

### <span data-ttu-id="385a3-136">Débogage de n’importe quelle page d’extension</span><span class="sxs-lookup"><span data-stu-id="385a3-136">Debugging any extension page</span></span>
<span data-ttu-id="385a3-137">La méthode suivante fonctionne pour toutes les pages d’extension, comme la page d’options et les fenêtres contextuelles:</span><span class="sxs-lookup"><span data-stu-id="385a3-137">The following method works for all extension pages like the options page and popups:</span></span>


1. <span data-ttu-id="385a3-138">Cliquez avec le bouton droit sur l’arrière-plan de votre page.</span><span class="sxs-lookup"><span data-stu-id="385a3-138">Right-click on the background of your page.</span></span>
2. <span data-ttu-id="385a3-139">Sélectionnez **«afficher la source»**.</span><span class="sxs-lookup"><span data-stu-id="385a3-139">Select **"View source"**.</span></span>

   ![débogage contextuelle avec F12](./../media/debug-popup-select.png)

3. <span data-ttu-id="385a3-141">Lorsque F12 s’ouvre, placez les points d’arrêt dans le fichier que vous voulez déboguer.</span><span class="sxs-lookup"><span data-stu-id="385a3-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>

   ![débogage contextuelle avec F12](./../media/debug-popup-f12.png)
4. <span data-ttu-id="385a3-143">Sélectionnez l’onglet **console** et exécutez la commande `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="385a3-143">Select the **Console** tab and execute the command `location.reload()`.</span></span> <span data-ttu-id="385a3-144">Cette opération permet de réexécuter le script de page, ce qui vous permet de parcourir votre code.</span><span class="sxs-lookup"><span data-stu-id="385a3-144">This will re-execute the page script, allowing you to step through your code.</span></span>  

   ![console avec emplacement. recharger entré](./../media/debug-f12-background-console.png)

### <span data-ttu-id="385a3-146">Débogage d’une page d’extension contextuelle</span><span class="sxs-lookup"><span data-stu-id="385a3-146">Debugging a popup extension page</span></span>
<span data-ttu-id="385a3-147">Bien que la méthode utilisée pour déboguer les pages d’extension s’applique également aux pages d’extension contextuelle, les étapes suivantes décrivent une autre méthode de débogage de votre fenêtre contextuelle:</span><span class="sxs-lookup"><span data-stu-id="385a3-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>

1. <span data-ttu-id="385a3-148">Cliquez avec le bouton droit sur l’icône de votre extension.</span><span class="sxs-lookup"><span data-stu-id="385a3-148">Right-click your extension's icon.</span></span>
2. <span data-ttu-id="385a3-149">Sélectionnez **«Inspect Popup»**.</span><span class="sxs-lookup"><span data-stu-id="385a3-149">Select **"Inspect popup"**.</span></span>

   ![inspection de débogage contextuelle](./../media/debug-popup-inspect.png)
3. <span data-ttu-id="385a3-151">Suivez les étapes 3 et 4 ci-dessus pour placer des points d’arrêt et recharger la fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="385a3-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>
