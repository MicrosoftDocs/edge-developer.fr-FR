---
description: Découvrez comment afficher et modifier localStorage à l’aide du volet stockage local et de la console.
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 25404e454187db941dc12d356dfe5ae7437d833b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125418"
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

# <span data-ttu-id="99624-104">Afficher et modifier le stockage local avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="99624-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="99624-105">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [localStorage][MDNWindowsLocalStorage] .</span><span class="sxs-lookup"><span data-stu-id="99624-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="99624-106">Afficher les clés et valeurs de localStorage</span><span class="sxs-lookup"><span data-stu-id="99624-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="99624-107">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="99624-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="99624-108">Le volet **manifeste** est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="99624-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="99624-110">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="99624-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="99624-111">Développez le menu **stockage local** .</span><span class="sxs-lookup"><span data-stu-id="99624-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="99624-113">Menu **stockage local**</span><span class="sxs-lookup"><span data-stu-id="99624-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="99624-114">Sélectionnez un domaine pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="99624-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="99624-116">`localStorage`Paires clé-valeur pour le `https://www.bing.com` domaine</span><span class="sxs-lookup"><span data-stu-id="99624-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="99624-117">Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="99624-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="99624-119">Afficher la valeur de la `eventLogQueue_Online` clé</span><span class="sxs-lookup"><span data-stu-id="99624-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="99624-120">Créer une paire clé-valeur localStorage</span><span class="sxs-lookup"><span data-stu-id="99624-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="99624-121">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="99624-121">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="99624-122">Double-cliquez sur la partie vide de la table.</span><span class="sxs-lookup"><span data-stu-id="99624-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="99624-123">DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .</span><span class="sxs-lookup"><span data-stu-id="99624-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="99624-125">Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="99624-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="99624-126">Modifier les clés ou valeurs de localStorage</span><span class="sxs-lookup"><span data-stu-id="99624-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="99624-127">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="99624-127">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="99624-128">Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.</span><span class="sxs-lookup"><span data-stu-id="99624-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="99624-130">Modifier une `localStorage` clé</span><span class="sxs-lookup"><span data-stu-id="99624-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="99624-131">Supprimer des paires clé-valeur localStorage</span><span class="sxs-lookup"><span data-stu-id="99624-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="99624-132">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="99624-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="99624-133">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="99624-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="99624-134">DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="99624-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="99624-135">Appuyez sur la `Delete` touche ou sélectionnez **Supprimer la sélection** \ (supprimer la ![ sélection ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="99624-135">Press the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="99624-136">Supprimer toutes les `localStorage` paires clé-valeur pour un domaine</span><span class="sxs-lookup"><span data-stu-id="99624-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="99624-137">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="99624-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="99624-138">Sélectionnez **Effacer tout** ( ![ Effacer tout ][ImageClearIcon] ).</span><span class="sxs-lookup"><span data-stu-id="99624-138">Choose **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="99624-139">Interagir avec localStorage à partir de la console</span><span class="sxs-lookup"><span data-stu-id="99624-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="99624-140">Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et dans la mesure où la **console** a accès aux contextes JavaScript de la page, vous pouvez interagir avec celle-ci `localStorage` à partir de la **console**.</span><span class="sxs-lookup"><span data-stu-id="99624-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="99624-141">Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `localStorage` paires clé/valeur d’un domaine autre que la page qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="99624-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="99624-143">Changer le contexte JavaScript de la console</span><span class="sxs-lookup"><span data-stu-id="99624-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="99624-144">Exécutez vos `localStorage` expressions dans la console, de la même façon que dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="99624-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="99624-146">Interagir avec `localStorage` à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="99624-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="99624-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="99624-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="99624-150">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="99624-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="99624-151">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="99624-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="99624-153">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="99624-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
