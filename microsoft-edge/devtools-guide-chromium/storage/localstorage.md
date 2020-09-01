---
title: Afficher et modifier le stockage local avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 72aee823d3a3143ae7399c7057f3b606bd1078c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983505"
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





# <span data-ttu-id="b67f2-103">Afficher et modifier le stockage local avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b67f2-103">View and edit local storage with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="b67f2-104">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [localStorage][MDNWindowsLocalStorage] .</span><span class="sxs-lookup"><span data-stu-id="b67f2-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="b67f2-105">Afficher les clés et valeurs de localStorage</span><span class="sxs-lookup"><span data-stu-id="b67f2-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="b67f2-106">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="b67f2-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="b67f2-107">Le volet **manifeste** est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="b67f2-107">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="b67f2-109">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="b67f2-109">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b67f2-110">Développez le menu **stockage local** .</span><span class="sxs-lookup"><span data-stu-id="b67f2-110">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menu stockage local" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="b67f2-112">Menu **stockage local**</span><span class="sxs-lookup"><span data-stu-id="b67f2-112">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b67f2-113">Sélectionnez un domaine pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="b67f2-113">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Paires clé-valeur localStorage pour le https://www.bing.com domaine" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="b67f2-115">`localStorage`Paires clé-valeur pour le `https://www.bing.com` domaine</span><span class="sxs-lookup"><span data-stu-id="b67f2-115">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b67f2-116">Sélectionnez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="b67f2-116">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Afficher la valeur de la clé de eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="b67f2-118">Afficher la valeur de la `eventLogQueue_Online` clé</span><span class="sxs-lookup"><span data-stu-id="b67f2-118">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b67f2-119">Créer une paire clé-valeur localStorage</span><span class="sxs-lookup"><span data-stu-id="b67f2-119">Create a new localStorage key-value pair</span></span>   

1.  <span data-ttu-id="b67f2-120">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b67f2-120">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b67f2-121">Double-cliquez sur la partie vide de la table.</span><span class="sxs-lookup"><span data-stu-id="b67f2-121">Double-click the empty part of the table.</span></span>  <span data-ttu-id="b67f2-122">DevTools crée une nouvelle ligne et concentre votre curseur dans la colonne **clé** .</span><span class="sxs-lookup"><span data-stu-id="b67f2-122">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="b67f2-124">Partie vide de la table dans laquelle vous pouvez double-cliquer pour créer une paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="b67f2-124">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b67f2-125">Modifier les clés ou valeurs de localStorage</span><span class="sxs-lookup"><span data-stu-id="b67f2-125">Edit localStorage keys or values</span></span>   

1.  <span data-ttu-id="b67f2-126">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b67f2-126">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b67f2-127">Double-cliquez sur une cellule dans la colonne **clé** ou **valeur** pour modifier cette clé ou valeur.</span><span class="sxs-lookup"><span data-stu-id="b67f2-127">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Modifier une clé de localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="b67f2-129">Modifier une `localStorage` clé</span><span class="sxs-lookup"><span data-stu-id="b67f2-129">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b67f2-130">Supprimer des paires clé-valeur localStorage</span><span class="sxs-lookup"><span data-stu-id="b67f2-130">Delete localStorage key-value pairs</span></span>   

1.  <span data-ttu-id="b67f2-131">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b67f2-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b67f2-132">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="b67f2-132">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="b67f2-133">DevTools met en surbrillance bleu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b67f2-133">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="b67f2-134">Appuyez sur la `Delete` touche ou cliquez sur **Supprimer la sélection** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="b67f2-134">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="b67f2-135">Supprimer toutes les `localStorage` paires clé-valeur pour un domaine</span><span class="sxs-lookup"><span data-stu-id="b67f2-135">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="b67f2-136">[Afficher les `localStorage` paires clé-valeur d’un domaine](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b67f2-136">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b67f2-137">Sélectionnez **Effacer tout** \ ( ![ Effacer tout ][ImageClearIcon] ).</span><span class="sxs-lookup"><span data-stu-id="b67f2-137">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="b67f2-138">Interagir avec localStorage à partir de la console</span><span class="sxs-lookup"><span data-stu-id="b67f2-138">Interact with localStorage from the Console</span></span>   

<span data-ttu-id="b67f2-139">Dans la mesure où vous pouvez exécuter JavaScript dans la **console**, et dans la mesure où la **console** a accès aux contextes JavaScript de la page, vous pouvez interagir avec celle-ci `localStorage` à partir de la **console**.</span><span class="sxs-lookup"><span data-stu-id="b67f2-139">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="b67f2-140">Utilisez le menu **contextes JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `localStorage` paires clé/valeur d’un domaine autre que la page qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b67f2-140">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Changer le contexte JavaScript de la console" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="b67f2-142">Changer le contexte JavaScript de la console</span><span class="sxs-lookup"><span data-stu-id="b67f2-142">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b67f2-143">Exécutez vos `localStorage` expressions dans la console, de la même façon que dans votre code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b67f2-143">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagir avec localStorage à partir de la console" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="b67f2-145">Interagir avec `localStorage` à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="b67f2-145">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="b67f2-148">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b67f2-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b67f2-149">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="b67f2-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="b67f2-151">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b67f2-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
