---
description: Découvrez comment afficher et modifier sessionStorage avec le volet Stockage de session et la console.
title: Afficher et modifier le stockage de session avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0168b01fd01071ebd19bd211c6d947ae006d778c
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439660"
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

# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="2ac38-104">Afficher et modifier le stockage de session avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2ac38-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="2ac38-105">Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour afficher, modifier et supprimer des paires clé-valeur [sessionStorage.][MDNSessionStorage]</span><span class="sxs-lookup"><span data-stu-id="2ac38-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [sessionStorage][MDNSessionStorage] key-value pairs.</span></span>  

## <a name="view-sessionstorage-keys-and-values"></a><span data-ttu-id="2ac38-106">Afficher les clés et les valeurs sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2ac38-106">View sessionStorage keys and values</span></span>  

1.  <span data-ttu-id="2ac38-107">Choisissez **l’onglet Application** pour ouvrir **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="2ac38-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="2ac38-108">Le **panneau** manifeste est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ac38-108">The **Manifest** panel is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="2ac38-110">Volet \*\*\*\* manifeste</span><span class="sxs-lookup"><span data-stu-id="2ac38-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ac38-111">Développez le menu **Stockage de** session.</span><span class="sxs-lookup"><span data-stu-id="2ac38-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Menu Stockage de session" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="2ac38-113">Menu **Stockage de** session</span><span class="sxs-lookup"><span data-stu-id="2ac38-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ac38-114">Choisissez un domaine pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="2ac38-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Paires clé-valeur sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="2ac38-116">Paires `sessionStorage` clé-valeur</span><span class="sxs-lookup"><span data-stu-id="2ac38-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ac38-117">Choisissez une ligne du tableau pour afficher la valeur dans la visionneuse sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="2ac38-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Afficher la valeur de la touche x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="2ac38-119">Afficher la valeur de la `x-sid` clé</span><span class="sxs-lookup"><span data-stu-id="2ac38-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a><span data-ttu-id="2ac38-120">Créer une paire clé-valeur sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2ac38-120">Create a new sessionStorage key-value pair</span></span>  

1.  <span data-ttu-id="2ac38-121">[Afficher les paires clé-valeur sessionStorage d’un domaine.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="2ac38-121">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2ac38-122">Double-cliquez sur la partie vide du tableau.</span><span class="sxs-lookup"><span data-stu-id="2ac38-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="2ac38-123">DevTools crée une ligne et concentre votre curseur dans la **colonne** Clé.</span><span class="sxs-lookup"><span data-stu-id="2ac38-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Partie vide du tableau à double-cliquer pour créer une paire clé-valeur" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="2ac38-125">Partie vide du tableau à double-cliquer pour créer une paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="2ac38-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a><span data-ttu-id="2ac38-126">Modifier les clés ou valeurs sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2ac38-126">Edit sessionStorage keys or values</span></span>  

1.  <span data-ttu-id="2ac38-127">[Afficher les paires clé-valeur sessionStorage d’un domaine.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="2ac38-127">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2ac38-128">Double-cliquez sur une cellule \*\*\*\* dans la colonne **Clé** ou Valeur pour modifier cette clé ou cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2ac38-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Modifier une clé sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="2ac38-130">Modifier une `sessionStorage` clé</span><span class="sxs-lookup"><span data-stu-id="2ac38-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a><span data-ttu-id="2ac38-131">Supprimer des paires clé-valeur sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2ac38-131">Delete sessionStorage key-value pairs</span></span>  

1.  <span data-ttu-id="2ac38-132">[Afficher les `sessionStorage` paires clé-valeur d’un domaine.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="2ac38-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2ac38-133">Choisissez la paire clé-valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2ac38-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="2ac38-134">DevTools le met en sur-soulignement en bleu pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2ac38-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="2ac38-135">Sélectionnez `Delete` la clé ou choisissez Supprimer **sélectionné** \( Supprimer ![ sélectionné ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="2ac38-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="2ac38-136">Supprimer toutes les paires clé-valeur sessionStorage pour un domaine</span><span class="sxs-lookup"><span data-stu-id="2ac38-136">Delete all sessionStorage key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="2ac38-137">[Afficher les `sessionStorage` paires clé-valeur d’un domaine.](#view-sessionstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="2ac38-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2ac38-138">Choose **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="2ac38-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-sessionstorage-from-the-console"></a><span data-ttu-id="2ac38-139">Interagir avec sessionStorage à partir de la console</span><span class="sxs-lookup"><span data-stu-id="2ac38-139">Interact with sessionStorage from the Console</span></span>  

<span data-ttu-id="2ac38-140">Étant donné que vous pouvez exécuter JavaScript dans la **console**et que la **console** a accès aux contextes JavaScript de la page, il est possible d’interagir avec à partir de `sessionStorage` la **console.**</span><span class="sxs-lookup"><span data-stu-id="2ac38-140">Since you may run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="2ac38-141">Utilisez le menu **Contexts JavaScript** pour modifier le contexte JavaScript de la **console** si vous souhaitez accéder aux `sessionStorage` paires clé-valeur d’un domaine autre que la page sur lequel vous êtes.</span><span class="sxs-lookup"><span data-stu-id="2ac38-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Modifier le contexte JavaScript de la console" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="2ac38-143">Modifier le contexte JavaScript de la **console**</span><span class="sxs-lookup"><span data-stu-id="2ac38-143">Change the JavaScript context of the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2ac38-144">Exécutez `sessionStorage` vos expressions dans la **console,** de la même manière que votre JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ac38-144">Run your `sessionStorage` expressions in the **Console**, the same as your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagir avec sessionStorage à partir de la console" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="2ac38-146">Interagir avec `sessionStorage` à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="2ac38-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2ac38-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2ac38-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage, | MDN"  

> [!NOTE]
> <span data-ttu-id="2ac38-150">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ac38-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2ac38-151">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2ac38-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2ac38-153">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ac38-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
