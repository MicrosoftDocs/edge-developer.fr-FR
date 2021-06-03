---
description: La fonctionnalité Overrides est une fonctionnalité de l’outil Sources de Microsoft Edge DevTools qui vous permet de copier des ressources de page web sur votre disque dur.  Lorsque vous actualisez la page web, DevTools ne charge pas la ressource, mais la remplace par votre copie locale.
title: Remplacer les ressources de page web avec des copies locales à l’Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 66c0686c166163f1640384d096288af0b530f135
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519435"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a><span data-ttu-id="f47de-105">Remplacer les ressources de page web avec des copies locales à l’Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f47de-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f47de-106">Parfois, vous devez essayer certains correctifs possibles pour une page web, mais vous n’avez pas accès aux fichiers sources, ou la modification de la page nécessite un processus de création lent et complexe.</span><span class="sxs-lookup"><span data-stu-id="f47de-106">Sometimes you need to try out some possible fixes for a webpage, but you don't have access to the source files, or changing the page requires a slow and complex build process.</span></span>  <span data-ttu-id="f47de-107">Vous pouvez déboguer et résoudre tous les types de problèmes dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="f47de-107">You may debug and fix all kind of problems in DevTools.</span></span>  <span data-ttu-id="f47de-108">Mais les modifications ne sont pas persistantes ; Une fois que vous avez actualisé le fichier local, tout votre travail a disparu.</span><span class="sxs-lookup"><span data-stu-id="f47de-108">But the changes do not persist; after you refresh the local file, all your work is gone.</span></span>  <span data-ttu-id="f47de-109">La fonctionnalité Remplacements de l’outil [Sources][DevToolsSourcesTool] vous aide à résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="f47de-109">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="f47de-110">Vous pouvez maintenant prendre une ressource de la page web actuelle et la stocker localement.</span><span class="sxs-lookup"><span data-stu-id="f47de-110">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="f47de-111">Lorsque vous actualisez la page web, le navigateur ne charge pas la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="f47de-111">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="f47de-112">Au lieu de cela, le navigateur le remplace par votre copie locale de la ressource.</span><span class="sxs-lookup"><span data-stu-id="f47de-112">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <a name="setting-up-your-local-folder-to-store-overrides"></a><span data-ttu-id="f47de-113">Configuration de votre dossier local pour stocker les remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-113">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="f47de-114">Accédez à **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="f47de-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="f47de-115">Dans le **volet Navigateur** (à gauche), sélectionnez **l’onglet Remplacements.**  Si **l’onglet Remplacements** n’est pas affiché, sélectionnez</span><span class="sxs-lookup"><span data-stu-id="f47de-115">In the **Navigator** pane (on the left), choose the **Overrides** tab.  If the **Overrides** tab is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="f47de-116">.</span><span class="sxs-lookup"><span data-stu-id="f47de-116">icon.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Outil Sources avec un espace insuffisant pour afficher l’option de remplacements" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="f47de-118">**Outil Sources** avec un espace insuffisant pour afficher l’option de remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-118">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Choisir l’option remplacements" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="f47de-120">Choisir l’option remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-120">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f47de-121">Choisissez un dossier sur votre ordinateur local pour stocker les fichiers de ressources à remplacer.</span><span class="sxs-lookup"><span data-stu-id="f47de-121">Choose a folder on your local computer to store the resource files that you want to replace.</span></span>  
     *   <span data-ttu-id="f47de-122">Pour rechercher un dossier, choisissez **+ Sélectionner un dossier pour les remplacements.**</span><span class="sxs-lookup"><span data-stu-id="f47de-122">To search for a folder, choose **+ Select folder for overrides**.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Choisir un dossier à utiliser pour les remplacements" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="f47de-124">Choisir un dossier à utiliser pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-124">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f47de-125">DevTools vous avertit que vous devez avoir un accès total au dossier et que vous ne devez pas révéler d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="f47de-125">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="f47de-126">Dans la barre d’avertissement, **sélectionnez Autoriser** l’accès.</span><span class="sxs-lookup"><span data-stu-id="f47de-126">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="accorder à DevTools l’accès au dossier ;" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="f47de-128">Accorder à DevTools l’accès au dossier</span><span class="sxs-lookup"><span data-stu-id="f47de-128">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f47de-129">Dans **l’onglet Remplacements,** une case à cocher s’affiche en regard de Activer les **remplacements locaux.**</span><span class="sxs-lookup"><span data-stu-id="f47de-129">In the **Overrides** tab, a checkbox is shown next to **Enable Local Overrides**.</span></span>  <span data-ttu-id="f47de-130">À droite de **l’icône Activer** les remplacements locaux, une icône de **configuration Effacer** vous permet de supprimer vos paramètres de remplacements locaux.</span><span class="sxs-lookup"><span data-stu-id="f47de-130">To the right of **Enable Local Overrides** is a **Clear configuration** icon that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="f47de-131">Vous avez maintenant terminé la configuration de votre dossier et êtes prêt à remplacer les ressources en direct par des ressources locales.</span><span class="sxs-lookup"><span data-stu-id="f47de-131">You are now done setting up your folder and are ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuration réussie d’un dossier de remplacements" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="f47de-133">Configuration réussie d’un dossier de remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-133">Successful setup of an overrides folder</span></span>  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a><span data-ttu-id="f47de-134">Ajout de fichiers à votre dossier Overrides</span><span class="sxs-lookup"><span data-stu-id="f47de-134">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="f47de-135">Pour ajouter des fichiers à votre dossier remplacements, ouvrez l’outil **Éléments** et inspectez la page web.</span><span class="sxs-lookup"><span data-stu-id="f47de-135">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="f47de-136">Pour modifier, choisissez le nom du fichier CSS dans l’inspecteur **de styles.**</span><span class="sxs-lookup"><span data-stu-id="f47de-136">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Choisir un fichier dans l’inspecteur styles" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="f47de-138">Choisir un fichier dans l’inspecteur **styles**</span><span class="sxs-lookup"><span data-stu-id="f47de-138">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f47de-139">Dans l’éditeur **sources,** pointez sur le nom de fichier de votre fichier choisi, ouvrez le menu contextuel \(clic droit\), puis choisissez Enregistrer pour **les remplacements.**</span><span class="sxs-lookup"><span data-stu-id="f47de-139">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Dans l’éditeur sources, ajoutez le nom du fichier aux remplacements" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="f47de-141">Dans **l’éditeur sources,** ajoutez le nom du fichier aux remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-141">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Dans le menu contexto, sélectionnez Enregistrer pour les remplacements" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="f47de-143">Dans le menu contexto, **sélectionnez Enregistrer pour les remplacements**</span><span class="sxs-lookup"><span data-stu-id="f47de-143">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="f47de-144">Le fichier est stocké dans votre dossier remplacements.</span><span class="sxs-lookup"><span data-stu-id="f47de-144">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="f47de-145">Vérifiez que DevTools crée un dossier nommé à l’aide de l’URL du fichier avec la structure de répertoires correcte.</span><span class="sxs-lookup"><span data-stu-id="f47de-145">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="f47de-146">Le fichier est stocké à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="f47de-146">The file is stored inside.</span></span>  <span data-ttu-id="f47de-147">Le nom du fichier dans l’éditeur affiche désormais également un point violet qui indique que le fichier est local et non en direct.</span><span class="sxs-lookup"><span data-stu-id="f47de-147">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Le fichier a été correctement stocké dans votre dossier remplacements" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="f47de-149">Le fichier a été correctement stocké dans votre dossier remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-149">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="f47de-150">Dans l’exemple suivant, vous pouvez maintenant modifier les styles de la page web.</span><span class="sxs-lookup"><span data-stu-id="f47de-150">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="f47de-151">Pour ajouter une bordure rouge autour du fichier, dans l’éditeur **styles,** copiez le style suivant et ajoutez-le à l’élément body.</span><span class="sxs-lookup"><span data-stu-id="f47de-151">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f47de-152">Le fichier est automatiquement enregistré sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f47de-152">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="f47de-153">Si vous actualisez le fichier, la bordure s’affiche et aucune partie de votre travail n’est perdue.</span><span class="sxs-lookup"><span data-stu-id="f47de-153">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Modifier les styles de page web de façon permanente en éditant un fichier dans votre dossier Remplacements" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="f47de-155">Modifier les styles de page web de façon permanente en éditant un fichier dans votre dossier Remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-155">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="f47de-156">Dans **l’outil Sources,** dans la section **Page,** pointez sur n’importe quel fichier, ouvrez le menu contextuel \(clic droit\) et ajoutez-le aux remplacements.</span><span class="sxs-lookup"><span data-stu-id="f47de-156">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="f47de-157">Là encore, les fichiers déjà dans votre dossier remplacements ont un point violet sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="f47de-157">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Choisir un fichier dans l’outil Sources pour les remplacements" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="f47de-159">Choisir un fichier dans **l’outil Sources** pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-159">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f47de-160">Vous pouvez également, sur l’outil **Réseau,** pointer sur n’importe quel fichier, ouvrir le menu contextuel \(clic droit\) et l’ajouter aux remplacements.</span><span class="sxs-lookup"><span data-stu-id="f47de-160">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="f47de-161">Lorsque les substitutions sont en vigueur, les fichiers qui se trouvent sur votre ordinateur et non à partir de la page web en direct.</span><span class="sxs-lookup"><span data-stu-id="f47de-161">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="f47de-162">Lorsque des substitutions sont en vigueur, sur l’outil **Réseau,** recherchez une icône d’avertissement en côté du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="f47de-162">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Choisir un fichier dans l’outil Réseau pour les remplacements" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="f47de-164">Choisir un fichier dans **l’outil** Réseau pour les remplacements</span><span class="sxs-lookup"><span data-stu-id="f47de-164">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a><span data-ttu-id="f47de-165">Interaction double des substitutions</span><span class="sxs-lookup"><span data-stu-id="f47de-165">Two-way interaction of overrides</span></span>  

<span data-ttu-id="f47de-166">Utilisez l’éditeur fourni avec l’outil **Sources** de DevTools ou tout éditeur pour modifier les fichiers.</span><span class="sxs-lookup"><span data-stu-id="f47de-166">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="f47de-167">Les modifications sont synchronisées entre tous les produits qui accèdent aux fichiers dans le dossier remplacements.</span><span class="sxs-lookup"><span data-stu-id="f47de-167">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f47de-168">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f47de-168">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
