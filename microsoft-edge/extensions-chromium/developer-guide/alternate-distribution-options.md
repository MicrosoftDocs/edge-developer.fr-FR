---
description: Processus de distribution de l’extension par un mécanisme autre que les magasins validés
title: Autre méthode de distribution de l’extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: a1a3ffe7a54f96df7e665ab5dc6f5b99bacb8b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565451"
---
# <span data-ttu-id="68247-104">Autre méthode de distribution de l’extension</span><span class="sxs-lookup"><span data-stu-id="68247-104">Alternate Method of Distributing Extension</span></span>  

<span data-ttu-id="68247-105">Si vous êtes un développeur qui veut distribuer une extension dans le cadre de la procédure d’installation d’autres logiciels ou d’un administrateur réseau qui souhaite distribuer une extension dans toute l’organisation, Microsoft Edge prend en charge les méthodes d’installation d’extension suivantes:</span><span class="sxs-lookup"><span data-stu-id="68247-105">If you are a developer who wants to distribute an Extension as part of the installation process for other software, or a network admin that want to distribute an Extension throughout their organization, Microsoft Edge supports the following Extension installation methods:</span></span>  

*   **<span data-ttu-id="68247-106">Utilisation du Registre Windows (Windows uniquement)</span><span class="sxs-lookup"><span data-stu-id="68247-106">Using the Windows registry \(Windows only\)</span></span>**  

<span data-ttu-id="68247-107">Microsoft Edge prend en charge l’installation d’une extension hébergée sur une extension `update_URL` .</span><span class="sxs-lookup"><span data-stu-id="68247-107">Microsoft Edge supports installing an Extension hosted at an `update_URL`.</span></span>  <span data-ttu-id="68247-108">Sous Windows, le `update_URL` doit pointer sur le catalogue des compléments Microsoft Edge (Microsoft Edge addons \) sur lequel l’extension doit être hébergée.</span><span class="sxs-lookup"><span data-stu-id="68247-108">On Windows, the `update_URL` must point to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\) where the Extension must be hosted.</span></span>  

> [!NOTE]
> <span data-ttu-id="68247-109">Installation externe de l’extension par le biais d’un fichier JSON préférences pour macOS</span><span class="sxs-lookup"><span data-stu-id="68247-109">External installation of Extension via a preferences json file for macOS</span></span> <!--and Linux--> <span data-ttu-id="68247-110">ne sont pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="68247-110">are not supported yet.</span></span>  <span data-ttu-id="68247-111">Cette prise en charge de cette fonctionnalité sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="68247-111">This feature support will soon be available.</span></span>

## <span data-ttu-id="68247-112">Utilisation du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="68247-112">Using the Windows registry</span></span>  

<span data-ttu-id="68247-113">Tout d’abord, publiez l’extension dans les modules complémentaires Microsoft Edge ou emportez un fichier. CRX et assurez-vous que le programme s’installe correctement.</span><span class="sxs-lookup"><span data-stu-id="68247-113">First, publish the Extension in the Microsoft Edge Addons, or package a .crx file and make sure that it installs successfully.</span></span>  

<span data-ttu-id="68247-114">Les étapes à suivre pour installer une extension via le registre dans Windows sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="68247-114">The steps to install Extension via registry in windows are:</span></span>  

*   <span data-ttu-id="68247-115">Recherchez ou créez la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="68247-115">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="68247-116">Windows 32 bits:</span><span class="sxs-lookup"><span data-stu-id="68247-116">32-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   <span data-ttu-id="68247-117">Windows 64 bits:</span><span class="sxs-lookup"><span data-stu-id="68247-117">64-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   <span data-ttu-id="68247-118">Créez une nouvelle clé \ (dossier \) sous la clé extensions avec le même nom que l’ID de votre extension \ (par exemple, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).</span><span class="sxs-lookup"><span data-stu-id="68247-118">Create a new key \(folder\) under the Extensions key with the same name as the ID of your Extension \(for example, `aaaaaaaaaabbbbbbbbbbcccccccccc`\).</span></span>  
*   <span data-ttu-id="68247-119">Dans votre clé d’extension, créez une propriété, `update_url` et définissez-la sur la valeur: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (cela pointe vers le CRX de votre extension dans les compléments Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="68247-119">In your Extension key, create a property, `update_url`, and set it to the value: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`,  \(this points to the crx of your extension in the Microsoft Edge Addons\).</span></span> <span data-ttu-id="68247-120">Si vous voulez installer une extension à partir du Web Store chrome, spécifiez l’URL de mise à jour du Web Store chrome `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="68247-120">If you want to install an extension from the Chrome Web Store, please provide the Chrome Web Store update URL, `https://clients2.google.com/service/update2/crx`.</span></span>  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   <span data-ttu-id="68247-121">Lancez le navigateur et accédez à `edge://extensions` ; l’extension doit apparaître dans la liste.</span><span class="sxs-lookup"><span data-stu-id="68247-121">Launch the browser and go to `edge://extensions`; you should see the extension listed.</span></span>  

## <span data-ttu-id="68247-122">Mise à jour et désinstallation</span><span class="sxs-lookup"><span data-stu-id="68247-122">Updating and uninstalling</span></span>  

<span data-ttu-id="68247-123">Microsoft Edge analyse les entrées de métadonnées du Registre chaque fois que le navigateur démarre, puis apporte les modifications nécessaires aux extensions externes installées.</span><span class="sxs-lookup"><span data-stu-id="68247-123">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any necessary changes to the installed external extensions.</span></span>  

<span data-ttu-id="68247-124">Pour mettre à jour votre extension vers une nouvelle version, mettez à jour le fichier, puis mettez à jour la version dans le registre.</span><span class="sxs-lookup"><span data-stu-id="68247-124">To update your extension to a new version, update the file, and then update the version in the registry.</span></span>  

<span data-ttu-id="68247-125">Pour désinstaller votre extension (par exemple, si votre logiciel est désinstallé), supprimez votre fichier de préférences \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) ou les métadonnées du Registre.</span><span class="sxs-lookup"><span data-stu-id="68247-125">To uninstall your extension \(for example, if your software is uninstalled\), remove your preference file \(`aaaaaaaaaabbbbbbbbbbcccccccccc.json`\) or the metadata from the registry.</span></span>  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="68247-126">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68247-126">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="68247-127">La page d’origine est disponible [ici](https://developer.chrome.com/apps/external_extensions).</span><span class="sxs-lookup"><span data-stu-id="68247-127">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="68247-129">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68247-129">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
