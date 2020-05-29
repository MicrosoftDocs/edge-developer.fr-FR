---
description: Différence de messagerie native de la documentation chrome
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565447"
---
# <span data-ttu-id="e2b3c-104">Messagerie native</span><span class="sxs-lookup"><span data-stu-id="e2b3c-104">Native Messaging</span></span>  

<span data-ttu-id="e2b3c-105">Microsoft Edge permet désormais d’installer une extension à partir du catalogue Microsoft Edge addons (Microsoft Edge addons) pour échanger des messages avec une application native utilisant des API de passage de messages.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-105">Microsoft Edge now allows Extension installed from Microsoft Edge Addons catalog \(Microsoft Edge Addons\) to exchange messages with a native application using message passing APIs.</span></span>  <span data-ttu-id="e2b3c-106">Pour activer cette fonctionnalité, vous devez vous assurer que les éléments suivants sont implémentés lors de l’implémentation de l’hôte de messagerie natif de votre application native.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-106">To enable the feature, you need to make sure of following things while implementing native messaging host of your Native Application.</span></span>  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  <span data-ttu-id="e2b3c-107">**Hôte de messagerie natif**:</span><span class="sxs-lookup"><span data-stu-id="e2b3c-107">**Native messaging host**:</span></span>  
    
    <span data-ttu-id="e2b3c-108">Pour enregistrer un hôte de messagerie natif, l’application doit installer un fichier manifeste qui définit la configuration de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-108">In order to register a native messaging host the application must install a manifest file that defines the native messaging host configuration.</span></span>  <span data-ttu-id="e2b3c-109">Voici un exemple du fichier manifeste:</span><span class="sxs-lookup"><span data-stu-id="e2b3c-109">Below is an example of the manifest file:</span></span>  
    
    ```xml
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
    ```  
    
<span data-ttu-id="e2b3c-110">Le fichier manifeste de l’hôte de messagerie natif doit être JSON valide et contenir les champs suivants:</span><span class="sxs-lookup"><span data-stu-id="e2b3c-110">The native messaging host manifest file must be valid JSON and contains the following fields:</span></span>  

| <span data-ttu-id="e2b3c-111">Nom</span><span class="sxs-lookup"><span data-stu-id="e2b3c-111">Name</span></span> | <span data-ttu-id="e2b3c-112">Description</span><span class="sxs-lookup"><span data-stu-id="e2b3c-112">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="e2b3c-113">Nom de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-113">Name of the native messaging host.</span></span> <span data-ttu-id="e2b3c-114">Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="e2b3c-114">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="e2b3c-115">Ce nom doit uniquement contenir des caractères alphanumériques minuscules, des traits de soulignement et des points.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-115">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="e2b3c-116">Le nom ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-116">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="e2b3c-117">Brève description de l’application.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-117">Short application description.</span></span> |  
| `path` | <span data-ttu-id="e2b3c-118">Chemin d’accès au fichier binaire de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-118">Path to the native messaging host binary.</span></span>  <span data-ttu-id="e2b3c-119">Sur Windows, le chemin d’accès peut être relatif au répertoire dans lequel se trouve le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-119">On Windows, the path may be relative to the directory in which the manifest file is located.</span></span>  <span data-ttu-id="e2b3c-120">Sur macOS, le chemin d’accès doit être absolu.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-120">On macOS, the path must be absolute.</span></span>  <span data-ttu-id="e2b3c-121">Le processus hôte est démarré avec le répertoire actif défini sur le répertoire contenant le fichier binaire hôte.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-121">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="e2b3c-122">Par exemple, si ce paramètre est défini sur `C:\Application\nm_host.exe` , le fichier binaire est démarré à l’aide du répertoire actif `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="e2b3c-122">For example if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="e2b3c-123">Type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-123">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="e2b3c-124">Il n’y a actuellement qu’une seule valeur possible pour ce paramètre: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="e2b3c-124">Currently there is only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="e2b3c-125">Cette valeur indique que Chrome doit utiliser `stdin` et `stdout` communiquer avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-125">This value indicates that Chrome should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="e2b3c-126">liste d’extensions qui doivent pouvoir accéder à l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-126">list of Extension that should access to the native messaging host.</span></span>  <span data-ttu-id="e2b3c-127">Pour permettre à votre application native d’identifier et de communiquer avec l’extension Microsoft Edge addons, définissez `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` dans le fichier manifeste de votre hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-127">To enable your Native Application identify and communicate with Microsoft Edge Addons Extension, set `allowedorigins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  

1.  **<span data-ttu-id="e2b3c-128">Emplacement d’hébergement de messagerie Native</span><span class="sxs-lookup"><span data-stu-id="e2b3c-128">Native messaging host location</span></span>**  
    
    <span data-ttu-id="e2b3c-129">L’emplacement du fichier manifeste dépend de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-129">The location of the manifest file depends on the platform.</span></span>  
    
    <span data-ttu-id="e2b3c-130">Sur Windows, le fichier manifeste est disponible n’importe où dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-130">On Windows, the manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="e2b3c-131">Le programme d’installation de l’application doit créer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="e2b3c-131">The application installer must create registry key</span></span>  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="e2b3c-132">ou</span><span class="sxs-lookup"><span data-stu-id="e2b3c-132">or</span></span>  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="e2b3c-133">,</span><span class="sxs-lookup"><span data-stu-id="e2b3c-133">,</span></span>  
    
    <span data-ttu-id="e2b3c-134">Définissez la valeur par défaut de cette clé sur le chemin d’accès complet au fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-134">and set default value of that key to the full path to the manifest file.</span></span>  <span data-ttu-id="e2b3c-135">Par exemple, à l’aide de la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="e2b3c-135">For example, using the following command:</span></span>  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    <span data-ttu-id="e2b3c-136">ou en utilisant le fichier. reg suivant:</span><span class="sxs-lookup"><span data-stu-id="e2b3c-136">or using the following .reg file:</span></span>  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    <span data-ttu-id="e2b3c-137">Lorsque Microsoft Edge recherche les hôtes de messagerie natifs, le registre 32 bits est interrogé en premier, puis le registre 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-137">When Microsoft Edge looks for native messaging hosts, the 32-bit registry is queried first, then the 64-bit registry.</span></span>  

<span data-ttu-id="e2b3c-138">Sur macOS, les hôtes de messagerie natif à l’échelle du système sont examinés à un emplacement fixe, tandis que les hôtes de messagerie natifs de niveau utilisateur sont recherchés dans un sous-répertoire du répertoire de profil utilisateur appelé `NativeMessagingHosts` .</span><span class="sxs-lookup"><span data-stu-id="e2b3c-138">On macOS, the system-wide native messaging hosts are looked up at a fixed location, while the user-level native messaging hosts are looked up in a subdirectory within the user profile directory called `NativeMessagingHosts`.</span></span>  

<span data-ttu-id="e2b3c-139">Microsoft Edge sur macOS \ (système à l’échelle de la planète):</span><span class="sxs-lookup"><span data-stu-id="e2b3c-139">Microsoft Edge on macOS \(system-wide\) :</span></span>  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

<span data-ttu-id="e2b3c-140">Microsoft Edge sur macOS \ (spécifique de l’utilisateur, chemin par défaut \):</span><span class="sxs-lookup"><span data-stu-id="e2b3c-140">Microsoft Edge on macOS \(user-specific, default path\):</span></span>  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` <span data-ttu-id="e2b3c-141">Il est possible que la fonction «Canaries», «dev» ou «beta».</span><span class="sxs-lookup"><span data-stu-id="e2b3c-141">may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="e2b3c-142">Dans le cas d’un canal stable, `Microsoft Edge` il ne doit être utilisé qu' `<ChannelName`>'n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e2b3c-142">For stable channel, only `Microsoft Edge` should be used, `<ChannelName`>\` is not required.</span></span>

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="e2b3c-143">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2b3c-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e2b3c-144">La page d’origine est disponible [ici](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="e2b3c-144">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="e2b3c-146">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2b3c-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
