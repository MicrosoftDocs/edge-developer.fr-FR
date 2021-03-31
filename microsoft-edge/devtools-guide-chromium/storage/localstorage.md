---
description: Découvrez comment afficher et modifier localStorage avec le volet Stockage local et la console.
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439674"
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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="7fb41-104">Afficher et modifier le stockage local avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7fb41-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7fb41-105">Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [localStorage.][MDNWindowsLocalStorage]</span><span class="sxs-lookup"><span data-stu-id="7fb41-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <a name="view-localstorage-keys-and-values"></a><span data-ttu-id="7fb41-106">Afficher les clés et les valeurs localStorage</span><span class="sxs-lookup"><span data-stu-id="7fb41-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="7fb41-107">Choisissez **l’onglet Application** pour ouvrir **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="7fb41-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="7fb41-108">Le **volet** Manifeste s’affiche par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fb41-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="7fb41-110">Volet  manifeste</span><span class="sxs-lookup"><span data-stu-id="7fb41-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7fb41-111">Développez le menu **Stockage** local.</span><span class="sxs-lookup"><span data-stu-id="7fb41-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menu Stockage local" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="7fb41-113">Menu **Stockage** local</span><span class="sxs-lookup"><span data-stu-id="7fb41-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7fb41-114">Choisissez un domaine pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="7fb41-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Paires clé-valeur localStorage pour le https://www.bing.com domaine" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="7fb41-116">Paires `localStorage` clé-valeur pour le `https://www.bing.com` domaine</span><span class="sxs-lookup"><span data-stu-id="7fb41-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7fb41-117">Choisissez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="7fb41-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Afficher la valeur de la eventLogQueue_Online clé" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="7fb41-119">Afficher la valeur de la `eventLogQueue_Online` clé</span><span class="sxs-lookup"><span data-stu-id="7fb41-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a><span data-ttu-id="7fb41-120">Créer une paire clé-valeur localStorage</span><span class="sxs-lookup"><span data-stu-id="7fb41-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="7fb41-121">[Afficher les paires clé-valeur localStorage d’un domaine.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="7fb41-121">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7fb41-122">Double-cliquez sur la partie vide du tableau.</span><span class="sxs-lookup"><span data-stu-id="7fb41-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="7fb41-123">DevTools crée une ligne et concentre votre curseur dans la **colonne** Clé.</span><span class="sxs-lookup"><span data-stu-id="7fb41-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Partie vide du tableau à double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="7fb41-125">Partie vide du tableau à double-cliquer pour créer une paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="7fb41-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a><span data-ttu-id="7fb41-126">Modifier les clés ou valeurs localStorage</span><span class="sxs-lookup"><span data-stu-id="7fb41-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="7fb41-127">[Afficher les paires clé-valeur localStorage d’un domaine.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="7fb41-127">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7fb41-128">Double-cliquez sur une cellule  dans la colonne **Clé** ou Valeur pour modifier cette clé ou cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7fb41-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Modifier une clé localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="7fb41-130">Modifier une `localStorage` clé</span><span class="sxs-lookup"><span data-stu-id="7fb41-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a><span data-ttu-id="7fb41-131">Supprimer les paires clé-valeur localStorage</span><span class="sxs-lookup"><span data-stu-id="7fb41-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="7fb41-132">[Afficher les `localStorage` paires clé-valeur d’un domaine.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="7fb41-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7fb41-133">Choisissez la paire clé-valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7fb41-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="7fb41-134">DevTools le met en sur-soulignement en bleu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7fb41-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="7fb41-135">Sélectionnez `Delete` la clé ou choisissez Supprimer **sélectionné** \( Supprimer ![ sélectionné ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="7fb41-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="7fb41-136">Supprimer toutes `localStorage` les paires clé-valeur pour un domaine</span><span class="sxs-lookup"><span data-stu-id="7fb41-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="7fb41-137">[Afficher les `localStorage` paires clé-valeur d’un domaine.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="7fb41-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="7fb41-138">Choose **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="7fb41-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-localstorage-from-the-console"></a><span data-ttu-id="7fb41-139">Interagir avec localStorage à partir de la console</span><span class="sxs-lookup"><span data-stu-id="7fb41-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="7fb41-140">Étant donné que vous pouvez exécuter JavaScript dans la **console**et que la **console** a accès aux contextes JavaScript de la page, il est possible d’interagir avec à partir de `localStorage` la **console.**</span><span class="sxs-lookup"><span data-stu-id="7fb41-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="7fb41-141">Utilisez le menu **Contexts JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux paires clé-valeur d’un domaine autre que la page qui `localStorage` s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7fb41-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Modifier le contexte JavaScript de la console" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="7fb41-143">Modifier le contexte JavaScript de la console</span><span class="sxs-lookup"><span data-stu-id="7fb41-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7fb41-144">Exécutez vos expressions dans la console, comme vous le faites `localStorage` dans votre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7fb41-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagir avec localStorage à partir de la console" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="7fb41-146">Interagir avec `localStorage` à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="7fb41-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7fb41-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7fb41-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="7fb41-150">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7fb41-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7fb41-151">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="7fb41-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="7fb41-153">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7fb41-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
