---
description: La fonctionnalité de substitution est une fonctionnalité de l’outil sources de Microsoft Edge DevTools qui vous permet de copier des ressources de pages Web sur votre disque dur.  Lorsque vous actualisez la page Web, DevTools ne chargez pas la ressource, mais remplacez-la par votre copie locale.
title: Remplacer les ressources de pages Web par des copies locales à l’aide de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 579ebe92dc50571837e7e3caf8fb7c1a9989bc59
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145155"
---
# <span data-ttu-id="7f159-105">Remplacer les ressources de pages Web par des copies locales à l’aide de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7f159-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7f159-106">Il peut arriver que vous deviez résoudre un problème sur une page Web à laquelle vous n’avez pas accès ou qui nécessite un processus de génération lent et complexe.</span><span class="sxs-lookup"><span data-stu-id="7f159-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="7f159-107">Vous pouvez déboguer et résoudre tout type de problème dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="7f159-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="7f159-108">Toutefois, le problème ne persiste pas.</span><span class="sxs-lookup"><span data-stu-id="7f159-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="7f159-109">Après avoir actualisé le fichier, tout votre bureau a disparu.</span><span class="sxs-lookup"><span data-stu-id="7f159-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="7f159-110">La fonctionnalité de remplacement de l’outil [sources][DevToolsSourcesTool] vous permet de résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="7f159-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="7f159-111">Vous pouvez à présent prendre une ressource de la page Web actuelle et la stocker localement.</span><span class="sxs-lookup"><span data-stu-id="7f159-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="7f159-112">Lorsque vous actualisez la page Web, le navigateur ne charge pas la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="7f159-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="7f159-113">Au lieu de cela, le navigateur le remplace par votre copie locale de la ressource.</span><span class="sxs-lookup"><span data-stu-id="7f159-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <span data-ttu-id="7f159-114">Configuration de votre dossier local pour le stockage des remplacements</span><span class="sxs-lookup"><span data-stu-id="7f159-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="7f159-115">Dans l’outil **sources** , recherchez plusieurs sections sur le côté gauche.</span><span class="sxs-lookup"><span data-stu-id="7f159-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="7f159-116">Si l’option **remplacements** ne s’affiche pas, sélectionnez</span><span class="sxs-lookup"><span data-stu-id="7f159-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="7f159-117">pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="7f159-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Outil sources avec un espace insuffisant pour afficher l’option de remplacement" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="7f159-119">Outil **sources** avec un espace insuffisant pour afficher l’option de remplacement</span><span class="sxs-lookup"><span data-stu-id="7f159-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Sélectionner l’option remplacements" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="7f159-121">Sélectionner l’option remplacements</span><span class="sxs-lookup"><span data-stu-id="7f159-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="7f159-122">Après avoir sélectionné l’option **remplacements** , vous devez choisir un dossier sur votre ordinateur local pour stocker les fichiers de ressources que vous souhaitez remplacer.</span><span class="sxs-lookup"><span data-stu-id="7f159-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="7f159-123">Pour rechercher un dossier, sélectionnez le **dossier + Sélectionner pour les remplacements** .</span><span class="sxs-lookup"><span data-stu-id="7f159-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Sélectionner un dossier à utiliser pour les remplacements" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="7f159-125">Sélectionner un dossier à utiliser pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="7f159-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7f159-126">DevTools vous avertit que vous devez disposer d’un accès complet au dossier et que vous ne devez pas divulguer d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="7f159-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="7f159-127">Dans la barre d’avertissement, sélectionnez **autoriser** pour accorder l’accès.</span><span class="sxs-lookup"><span data-stu-id="7f159-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="accorder à DevTools l’accès au dossier" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="7f159-129">Accorder à DevTools l’accès au dossier</span><span class="sxs-lookup"><span data-stu-id="7f159-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7f159-130">Dans le volet **remplacements** , une case à cocher doit s’afficher à côté `Enable Local Overrides` et au dossier de remplacements.</span><span class="sxs-lookup"><span data-stu-id="7f159-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="7f159-131">Une icône s’affiche à côté de celle-ci pour vous permettre de supprimer vos paramètres de remplacement locaux.</span><span class="sxs-lookup"><span data-stu-id="7f159-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="7f159-132">Vous avez terminé la configuration de votre dossier et vous êtes prêt à remplacer les ressources dynamiques par des ressources locales.</span><span class="sxs-lookup"><span data-stu-id="7f159-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuration réussie d’un dossier de remplacement" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="7f159-134">Configuration réussie d’un dossier de remplacement</span><span class="sxs-lookup"><span data-stu-id="7f159-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7f159-135">Ajouter des fichiers à votre dossier de remplacement</span><span class="sxs-lookup"><span data-stu-id="7f159-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="7f159-136">Pour ajouter des fichiers à votre dossier de remplacements, ouvrez l’outil **éléments** et examinez la page Web.</span><span class="sxs-lookup"><span data-stu-id="7f159-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="7f159-137">Pour modifier le fichier CSS, sélectionnez son nom dans l’inspecteur de **styles** .</span><span class="sxs-lookup"><span data-stu-id="7f159-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Sélectionner un fichier dans l’inspecteur de styles" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="7f159-139">Sélectionner un fichier dans l’inspecteur de **styles**</span><span class="sxs-lookup"><span data-stu-id="7f159-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="7f159-140">Dans l’éditeur de **sources** , pointez sur le nom du fichier que vous avez choisi, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **Enregistrer pour les remplacements**.</span><span class="sxs-lookup"><span data-stu-id="7f159-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Dans l’éditeur de sources, ajoutez le nom du fichier aux substitutions." lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="7f159-142">Dans l’éditeur de **sources** , ajoutez le nom du fichier aux substitutions.</span><span class="sxs-lookup"><span data-stu-id="7f159-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Dans le menu contextuel, cliquez sur Enregistrer pour les remplacements" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="7f159-144">Dans le menu contextuel, cliquez sur **Enregistrer pour les remplacements**</span><span class="sxs-lookup"><span data-stu-id="7f159-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="7f159-145">Le fichier est stocké dans votre dossier Overrides.</span><span class="sxs-lookup"><span data-stu-id="7f159-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="7f159-146">Vérifiez que DevTools crée un dossier nommé à l’aide de l’URL du fichier avec la structure de répertoires correcte.</span><span class="sxs-lookup"><span data-stu-id="7f159-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="7f159-147">Le fichier est stocké dans.</span><span class="sxs-lookup"><span data-stu-id="7f159-147">The file is stored inside.</span></span>  <span data-ttu-id="7f159-148">Le nom de fichier de l’éditeur comporte également un point violet qui indique que le fichier est local et non en cours.</span><span class="sxs-lookup"><span data-stu-id="7f159-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Le fichier a été enregistré dans le dossier de remplacements" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="7f159-150">Le fichier a été enregistré dans le dossier de remplacements</span><span class="sxs-lookup"><span data-stu-id="7f159-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="7f159-151">Dans l’exemple suivant, vous pouvez désormais modifier les styles de la page Web.</span><span class="sxs-lookup"><span data-stu-id="7f159-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="7f159-152">Pour ajouter une bordure rouge autour du fichier, dans l’éditeur de **styles** , copiez le style suivant et ajoutez-le à l’élément de corps.</span><span class="sxs-lookup"><span data-stu-id="7f159-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="7f159-153">Le fichier est enregistré automatiquement sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f159-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="7f159-154">Si vous actualisez le fichier, la bordure est affichée et aucune de vos tâches ne sera perdue.</span><span class="sxs-lookup"><span data-stu-id="7f159-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Changer les styles de pages Web de façon permanente en modifiant un fichier dans votre dossier de remplacement" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="7f159-156">Changer les styles de pages Web de façon permanente en modifiant un fichier dans votre dossier de remplacement</span><span class="sxs-lookup"><span data-stu-id="7f159-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="7f159-157">Dans l’outil **sources** , dans la section **page** , pointez sur un fichier, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et ajoutez-le à des substitutions.</span><span class="sxs-lookup"><span data-stu-id="7f159-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="7f159-158">Là encore, les fichiers qui se trouvent déjà dans votre dossier remplacements sont dotés d’un point violet sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="7f159-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Choisir un fichier à partir de l’outil sources pour les remplacements" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="7f159-160">Choisir un fichier à partir de l’outil **sources** pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="7f159-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="7f159-161">Vous pouvez également accéder à un fichier à l’aide de l’outil **réseau** , ouvrir le menu contextuel \ (cliquez avec le bouton droit sur \) et l’ajouter aux remplacements.</span><span class="sxs-lookup"><span data-stu-id="7f159-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="7f159-162">Lorsque les remplacements sont activés, les fichiers qui se trouvent sur votre ordinateur et non à partir de la page Web dynamique.</span><span class="sxs-lookup"><span data-stu-id="7f159-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="7f159-163">Lorsque les remplacements sont activés, dans l’outil **réseau** , recherchez une icône d’avertissement en regard du nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="7f159-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Choisir un fichier à partir de l’outil réseau pour les remplacements" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="7f159-165">Choisir un fichier à partir de l’outil **réseau** pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="7f159-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="7f159-166">Interaction bidirectionnelle des substitutions</span><span class="sxs-lookup"><span data-stu-id="7f159-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="7f159-167">Utilisez l’éditeur fourni avec l’outil **sources** de devtools ou un éditeur pour lequel vous voulez modifier les fichiers.</span><span class="sxs-lookup"><span data-stu-id="7f159-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="7f159-168">Les modifications sont synchronisées au sein des différents produits qui accèdent aux fichiers dans le dossier remplacements.</span><span class="sxs-lookup"><span data-stu-id="7f159-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <span data-ttu-id="7f159-169">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="7f159-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources.md "Présentation de l’outil sources | Documents Microsoft"  
