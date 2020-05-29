---
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612010"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="d1d44-103">Afficher et modifier le stockage local avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d1d44-103">View And Edit Local Storage With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="d1d44-104">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des [`localStorage`][MDNWindowsLocalStorage] paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="d1d44-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`localStorage`][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="d1d44-105">Afficher les clés et valeurs de localStorage</span><span class="sxs-lookup"><span data-stu-id="d1d44-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="d1d44-106">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="d1d44-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="d1d44-107">Le volet **manifeste** est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1d44-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-108">Figure1</span><span class="sxs-lookup"><span data-stu-id="d1d44-108">Figure 1</span></span>  
    > <span data-ttu-id="d1d44-109">Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="d1d44-109">The Manifest pane</span></span>  
    > ![Volet manifeste][ImageManifest]  

1.  <span data-ttu-id="d1d44-111">Développez le menu **stockage local** .</span><span class="sxs-lookup"><span data-stu-id="d1d44-111">Expand the **Local Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-112">Figure 2</span><span class="sxs-lookup"><span data-stu-id="d1d44-112">Figure 2</span></span>  
    > <span data-ttu-id="d1d44-113">Le menu **stockage local** affiche deux domaines: `https://business.bing.com` et</span><span class="sxs-lookup"><span data-stu-id="d1d44-113">The **Local Storage** menu shows two domains: `https://business.bing.com` and</span></span> `https://www.bing.com`  
    > ![Menu stockage local][ImageLocalStorageMenu]  

1.  <span data-ttu-id="d1d44-115">Sélectionnez un domaine pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="d1d44-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-116">Figure3</span><span class="sxs-lookup"><span data-stu-id="d1d44-116">Figure 3</span></span>  
    > <span data-ttu-id="d1d44-117">`localStorage`Paires clé-valeur pour le `https://www.bing.com` domaine</span><span class="sxs-lookup"><span data-stu-id="d1d44-117">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    > ![Paires clé-valeur localStorage pour le https://www.bing.com domaine][ImageLocalStorage]  

1.  <span data-ttu-id="d1d44-119">Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="d1d44-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-120">Figure 4</span><span class="sxs-lookup"><span data-stu-id="d1d44-120">Figure 4</span></span>  
    > <span data-ttu-id="d1d44-121">Affichage de la valeur de la `eventLogQueue_Online` clé</span><span class="sxs-lookup"><span data-stu-id="d1d44-121">Viewing the value of the `eventLogQueue_Online` key</span></span>  
    > ![Affichage de la valeur de la clé eventLogQueue_Online][ImageLocalStorageViewer]  

## <span data-ttu-id="d1d44-123">Créer une `localStorage` paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="d1d44-123">Create a new `localStorage` key-value pair</span></span>   

1.  <span data-ttu-id="d1d44-124">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1d44-124">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1d44-125">Double-cliquez sur la partie vide de la table.</span><span class="sxs-lookup"><span data-stu-id="d1d44-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="d1d44-126">DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .</span><span class="sxs-lookup"><span data-stu-id="d1d44-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-127">Figure 5</span><span class="sxs-lookup"><span data-stu-id="d1d44-127">Figure 5</span></span>  
    > <span data-ttu-id="d1d44-128">Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="d1d44-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur][ImageLocalStorageCreate]  

## <span data-ttu-id="d1d44-130">Modifier les `localStorage` clés ou les valeurs</span><span class="sxs-lookup"><span data-stu-id="d1d44-130">Edit `localStorage` keys or values</span></span>   

1.  <span data-ttu-id="d1d44-131">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1d44-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1d44-132">Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.</span><span class="sxs-lookup"><span data-stu-id="d1d44-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-133">Figure 6</span><span class="sxs-lookup"><span data-stu-id="d1d44-133">Figure 6</span></span>  
    > <span data-ttu-id="d1d44-134">Modification d’une `localStorage` touche</span><span class="sxs-lookup"><span data-stu-id="d1d44-134">Editing a `localStorage` key</span></span>  
    > ![Modification d’une clé localStorage][ImageLocalStorageEdit]  

## <span data-ttu-id="d1d44-136">Supprimer `localStorage` des paires clé-valeur</span><span class="sxs-lookup"><span data-stu-id="d1d44-136">Delete `localStorage` key-value pairs</span></span>   

1.  <span data-ttu-id="d1d44-137">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1d44-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1d44-138">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="d1d44-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="d1d44-139">DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d1d44-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="d1d44-140">Appuyez sur la `Delete` touche ou cliquez sur supprimer la suppression **sélectionnée** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="d1d44-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="d1d44-141">Supprimer toutes les `localStorage` paires clé-valeur pour un domaine</span><span class="sxs-lookup"><span data-stu-id="d1d44-141">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="d1d44-142">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1d44-142">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="d1d44-143">Sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="d1d44-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="d1d44-144">Interagir avec `localStorage` à partir de la console</span><span class="sxs-lookup"><span data-stu-id="d1d44-144">Interact with `localStorage` from the Console</span></span>   

<span data-ttu-id="d1d44-145">Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et dans la mesure où la **console** a accès aux contextes JavaScript de la page, vous pouvez interagir avec celle-ci `localStorage` à partir de la **console**.</span><span class="sxs-lookup"><span data-stu-id="d1d44-145">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="d1d44-146">Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `localStorage` paires clé/valeur d’un domaine autre que la page qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d1d44-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-147">Figure 7</span><span class="sxs-lookup"><span data-stu-id="d1d44-147">Figure 7</span></span>  
    > <span data-ttu-id="d1d44-148">Modification du contexte JavaScript de la **console**</span><span class="sxs-lookup"><span data-stu-id="d1d44-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Modification du contexte JavaScript de la console][ImageJSContext]  

1.  <span data-ttu-id="d1d44-150">Exécutez vos `localStorage` expressions dans la console, de la même façon que dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1d44-150">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="d1d44-151">Figure8</span><span class="sxs-lookup"><span data-stu-id="d1d44-151">Figure 8</span></span>  
    > <span data-ttu-id="d1d44-152">Interaction `localStorage` à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="d1d44-152">Interacting with `localStorage` from the **Console**</span></span>  
    > ![Interaction avec localStorage à partir de la console][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Figure 2: menu stockage local"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Figure 3: paires clé-valeur localStorage pour le https://www.bing.com domaine"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Figure 4: affichage de la valeur de la clé de eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Figure 5: partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Figure 6: modification d’une clé de localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Figure 7: modification du contexte JavaScript de la console"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Figure 8: interaction avec localStorage à partir de la console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="d1d44-164">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d1d44-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d1d44-165">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="d1d44-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="d1d44-167">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d1d44-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
