---
description: La fonctionnalité Overrides est une fonctionnalité de l’outil Sources de Microsoft Edge DevTools qui vous permet de copier des ressources de page web sur votre disque dur.  Lorsque vous actualisez la page web, DevTools ne charge pas la ressource, mais la remplace par votre copie locale.
title: Remplacer les ressources de page web avec des copies locales à l’aide de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11230963"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a><span data-ttu-id="720f8-105">Remplacer les ressources de page web avec des copies locales à l’aide de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="720f8-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="720f8-106">Parfois, vous devez résoudre un problème sur une page web à qui vous n’avez pas accès ou les correctifs impliquent un processus de création lent et complexe.</span><span class="sxs-lookup"><span data-stu-id="720f8-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="720f8-107">Vous pouvez déboguer et résoudre tous les types de problèmes dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="720f8-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="720f8-108">Mais le problème est que les modifications ne sont pas persistantes.</span><span class="sxs-lookup"><span data-stu-id="720f8-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="720f8-109">Une fois que vous avez actualisé le fichier, tout votre travail a disparu.</span><span class="sxs-lookup"><span data-stu-id="720f8-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="720f8-110">La fonctionnalité Remplacements de l’outil [Sources][DevToolsSourcesTool] vous aide à résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="720f8-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="720f8-111">Vous pouvez maintenant prendre une ressource de la page web actuelle et la stocker localement.</span><span class="sxs-lookup"><span data-stu-id="720f8-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="720f8-112">Lorsque vous actualisez la page web, le navigateur ne charge pas la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="720f8-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="720f8-113">Au lieu de cela, le navigateur le remplace par votre copie locale de la ressource.</span><span class="sxs-lookup"><span data-stu-id="720f8-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <a name="setting-up-your-local-folder-to-store-overrides"></a><span data-ttu-id="720f8-114">Configuration de votre dossier local pour stocker les remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="720f8-115">Dans **l’outil Sources,** recherchez plusieurs sections sur le côté gauche.</span><span class="sxs-lookup"><span data-stu-id="720f8-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="720f8-116">Si **l’option Remplacements** n’est pas affichée, choisissez la</span><span class="sxs-lookup"><span data-stu-id="720f8-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="720f8-117">pour y arriver.</span><span class="sxs-lookup"><span data-stu-id="720f8-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Outil Sources avec un espace insuffisant pour afficher l’option de remplacements" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="720f8-119">**Outil Sources** avec un espace insuffisant pour afficher l’option de remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Choisir l’option remplacements" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="720f8-121">Choisir l’option remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="720f8-122">Après avoir choisi **l’option Remplacements,** vous devez choisir un dossier sur votre ordinateur local pour stocker les fichiers de ressources que vous souhaitez remplacer.</span><span class="sxs-lookup"><span data-stu-id="720f8-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="720f8-123">Choisissez le **dossier + Sélectionner pour les remplacements** pour rechercher un dossier.</span><span class="sxs-lookup"><span data-stu-id="720f8-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Choisir un dossier à utiliser pour les remplacements" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="720f8-125">Choisir un dossier à utiliser pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="720f8-126">DevTools vous avertit que vous devez avoir un accès total au dossier et que vous ne devez pas révéler d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="720f8-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="720f8-127">Dans la barre d’avertissement, **sélectionnez Autoriser** l’accès.</span><span class="sxs-lookup"><span data-stu-id="720f8-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="accorder à DevTools l’accès au dossier ;" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="720f8-129">Accorder à DevTools l’accès au dossier</span><span class="sxs-lookup"><span data-stu-id="720f8-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="720f8-130">Dans le **volet Remplacements,** une case à cocher doit s’afficher en regard de votre dossier `Enable Local Overrides` remplacements.</span><span class="sxs-lookup"><span data-stu-id="720f8-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="720f8-131">Une icône s’affiche en face de celle-ci qui vous permet de supprimer vos paramètres de remplacements locaux.</span><span class="sxs-lookup"><span data-stu-id="720f8-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="720f8-132">Vous avez maintenant terminé la configuration de votre dossier et êtes prêt à remplacer les ressources en direct par des ressources locales.</span><span class="sxs-lookup"><span data-stu-id="720f8-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="La mise en place d’un dossier de remplacements a réussi" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="720f8-134">La mise en place d’un dossier de remplacements a réussi</span><span class="sxs-lookup"><span data-stu-id="720f8-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a><span data-ttu-id="720f8-135">Ajout de fichiers à votre dossier Overrides</span><span class="sxs-lookup"><span data-stu-id="720f8-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="720f8-136">Pour ajouter des fichiers à votre dossier de remplacements, ouvrez l’outil **Éléments** et examinez la page web.</span><span class="sxs-lookup"><span data-stu-id="720f8-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="720f8-137">Pour modifier, choisissez le nom du fichier CSS dans l’inspecteur **de styles.**</span><span class="sxs-lookup"><span data-stu-id="720f8-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Choisir un fichier dans l’inspecteur styles" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="720f8-139">Choisir un fichier dans l’inspecteur **styles**</span><span class="sxs-lookup"><span data-stu-id="720f8-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="720f8-140">Dans l’éditeur **sources,** pointez sur le nom de fichier de votre fichier choisi, ouvrez le menu contextuel \(clic droit\), puis choisissez Enregistrer pour **les remplacements.**</span><span class="sxs-lookup"><span data-stu-id="720f8-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Dans l’éditeur sources, ajoutez le nom du fichier aux substitutions" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="720f8-142">Dans **l’éditeur sources,** ajoutez le nom du fichier aux substitutions</span><span class="sxs-lookup"><span data-stu-id="720f8-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Dans le menu contexto, sélectionnez Enregistrer pour les remplacements" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="720f8-144">Dans le menu contexto, **sélectionnez Enregistrer pour les remplacements**</span><span class="sxs-lookup"><span data-stu-id="720f8-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="720f8-145">Le fichier est stocké dans votre dossier remplacements.</span><span class="sxs-lookup"><span data-stu-id="720f8-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="720f8-146">Vérifiez que DevTools crée un dossier nommé à l’aide de l’URL du fichier avec la structure de répertoires correcte.</span><span class="sxs-lookup"><span data-stu-id="720f8-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="720f8-147">Le fichier est stocké à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="720f8-147">The file is stored inside.</span></span>  <span data-ttu-id="720f8-148">Le nom de fichier dans l’éditeur affiche désormais également un point violet qui indique que le fichier est local et non en direct.</span><span class="sxs-lookup"><span data-stu-id="720f8-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Le fichier a été correctement stocké dans votre dossier remplacements" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="720f8-150">Le fichier a été correctement stocké dans votre dossier remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="720f8-151">Dans l’exemple suivant, vous pouvez maintenant modifier les styles de la page web.</span><span class="sxs-lookup"><span data-stu-id="720f8-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="720f8-152">Pour ajouter une bordure rouge autour du fichier, dans l’éditeur **styles,** copiez le style suivant et ajoutez-le à l’élément body.</span><span class="sxs-lookup"><span data-stu-id="720f8-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="720f8-153">Le fichier est automatiquement enregistré sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="720f8-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="720f8-154">Si vous actualisez le fichier, la bordure s’affiche et aucune partie de votre travail n’est perdue.</span><span class="sxs-lookup"><span data-stu-id="720f8-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Modifier les styles de page web de façon permanente en éditant un fichier dans votre dossier Remplacements" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="720f8-156">Modifier les styles de page web de façon permanente en éditant un fichier dans votre dossier Remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="720f8-157">Dans **l’outil Sources,** dans la section **Page,** pointez sur n’importe quel fichier, ouvrez le menu contextuel \(clic droit\) et ajoutez-le aux remplacements.</span><span class="sxs-lookup"><span data-stu-id="720f8-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="720f8-158">Là encore, les fichiers déjà dans votre dossier remplacements ont un point violet sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="720f8-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Choisir un fichier dans l’outil Sources pour les remplacements" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="720f8-160">Choisir un fichier dans **l’outil Sources** pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="720f8-161">Vous pouvez également, sur l’outil **Réseau,** pointer sur n’importe quel fichier, ouvrir le menu contextuel \(clic droit\) et l’ajouter aux remplacements.</span><span class="sxs-lookup"><span data-stu-id="720f8-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="720f8-162">Lorsque les substitutions sont en vigueur, les fichiers qui se trouvent sur votre ordinateur et non à partir de la page web en direct.</span><span class="sxs-lookup"><span data-stu-id="720f8-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="720f8-163">Lorsque les substitutions sont en vigueur, sur l’outil **Réseau,** recherchez une icône d’avertissement en face du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="720f8-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Choisir un fichier dans l’outil Réseau pour les remplacements" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="720f8-165">Choisir un fichier dans **l’outil** Réseau pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="720f8-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a><span data-ttu-id="720f8-166">Interaction double des substitutions</span><span class="sxs-lookup"><span data-stu-id="720f8-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="720f8-167">Utilisez l’éditeur fourni avec l’outil **Sources** de DevTools ou tout éditeur que vous souhaitez modifier les fichiers.</span><span class="sxs-lookup"><span data-stu-id="720f8-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="720f8-168">Les modifications sont synchronisées entre tous les produits qui accèdent aux fichiers dans le dossier remplacements.</span><span class="sxs-lookup"><span data-stu-id="720f8-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="720f8-169">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="720f8-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
