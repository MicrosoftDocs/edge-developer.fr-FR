---
title: Afficher et modifier le stockage de session avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612080"
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





# <span data-ttu-id="65cbb-103">Afficher et modifier le stockage de session avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="65cbb-103">View And Edit Session Storage With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="65cbb-104">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des [`sessionStorage`][MDNSessionStorage] paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="65cbb-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="65cbb-105">Afficher les clés et valeurs de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="65cbb-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="65cbb-106">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="65cbb-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="65cbb-107">Le volet **manifeste** est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="65cbb-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-108">Figure1</span><span class="sxs-lookup"><span data-stu-id="65cbb-108">Figure 1</span></span>  
    > <span data-ttu-id="65cbb-109">Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="65cbb-109">The Manifest pane</span></span>  
    > ![Volet manifeste][ImageManifest]  

1.  <span data-ttu-id="65cbb-111">Développez le menu stockage de la **session** .</span><span class="sxs-lookup"><span data-stu-id="65cbb-111">Expand the **Session Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-112">Figure 2</span><span class="sxs-lookup"><span data-stu-id="65cbb-112">Figure 2</span></span>  
    > <span data-ttu-id="65cbb-113">Menu de **stockage de session**</span><span class="sxs-lookup"><span data-stu-id="65cbb-113">The **Session Storage** Menu</span></span>  
    > ![Menu de stockage de session][ImageSessionStorageMenu]  

1.  <span data-ttu-id="65cbb-115">Sélectionnez un domaine pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="65cbb-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-116">Figure3</span><span class="sxs-lookup"><span data-stu-id="65cbb-116">Figure 3</span></span>  
    > <span data-ttu-id="65cbb-117">Paires clé-valeur sessionStorage</span><span class="sxs-lookup"><span data-stu-id="65cbb-117">The sessionStorage key-value pairs</span></span>  
    > ![Paires clé-valeur «sessionStorage»][ImageSessionStorage]  

1.  <span data-ttu-id="65cbb-119">Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="65cbb-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-120">Figure 4</span><span class="sxs-lookup"><span data-stu-id="65cbb-120">Figure 4</span></span>  
    > <span data-ttu-id="65cbb-121">Affichage de la valeur de la `x-sid` clé</span><span class="sxs-lookup"><span data-stu-id="65cbb-121">Viewing the value of the `x-sid` key</span></span>  
    > ![Affichage de la valeur de la clé x-sid][ImageSessionStorageViewer]  

## <span data-ttu-id="65cbb-123">Créer une paire clé-valeur sessionStorage</span><span class="sxs-lookup"><span data-stu-id="65cbb-123">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="65cbb-124">[Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="65cbb-124">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="65cbb-125">Double-cliquez sur la partie vide de la table.</span><span class="sxs-lookup"><span data-stu-id="65cbb-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="65cbb-126">DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .</span><span class="sxs-lookup"><span data-stu-id="65cbb-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-127">Figure 5</span><span class="sxs-lookup"><span data-stu-id="65cbb-127">Figure 5</span></span>  
    > <span data-ttu-id="65cbb-128">Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="65cbb-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur][ImageSessionStorageCreate]  

## <span data-ttu-id="65cbb-130">Modifier les clés ou valeurs de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="65cbb-130">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="65cbb-131">[Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="65cbb-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="65cbb-132">Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.</span><span class="sxs-lookup"><span data-stu-id="65cbb-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-133">Figure 6</span><span class="sxs-lookup"><span data-stu-id="65cbb-133">Figure 6</span></span>  
    > <span data-ttu-id="65cbb-134">Modification d’une `sessionStorage` touche</span><span class="sxs-lookup"><span data-stu-id="65cbb-134">Editing a `sessionStorage` key</span></span>  
    > ![Modification d’une clé sessionStorage][ImageSessionStorageEdit]  

## <span data-ttu-id="65cbb-136">Supprimer des paires clé-valeur sessionStorage</span><span class="sxs-lookup"><span data-stu-id="65cbb-136">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="65cbb-137">[Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="65cbb-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="65cbb-138">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="65cbb-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="65cbb-139">DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="65cbb-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="65cbb-140">Appuyez sur la `Delete` touche ou cliquez sur supprimer la suppression **sélectionnée** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="65cbb-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="65cbb-141">Suppression de toutes les paires clé-valeur sessionStorage pour un domaine</span><span class="sxs-lookup"><span data-stu-id="65cbb-141">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="65cbb-142">[Afficher les `sessionStorage` paires clé-valeur d’un domaine](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="65cbb-142">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="65cbb-143">Sélectionnez **Effacer tout** ![ Effacer tout ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="65cbb-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="65cbb-144">Interagir avec sessionStorage à partir de la console</span><span class="sxs-lookup"><span data-stu-id="65cbb-144">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="65cbb-145">Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et puisque la **console** a accès aux contextes JavaScript de la page, il est possible d’interagir avec `sessionStorage` à partir de la **console**.</span><span class="sxs-lookup"><span data-stu-id="65cbb-145">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="65cbb-146">Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `sessionStorage` paires clé-valeur d’un domaine autre que celui de la page sur laquelle vous vous trouvez.</span><span class="sxs-lookup"><span data-stu-id="65cbb-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-147">Figure 7</span><span class="sxs-lookup"><span data-stu-id="65cbb-147">Figure 7</span></span>  
    > <span data-ttu-id="65cbb-148">Modification du contexte JavaScript de la **console**</span><span class="sxs-lookup"><span data-stu-id="65cbb-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Modification du contexte JavaScript de la console][ImageJSContext]  

1.  <span data-ttu-id="65cbb-150">Exécutez vos `sessionStorage` expressions dans la console, de la même manière que dans JavaScript.</span><span class="sxs-lookup"><span data-stu-id="65cbb-150">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="65cbb-151">Figure8</span><span class="sxs-lookup"><span data-stu-id="65cbb-151">Figure 8</span></span>  
    > <span data-ttu-id="65cbb-152">Interaction `sessionStorage` à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="65cbb-152">Interacting with `sessionStorage` from the **Console**</span></span>  
    > ![Interaction avec sessionStorage à partir de la console][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Figure 2: menu de stockage de session"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Figure 3: paires clé-valeur sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Figure 4: affichage de la valeur de la clé x-sid"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Figure 5: partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur"  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Figure 6: modification d’une clé de sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Figure 7: modification du contexte JavaScript de la console"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Figure 8: interaction avec sessionStorage à partir de la console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="65cbb-164">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="65cbb-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="65cbb-165">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="65cbb-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="65cbb-167">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="65cbb-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
