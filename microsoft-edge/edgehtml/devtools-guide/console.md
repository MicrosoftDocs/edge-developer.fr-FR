---
description: Utilisez l’outil console pour le débogage interactif et les tests ad hoc.
title: DevTools-console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472aafa9e6c6fd98ea952804f0e92ed0b774f59c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233060"
---
# <span data-ttu-id="1518d-104">Console</span><span class="sxs-lookup"><span data-stu-id="1518d-104">Console</span></span>

<span data-ttu-id="1518d-105">L’outil de développement de console dans Microsoft Edge enregistre les informations associées à une page Web (par exemple, JavaScript, requêtes réseau et erreurs de sécurité).</span><span class="sxs-lookup"><span data-stu-id="1518d-105">The Console developer tool in Microsoft Edge logs information that's associated with a webpage, such as JavaScript, network requests, and security errors.</span></span> <span data-ttu-id="1518d-106">Vous pouvez utiliser la console pour le débogage interactif et les tests ad hoc.</span><span class="sxs-lookup"><span data-stu-id="1518d-106">You can use the Console for interactive debugging and ad hoc testing.</span></span> 

<span data-ttu-id="1518d-107">Pour ouvrir l’outil console dans Microsoft Edge, appuyez sur la touche F12 pour accéder à la fenêtre de l’outil de développement (ou cliquez avec le bouton droit sur la page, puis sélectionnez **inspecter l’élément**).</span><span class="sxs-lookup"><span data-stu-id="1518d-107">To open the Console tool in Microsoft Edge, press the F12 key to access the developer tool window (or right-click on the page, and then select **Inspect Element**).</span></span> <span data-ttu-id="1518d-108">Ensuite, sélectionnez l’onglet de la **console** en haut de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1518d-108">Then, select the **Console** tab at the top of the window.</span></span> 

<span data-ttu-id="1518d-109">Vous pouvez également utiliser l’outil console pour communiquer avec une page Web en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1518d-109">You can also use the Console tool to communicate to and from a running webpage.</span></span> <span data-ttu-id="1518d-110">Vous pouvez utiliser la console pour:</span><span class="sxs-lookup"><span data-stu-id="1518d-110">You can use the Console to:</span></span>

- <span data-ttu-id="1518d-111">Publiez des [codes d’erreur](./console/error-and-status-codes.md) et de statut standard et des messages d’information lors de l’exécution de votre code.</span><span class="sxs-lookup"><span data-stu-id="1518d-111">Post standard [error and status codes](./console/error-and-status-codes.md) and informational messages as your code runs.</span></span>
- <span data-ttu-id="1518d-112">Générez des journaux de débogage personnalisés à partir des appels d' [API de console](./console/console-api.md) que vous incluez dans votre code.</span><span class="sxs-lookup"><span data-stu-id="1518d-112">Generate custom debug logs from the [Console API](./console/console-api.md) calls you include in your code.</span></span>
- <span data-ttu-id="1518d-113">Fournissez un affichage [ligne de commande](./console/command-line.md) et arborescence interactive pour inspecter les valeurs de retour actuelles des variables et fonctions clés.</span><span class="sxs-lookup"><span data-stu-id="1518d-113">Provide a [command line](./console/command-line.md) and interactive tree view for inspecting current return values of key variables and functions.</span></span>

## <span data-ttu-id="1518d-114">Éléments de la console</span><span class="sxs-lookup"><span data-stu-id="1518d-114">Parts of the Console</span></span>

<span data-ttu-id="1518d-115">L’image ci-après illustre les principales composantes de la console:</span><span class="sxs-lookup"><span data-stu-id="1518d-115">The following image shows the key parts of the Console:</span></span>

![Console Microsoft Edge DevTools](./media/console.png)

1. <span data-ttu-id="1518d-117">**Erreurs**  /  **Avertissements**  /  **Infos**  /  Boutons **journaux** : filtrez la sortie de la console par le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="1518d-117">**Errors** / **Warnings** / **Info** / **Logs** buttons: Filter console output by the specified type.</span></span> <span data-ttu-id="1518d-118">Vous pouvez sélectionner plusieurs boutons en maintenant la touche **CTRL** enfoncée.</span><span class="sxs-lookup"><span data-stu-id="1518d-118">You can multi-select buttons by holding down the **Ctrl** key.</span></span> <span data-ttu-id="1518d-119">Le bouton **tout** annule tous les filtres.</span><span class="sxs-lookup"><span data-stu-id="1518d-119">The **All** button clears all filters.</span></span>

2. <span data-ttu-id="1518d-120">Bouton **Effacer** (**Ctrl + L**): le bouton **Effacer** efface l’affichage actuel de la console.</span><span class="sxs-lookup"><span data-stu-id="1518d-120">**Clear** button (**Ctrl+L**): The **Clear** button clears the current console display.</span></span>

3. <span data-ttu-id="1518d-121">Case à cocher **conserver le journal** : activez la case à cocher **conserver le journal** pour conserver la sortie de votre console sur toutes les mises à jour de la page, puis fermez et rouvrez devtools.</span><span class="sxs-lookup"><span data-stu-id="1518d-121">**Preserve Log** check box: Selecting the **Preserve Log** check box persists your console output across page refreshes and closing and reopening DevTools.</span></span> <span data-ttu-id="1518d-122">L’historique de la console ne s’efface que lorsque vous fermez l’onglet ou vous effacez manuellement la console.</span><span class="sxs-lookup"><span data-stu-id="1518d-122">The Console history clears only when the tab is closed or you manually clear the Console.</span></span>

4. <span data-ttu-id="1518d-123">**Target**: utilisez le menu déroulant **target** pour basculer vers un autre contexte d’exécution, tel qu’un `<iframe>` dans votre page ou une extension en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1518d-123">**Target**: Use the **Target** drop-down menu to switch to a different execution context, such as an `<iframe>` in your page or a running extension.</span></span> <span data-ttu-id="1518d-124">Par défaut, le cadre de niveau supérieur de votre page est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1518d-124">By default, the top-level frame of your page is selected.</span></span> <span data-ttu-id="1518d-125">Pointez sur une image sélectionnée pour afficher une info-bulle indiquant l’URL complète de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="1518d-125">Hovering over a selected frame displays a tooltip that shows the full URL for that resource.</span></span>

5. <span data-ttu-id="1518d-126">**Afficher la console**  /  Bouton **masquer la console** (**CTRL** +  **&grave;** ): outre le panneau de la console, vous pouvez utiliser la console à partir du bas de n’importe quel autre panneau devtools en appuyant sur le bouton **Afficher**la console  /  **Masquer** .</span><span class="sxs-lookup"><span data-stu-id="1518d-126">**Show Console** / **Hide Console** button (**Ctrl**+ **&grave;** ): In addition to the Console panel, you can use the console from the bottom of any other DevTools panel by pressing the **Show Console** / **Hide Console** button.</span></span> <span data-ttu-id="1518d-127">Le bouton n’a aucun effet lorsque DevTools est ouvert dans le panneau de la console.</span><span class="sxs-lookup"><span data-stu-id="1518d-127">The button has no effect when DevTools is open to the Console panel.</span></span>
 
6. <span data-ttu-id="1518d-128">**Journaux de filtre** (**Ctrl + F**): vous pouvez également filtrer les journaux à l’aide d’une chaîne de texte spécifique dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="1518d-128">**Filter logs** (**Ctrl+F**) : You can also filter logs by using a specific text string in the search box.</span></span>

7. <span data-ttu-id="1518d-129">**Débogueur**: sélectionnez n’importe quel lien source bleu pour ouvrir le débogueur devtools à cette ligne de code pour une inspection plus poussée.</span><span class="sxs-lookup"><span data-stu-id="1518d-129">**Debugger**: Select any blue source link to open the DevTools Debugger to that particular line of code for further inspection.</span></span>

## <span data-ttu-id="1518d-130">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="1518d-130">Shortcuts</span></span>

<span data-ttu-id="1518d-131">Action</span><span class="sxs-lookup"><span data-stu-id="1518d-131">Action</span></span>                                            | <span data-ttu-id="1518d-132">Raccourci</span><span class="sxs-lookup"><span data-stu-id="1518d-132">Shortcut</span></span>               
:-------------------------------------------------| :----------------------
<span data-ttu-id="1518d-133">Lancer DevTools avec la console activée</span><span class="sxs-lookup"><span data-stu-id="1518d-133">Launch DevTools with Console in focus</span></span>             | <span data-ttu-id="1518d-134">**CTRL**  +  **MAJ**  +  **J**</span><span class="sxs-lookup"><span data-stu-id="1518d-134">**Ctrl** + **Shift** + **J**</span></span> 
<span data-ttu-id="1518d-135">Basculer vers la console</span><span class="sxs-lookup"><span data-stu-id="1518d-135">Switch to the Console</span></span>                                 | <span data-ttu-id="1518d-136">**CTRL**  +  **2**</span><span class="sxs-lookup"><span data-stu-id="1518d-136">**Ctrl** + **2**</span></span>           
<span data-ttu-id="1518d-137">Afficher/masquer la console à partir d’un autre onglet DevTools</span><span class="sxs-lookup"><span data-stu-id="1518d-137">Show/hide the Console from another DevTools tab</span></span>       | <span data-ttu-id="1518d-138">\*\*\*\*  +  CTRL **&grave;** (battement du retour)</span><span class="sxs-lookup"><span data-stu-id="1518d-138">**Ctrl** + **&grave;** (back tick)</span></span>  
<span data-ttu-id="1518d-139">Exécuter (commande sur une ligne)</span><span class="sxs-lookup"><span data-stu-id="1518d-139">Execute (single-line command)</span></span>                     | **<span data-ttu-id="1518d-140">Entrée</span><span class="sxs-lookup"><span data-stu-id="1518d-140">Enter</span></span>**                
<span data-ttu-id="1518d-141">Saut de ligne sans s’exécuter (commande de plusieurs lignes)</span><span class="sxs-lookup"><span data-stu-id="1518d-141">Line break without executing (multi-line command)</span></span> | <span data-ttu-id="1518d-142">**MAJ**  +  **Entrée** ou **CTRL +**  +  **entrée**</span><span class="sxs-lookup"><span data-stu-id="1518d-142">**Shift** + **Enter** or **Ctrl** + **Enter**</span></span>      
<span data-ttu-id="1518d-143">Effacer la console de tous les messages</span><span class="sxs-lookup"><span data-stu-id="1518d-143">Clear the Console of all messages</span></span>                 | <span data-ttu-id="1518d-144">**CTRL**  +  **L**</span><span class="sxs-lookup"><span data-stu-id="1518d-144">**Ctrl** + **L**</span></span>           
<span data-ttu-id="1518d-145">Journaux de filtre (Positionnez le focus sur la zone de recherche)</span><span class="sxs-lookup"><span data-stu-id="1518d-145">Filter logs (set focus to search box)</span></span>             | <span data-ttu-id="1518d-146">**CTRL**  +  **F**</span><span class="sxs-lookup"><span data-stu-id="1518d-146">**Ctrl** + **F**</span></span>           
<span data-ttu-id="1518d-147">Accepter la suggestion de saisie semi-automatique (activée)</span><span class="sxs-lookup"><span data-stu-id="1518d-147">Accept auto-completion suggestion (when in focus)</span></span> | <span data-ttu-id="1518d-148">**Entrée** ou **Tab**</span><span class="sxs-lookup"><span data-stu-id="1518d-148">**Enter** or **Tab**</span></span>       
<span data-ttu-id="1518d-149">Suggestion de saisie semi-automatique précédente/suivante</span><span class="sxs-lookup"><span data-stu-id="1518d-149">Previous/next auto-completion suggestion</span></span>          | <span data-ttu-id="1518d-150">Touche de direction **haut** / **Touche de direction bas**</span><span class="sxs-lookup"><span data-stu-id="1518d-150">**Up arrow key**/**Down arrow key**</span></span>   
