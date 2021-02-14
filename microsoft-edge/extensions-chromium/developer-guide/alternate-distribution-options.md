---
description: Découvrez comment distribuer des extensions à l’aide d’autres méthodes qui n’utilisent pas de magasins vérifiés
title: Autre méthode de distribution des extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, extensions, centre de partenaires, développeur
ms.openlocfilehash: 9232b8912acaa52c8d97fdd5f13b82ec33c865d4
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327623"
---
# <span data-ttu-id="94acb-104">Autres méthodes de distribution d’extension</span><span class="sxs-lookup"><span data-stu-id="94acb-104">Alternate extension distribution methods</span></span>  

<span data-ttu-id="94acb-105">En règle générale, les extensions sont distribuées via le magasin de modules extensions Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="94acb-105">Generally, extensions are distributed through the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="94acb-106">Dans certains scénarios, les développeurs peuvent avoir besoin de distribuer des extensions à l’aide d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="94acb-106">There are some scenarios where developers may need to distribute extensions using alternate methods.</span></span> <span data-ttu-id="94acb-107">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="94acb-107">For example:</span></span>

1.  <span data-ttu-id="94acb-108">L’extension est associée à d’autres logiciels et doit être installée avec le reste du logiciel groupé.</span><span class="sxs-lookup"><span data-stu-id="94acb-108">The extension is associated with other software, and it should be installed together with the rest of the bundled software.</span></span>   
1.  <span data-ttu-id="94acb-109">Les administrateurs réseau souhaitent distribuer une extension dans toute leur organisation.</span><span class="sxs-lookup"><span data-stu-id="94acb-109">Network administrators want to distribute an extension throughout their organization.</span></span>   

<span data-ttu-id="94acb-110">Les extensions qui ne sont pas chargées à partir du magasin d’extensions Edge sont appelées extensions installées en externe.</span><span class="sxs-lookup"><span data-stu-id="94acb-110">Extensions that are not loaded from the Edge add-ons store are referred to as externally installed extensions.</span></span> <span data-ttu-id="94acb-111">La liste suivante fournit d’autres méthodes de distribution des extensions installées en externe.</span><span class="sxs-lookup"><span data-stu-id="94acb-111">The following list provides alternate methods of distributing externally installed extensions.</span></span> 

*   <span data-ttu-id="94acb-112">Utilisez le Registre Windows (Windows uniquement).</span><span class="sxs-lookup"><span data-stu-id="94acb-112">Use the Windows registry (Windows only).</span></span>  
*   <span data-ttu-id="94acb-113">Utilisez un fichier JSON de préférences (macOS et Linux).</span><span class="sxs-lookup"><span data-stu-id="94acb-113">Use a preferences JSON file (macOS and Linux).</span></span>  
    
## <span data-ttu-id="94acb-114">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="94acb-114">Before you begin</span></span>  

<span data-ttu-id="94acb-115">Veillez à publier votre extension dans le magasin de modules de microsoft Edge ou à mettre en package un fichier et assurez-vous qu’il s’installe `.crx` correctement sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="94acb-115">Ensure that you publish your extension in the Microsoft Edge Add-ons store, or package a `.crx` file and ensure that it installs successfully on your computer.</span></span>  <span data-ttu-id="94acb-116">Si vous installez le `.crx` fichier à l’aide de `update_URL` la , assurez-vous que vous pouvez accéder à votre extension à cette URL.</span><span class="sxs-lookup"><span data-stu-id="94acb-116">If you install the `.crx` file using the `update_URL`, ensure you can navigate to your extension at that URL.</span></span>  

<span data-ttu-id="94acb-117">Assurez-vous également que vous avez les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="94acb-117">Also, ensure that you have the following information.</span></span>    

1.  <span data-ttu-id="94acb-118">Chemin d’accès du `.crx` fichier ou de votre `update_URL` extension.</span><span class="sxs-lookup"><span data-stu-id="94acb-118">The file path of the `.crx` file, or the `update_URL` of your extension.</span></span>
1.  <span data-ttu-id="94acb-119">Version de votre extension.</span><span class="sxs-lookup"><span data-stu-id="94acb-119">The version of your extension.</span></span>  <span data-ttu-id="94acb-120">Les informations de version sont disponibles dans votre fichier manifeste ou dans Microsoft Edge après le chargement de `edge://extensions` l’extension packaisée.</span><span class="sxs-lookup"><span data-stu-id="94acb-120">The version information is available in your manifest file, or in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>   
1.  <span data-ttu-id="94acb-121">ID de votre extension.</span><span class="sxs-lookup"><span data-stu-id="94acb-121">The ID of your extension.</span></span>  <span data-ttu-id="94acb-122">Les informations d’ID sont disponibles dans Microsoft Edge après le chargement `edge://extensions` de l’extension packée.</span><span class="sxs-lookup"><span data-stu-id="94acb-122">The ID information is available in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>  

> [!NOTE] 
> <span data-ttu-id="94acb-123">Les exemples `1.0` suivants utilisent la version et `aaaaaaaaaabbbbbbbbbbcccccccccc` l’ID.</span><span class="sxs-lookup"><span data-stu-id="94acb-123">The following examples use `1.0` as the version, and `aaaaaaaaaabbbbbbbbbbcccccccccc` for the ID.</span></span>  

## <span data-ttu-id="94acb-124">Utiliser le Registre Windows (Windows uniquement)</span><span class="sxs-lookup"><span data-stu-id="94acb-124">Use the Windows registry (Windows only)</span></span>  

<span data-ttu-id="94acb-125">Pour distribuer votre extension à l’aide du Registre Windows, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="94acb-125">To distribute your extension using the Windows registry, perform the following steps.</span></span>

1.  <span data-ttu-id="94acb-126">Recherchez ou créez la clé suivante dans le Registre :</span><span class="sxs-lookup"><span data-stu-id="94acb-126">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="94acb-127">Windows 32 bits  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` : .</span><span class="sxs-lookup"><span data-stu-id="94acb-127">32-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`.</span></span>  
    *   <span data-ttu-id="94acb-128">Windows 64 bits  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` : .</span><span class="sxs-lookup"><span data-stu-id="94acb-128">64-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`.</span></span>  
1.  <span data-ttu-id="94acb-129">Créez une clé ou un dossier sous **Extensions** avec le même nom que l’ID de votre extension.</span><span class="sxs-lookup"><span data-stu-id="94acb-129">Create a new key, or folder, under **Extensions** with the same name as the ID of your extension.</span></span> <span data-ttu-id="94acb-130">Par exemple, créez la clé avec le nom `aaaaaaaaaabbbbbbbbbbcccccccccc` .</span><span class="sxs-lookup"><span data-stu-id="94acb-130">For example, create the key with the name `aaaaaaaaaabbbbbbbbbbcccccccccc`.</span></span>  
1.  <span data-ttu-id="94acb-131">Dans la **clé Extensions,** créez `update_url` la propriété et définissez la valeur sur `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="94acb-131">In the **Extensions** key, create the `update_url` property, and set the value to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="94acb-132">La propriété pointe vers le fichier de votre extension dans le magasin de `update_url` `.crx` modules supplémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="94acb-132">The `update_url` property points to the `.crx` file of your extension in the Microsoft Edge Add-ons store.</span></span>  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="94acb-133">Si vous souhaitez installer une extension à partir du Chrome Web Store, définissez la valeur `update_url` sur `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="94acb-133">If you want to install an extension from the Chrome Web Store, set the value of `update_url` to `https://clients2.google.com/service/update2/crx`.</span></span>  
  
1.  <span data-ttu-id="94acb-134">Vérifiez que votre extension est répertoriée dans Microsoft Edge en naviguant vers `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="94acb-134">Verify that your extension is listed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="94acb-135">Utiliser un fichier JSON de préférences (macOS et Linux)</span><span class="sxs-lookup"><span data-stu-id="94acb-135">Use a preferences JSON file (macOS and Linux)</span></span>  

<span data-ttu-id="94acb-136">Pour distribuer votre extension à l’aide d’un fichier JSON de préférences, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="94acb-136">To distribute your extension using a preferences JSON file, perform the following steps.</span></span>

1.  <span data-ttu-id="94acb-137">Lorsque vous utilisez Linux, assurez-vous que votre fichier d’extension est disponible sur l’ordinateur sur qui `.crx` l’extension sera installée.</span><span class="sxs-lookup"><span data-stu-id="94acb-137">When using Linux, ensure your `.crx` extension file is available on the machine that the extension will be installed on.</span></span> <span data-ttu-id="94acb-138">Copiez le fichier d’extension dans un répertoire local ou utilisez un partage réseau `.crx` accessible à partir de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="94acb-138">Copy the `.crx` extension file to a local directory, or use a  network share that is reachable from the machine.</span></span> 
1.  <span data-ttu-id="94acb-139">Créez un fichier JSON dans lequel le nom du fichier correspond à l’ID de votre extension.</span><span class="sxs-lookup"><span data-stu-id="94acb-139">Create a JSON file where the name of the file corresponds to the ID of your extension.</span></span> <span data-ttu-id="94acb-140">Par exemple, créez un fichier JSON avec le nom de fichier `aaaaaaaaaabbbbbbbbbbcccccccccc.json` .</span><span class="sxs-lookup"><span data-stu-id="94acb-140">For example, create a JSON file with the file name `aaaaaaaaaabbbbbbbbbbcccccccccc.json`.</span></span>  
1.  <span data-ttu-id="94acb-141">Selon votre système d’exploitation, enregistrez le fichier JSON dans l’un des dossiers suivants.</span><span class="sxs-lookup"><span data-stu-id="94acb-141">Depending on your operating system, save the JSON file to one of the following folders.</span></span>   
    *   **<span data-ttu-id="94acb-142">macOS</span><span class="sxs-lookup"><span data-stu-id="94acb-142">macOS</span></span>**  
        *   <span data-ttu-id="94acb-143">Spécifiques à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="94acb-143">User specific:</span></span> `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   <span data-ttu-id="94acb-144">Tous les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="94acb-144">All users:</span></span> `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        <span data-ttu-id="94acb-145">Pour empêcher les utilisateurs non autorisés d’installer des extensions pour tous les utilisateurs, assurez-vous que votre fichier d’extension est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="94acb-145">To prevent unauthorized users from installing extensions for all users, ensure your extension file is read only.</span></span> <span data-ttu-id="94acb-146">En outre, assurez-vous que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="94acb-146">Additionally, ensure that the following conditions are met:</span></span>
        
        *   <span data-ttu-id="94acb-147">Chaque répertoire du chemin d’accès appartient à la racine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="94acb-147">Every directory in the path is owned by the user root.</span></span>  
        *   <span data-ttu-id="94acb-148">Chaque répertoire du chemin d’accès est affecté au `admin` ou au `wheel` groupe.</span><span class="sxs-lookup"><span data-stu-id="94acb-148">Every directory in the path is assigned to the `admin` or `wheel` group.</span></span>  
        *   <span data-ttu-id="94acb-149">Tous les répertoires du chemin d’accès ne sont pas accessibles en création.</span><span class="sxs-lookup"><span data-stu-id="94acb-149">Every directory in the path isn't world writable.</span></span>  
        *   <span data-ttu-id="94acb-150">Le chemin d’accès doit également être exempt de liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="94acb-150">The path must also be free of symbolic links.</span></span>  
        
    *   **<span data-ttu-id="94acb-151">Linux</span><span class="sxs-lookup"><span data-stu-id="94acb-151">Linux</span></span>**  
        *   <span data-ttu-id="94acb-152">Spécifiques à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="94acb-152">User specific:</span></span> `~/.config/microsoft-edge/External Extensions/`  
        *   <span data-ttu-id="94acb-153">Tous les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="94acb-153">All users:</span></span> `/usr/share/microsoft-edge/extensions/`  
1.  <span data-ttu-id="94acb-154">Selon votre scénario, copiez le code approprié qui suit dans votre fichier JSON.</span><span class="sxs-lookup"><span data-stu-id="94acb-154">Depending on your scenario, copy the appropriate code that follows to your JSON file.</span></span> 
    *   <span data-ttu-id="94acb-155">S’applique uniquement à Linux.</span><span class="sxs-lookup"><span data-stu-id="94acb-155">Applies to Linux only.</span></span> <span data-ttu-id="94acb-156">Si vous installez à partir d’un fichier, spécifiez l’emplacement et la version à `external_crx` l’aide et `external_version` .</span><span class="sxs-lookup"><span data-stu-id="94acb-156">If you install from a file, specify the location and version using `external_crx` and `external_version`.</span></span>  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   <span data-ttu-id="94acb-157">S’applique à macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="94acb-157">Applies to macOS and Linux.</span></span> <span data-ttu-id="94acb-158">Si vous installez à partir `update_URL` d’un , spécifiez l’URL de mise à jour à l’aide `external_update_url` .</span><span class="sxs-lookup"><span data-stu-id="94acb-158">If you install from an `update_URL`, specify the update URL using `external_update_url`.</span></span> 
        
        <span data-ttu-id="94acb-159">Copiez le code suivant dans votre fichier JSON lors de l’installation à partir de fichiers locaux `.crx` sur Linux uniquement.</span><span class="sxs-lookup"><span data-stu-id="94acb-159">Copy the following code to your JSON file when installing from local `.crx` files on Linux only.</span></span>  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  <span data-ttu-id="94acb-160">Copiez le code suivant dans votre fichier JSON lors de l’installation à partir du magasin de modules de microsoft Edge sur macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="94acb-160">Copy the following code to your JSON file when installing from the Microsoft Edge add-ons store on macOS and Linux.</span></span>
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  <span data-ttu-id="94acb-161">Pour installer des extensions pour des paramètres régionaux spécifiques, listez les paramètres régionaux pris en charge à l’aide `supported_locale` de .</span><span class="sxs-lookup"><span data-stu-id="94acb-161">To install extensions for specific locales, list the supported locales using `supported_locale`.</span></span>  <span data-ttu-id="94acb-162">Vous pouvez également spécifier des paramètres régionaux parents pour installer votre extension pour tous les paramètres régionaux de langue qui utilisent ce parent.</span><span class="sxs-lookup"><span data-stu-id="94acb-162">You may also specify parent locales to install your extension for all language locales that use that parent.</span></span> <span data-ttu-id="94acb-163">Par exemple, lorsque vous utilisez les paramètres régionaux parents, votre extension s’installe pour tous les paramètres régionaux anglais, tels `en` que , et ainsi de `en-US` `en-GB` suite.</span><span class="sxs-lookup"><span data-stu-id="94acb-163">For example, when using the parent locale `en`, your extension installs for all English locales, such as `en-US`, `en-GB`, and so on.</span></span>  <span data-ttu-id="94acb-164">Lorsque les utilisateurs modifient leurs paramètres régionaux dans leur navigateur, les extensions installées en externe sont désinstallées.</span><span class="sxs-lookup"><span data-stu-id="94acb-164">When users change their locale in their browser, externally installed extensions are uninstalled.</span></span>  <span data-ttu-id="94acb-165">Pour installer votre extension pour tous les paramètres régionaux, n’utilisez pas `supported_locales` .</span><span class="sxs-lookup"><span data-stu-id="94acb-165">To install your extension for any locale, do not use `supported_locales`.</span></span>  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  <span data-ttu-id="94acb-166">Vérifiez que votre extension est installée dans Microsoft Edge en naviguant vers `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="94acb-166">Verify that your extension is installed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="94acb-167">Mettre à jour et désinstaller les extensions installées en externe</span><span class="sxs-lookup"><span data-stu-id="94acb-167">Update and uninstall externally installed extensions</span></span>

<span data-ttu-id="94acb-168">Microsoft Edge analyse les entrées de métadonnées dans le Registre chaque fois que le navigateur démarre et modifie les extensions installées en externe.</span><span class="sxs-lookup"><span data-stu-id="94acb-168">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any changes to the externally installed extensions.</span></span>  

<span data-ttu-id="94acb-169">Pour mettre à jour votre extension vers une nouvelle version, mettez à jour la version dans le fichier manifeste, puis mettez à jour la version dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="94acb-169">To update your extension to a new version, update the version in the manifest file, and then update the version in the registry.</span></span>  

<span data-ttu-id="94acb-170">Vous devrez peut-être désinstaller les extensions installées en externe, qui ont été installées dans le cadre d’un ensemble de logiciels précédemment installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="94acb-170">You may need to uninstall externally installed extensions, which were installed as part of a bundle of software that was previously installed on the machine.</span></span>  <span data-ttu-id="94acb-171">Pour désinstaller votre extension, supprimez votre fichier JSON de préférences ou supprimez la clé du Registre.</span><span class="sxs-lookup"><span data-stu-id="94acb-171">To uninstall your extension, remove your preferences JSON file or remove the key from the registry.</span></span>   

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="94acb-172">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="94acb-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  <span data-ttu-id="94acb-173">La page d’origine se trouve [ici.](https://developer.chrome.com/apps/external_extensions)</span><span class="sxs-lookup"><span data-stu-id="94acb-173">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="94acb-175">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="94acb-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
