---
description: Documentation de messagerie Native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088554"
---
# <span data-ttu-id="1c58e-104">Messagerie native</span><span class="sxs-lookup"><span data-stu-id="1c58e-104">Native messaging</span></span>  

<span data-ttu-id="1c58e-105">Les extensions peuvent communiquer avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de passage de messages.</span><span class="sxs-lookup"><span data-stu-id="1c58e-105">Extensions can communicate with a native Win32 application installed on a user’s device using message passing APIs.</span></span> <span data-ttu-id="1c58e-106">L’hôte d’application natif peut envoyer et recevoir des messages avec des extensions à l’aide d’entrées standard et d’une sortie standard.</span><span class="sxs-lookup"><span data-stu-id="1c58e-106">The native application host can send and receive messages with extensions using standard input and standard output.</span></span> <span data-ttu-id="1c58e-107">Les extensions utilisant la messagerie Native sont installées dans Microsoft Edge de la même façon que dans n’importe quelle autre extension.</span><span class="sxs-lookup"><span data-stu-id="1c58e-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span> <span data-ttu-id="1c58e-108">Toutefois, les applications natives ne sont pas installées ni gérées par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1c58e-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>

<span data-ttu-id="1c58e-109">Pour acquérir l’extension et l’hôte de l’application native, vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="1c58e-109">To acquire the extension and native application host, you can:</span></span>

1. <span data-ttu-id="1c58e-110">Empaquetez l’extension et l’hôte ensemble.</span><span class="sxs-lookup"><span data-stu-id="1c58e-110">Package the extension and the host together.</span></span> <span data-ttu-id="1c58e-111">Quand les utilisateurs installent le package, l’extension et l’hôte sont installés.</span><span class="sxs-lookup"><span data-stu-id="1c58e-111">When users install the package, both the extension and the host are installed.</span></span>
1. <span data-ttu-id="1c58e-112">Installez l’extension à partir du [magasin de modules complémentaires Microsoft Edge][EdgeAddons]et demandez aux utilisateurs d’installer l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1c58e-112">Install the extension from the [Microsoft Edge Add-ons store][EdgeAddons], and have your extension prompt users to install the host.</span></span> 

<span data-ttu-id="1c58e-113">Reportez-vous aux étapes ci-dessous pour configurer votre extension pour envoyer et recevoir des messages avec des hôtes d’application natifs.</span><span class="sxs-lookup"><span data-stu-id="1c58e-113">Refer to the steps below to setup your extension to send and receive messages with native application hosts.</span></span>

### <span data-ttu-id="1c58e-114">Étape 1: ajouter des autorisations au manifeste de l’extension</span><span class="sxs-lookup"><span data-stu-id="1c58e-114">Step 1: Add permissions to the extension manifest</span></span>

<span data-ttu-id="1c58e-115">Ajoutez l’autorisation nativeMessaging sur le fichier **manifest.js** de l’extension.</span><span class="sxs-lookup"><span data-stu-id="1c58e-115">Add the nativeMessaging permission to the extension’s **manifest.json** file.</span></span> <span data-ttu-id="1c58e-116">Vous trouverez ci-dessous un exemple de manifest.jssur:</span><span class="sxs-lookup"><span data-stu-id="1c58e-116">Below is an example of manifest.json:</span></span>

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```

### <span data-ttu-id="1c58e-117">Étape 2: créer le fichier de manifeste de votre hôte de messagerie natif</span><span class="sxs-lookup"><span data-stu-id="1c58e-117">Step 2: Create your native messaging host manifest file</span></span>
    
<span data-ttu-id="1c58e-118">Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="1c58e-118">Native applications must provide a native messaging host manifest file.</span></span> <span data-ttu-id="1c58e-119">Ce fichier manifeste contient le chemin d’accès au fichier exécutable de l’hôte de messagerie natif, la méthode de communication avec l’extension et la liste des extensions autorisées avec lesquelles il peut communiquer.</span><span class="sxs-lookup"><span data-stu-id="1c58e-119">This manifest file contains the path to the native messaging host executable, the method of communication with the extension, and a list of allowed extensions it can communicate with.</span></span> <span data-ttu-id="1c58e-120">Le navigateur lit et valide le manifeste de l’hôte de messagerie natif, mais n’est jamais installé ou géré par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="1c58e-120">Browsers read and validate the native messaging host manifest, but it’s never installed or managed by the browser.</span></span> <span data-ttu-id="1c58e-121">Le fichier de manifeste hôte doit être un fichier JSON valide contenant les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="1c58e-121">The host manifest file must be a valid json file containing the following fields.</span></span>

    
```json
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




| <span data-ttu-id="1c58e-122">Nom</span><span class="sxs-lookup"><span data-stu-id="1c58e-122">Name</span></span> | <span data-ttu-id="1c58e-123">Description</span><span class="sxs-lookup"><span data-stu-id="1c58e-123">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="1c58e-124">Nom de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="1c58e-124">Name of the native messaging host.</span></span> <span data-ttu-id="1c58e-125">Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="1c58e-125">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="1c58e-126">Ce nom doit uniquement contenir des caractères alphanumériques minuscules, des traits de soulignement et des points.</span><span class="sxs-lookup"><span data-stu-id="1c58e-126">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="1c58e-127">Le nom ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point.</span><span class="sxs-lookup"><span data-stu-id="1c58e-127">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="1c58e-128">Brève description de l’application.</span><span class="sxs-lookup"><span data-stu-id="1c58e-128">Brief description of the application.</span></span> |  
| `path` | <span data-ttu-id="1c58e-129">Chemin d’accès au fichier binaire de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="1c58e-129">Path to the native messaging host binary.</span></span> <span data-ttu-id="1c58e-130">Sur les appareils Windows, vous pouvez utiliser des chemins d’accès relatifs à l’annuaire qui contient le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="1c58e-130">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span> <span data-ttu-id="1c58e-131">Sur macOS et Linux, le chemin d’accès doit être absolu.</span><span class="sxs-lookup"><span data-stu-id="1c58e-131">On macOS and Linux, the path must be absolute.</span></span> <span data-ttu-id="1c58e-132">Le processus hôte est démarré avec le répertoire actif défini sur le répertoire contenant le fichier binaire hôte.</span><span class="sxs-lookup"><span data-stu-id="1c58e-132">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="1c58e-133">Par exemple, si ce paramètre est défini sur `C:\Application\nm_host.exe` , le fichier binaire est démarré à l’aide du répertoire actif `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="1c58e-133">For example, if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="1c58e-134">Type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="1c58e-134">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="1c58e-135">Il n’y a actuellement qu’une seule valeur possible pour ce paramètre: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="1c58e-135">Currently there's only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="1c58e-136">Cette valeur indique que Microsoft Edge doit utiliser `stdin` et `stdout` communiquer avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1c58e-136">This value indicates that Microsoft Edge should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="1c58e-137">Liste des extensions susceptibles d’avoir accès à l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="1c58e-137">List of extensions that may have access to the native messaging host.</span></span>  <span data-ttu-id="1c58e-138">Pour permettre à votre application d’identifier et de communiquer avec une extension, définissez `allowed_origins` `chrome-extension://[Microsoft-Catalog-extensionID]` dans le fichier manifeste de votre hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="1c58e-138">To enable your application to identify and communicate with an extension, set `allowed_origins` to `chrome-extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  


<span data-ttu-id="1c58e-139">Pendant le développement, vous pouvez charger votre extension pour tester la messagerie native avec l’hôte:</span><span class="sxs-lookup"><span data-stu-id="1c58e-139">While developing, you can sideload your extension to test native messaging with the host by:</span></span>
1. <span data-ttu-id="1c58e-140">Accédez à `edge://extensions` , puis activez le bouton bascule mode développeur.</span><span class="sxs-lookup"><span data-stu-id="1c58e-140">Navigating to `edge://extensions`, and then turning on the Developer mode toggle button.</span></span> 
1. <span data-ttu-id="1c58e-141">Sélectionnez charger le fichier non emballé, puis sélectionnez votre package d’extension pour charger.</span><span class="sxs-lookup"><span data-stu-id="1c58e-141">Choose Load unpacked, and then select your extension package to sideload.</span></span>  
1. <span data-ttu-id="1c58e-142">Choisissez OK.</span><span class="sxs-lookup"><span data-stu-id="1c58e-142">Choose OK.</span></span>
1. <span data-ttu-id="1c58e-143">Vérifiez que la `edge://extensions` page affiche désormais votre extension.</span><span class="sxs-lookup"><span data-stu-id="1c58e-143">Verify the `edge://extensions` page now lists your extension.</span></span> 
1. <span data-ttu-id="1c58e-144">Copiez la clé à partir de l’ID de la liste d’extensions sur la page.</span><span class="sxs-lookup"><span data-stu-id="1c58e-144">Copy the key from ID from the extension listing on the page.</span></span>

<span data-ttu-id="1c58e-145">Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez votre extension sur le magasin des modules complémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1c58e-145">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="1c58e-146">L’ID de l’extension publiée doit être différent de l’ID utilisé lors de la chargement indépendant votre extension.</span><span class="sxs-lookup"><span data-stu-id="1c58e-146">The extension ID of the published extension may be different to the ID used while sideloading your extension.</span></span> <span data-ttu-id="1c58e-147">Si l’ID a changé, mettez à jour `allowed_origins` le fichier de manifeste hôte avec l’ID de votre extension publiée.</span><span class="sxs-lookup"><span data-stu-id="1c58e-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span> 



### <span data-ttu-id="1c58e-148">Étape 3: copier le fichier manifeste de l’hôte de messagerie natif sur votre système</span><span class="sxs-lookup"><span data-stu-id="1c58e-148">Step 3: Copy the native messaging host manifest file to your system</span></span>

<span data-ttu-id="1c58e-149">La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie natif sur votre ordinateur et à vérifier qu’il est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="1c58e-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it’s configured correctly.</span></span> <span data-ttu-id="1c58e-150">Suivez les étapes ci-dessous pour vous assurer que le fichier hôte de messagerie natif est placé à l’emplacement attendu, car il varie en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="1c58e-150">Follow the steps below to ensure the native messaging host file is placed in the expected location because it varies by platform.</span></span>
    
<span data-ttu-id="1c58e-151">**Windows**.</span><span class="sxs-lookup"><span data-stu-id="1c58e-151">**Windows**.</span></span> <span data-ttu-id="1c58e-152">Le fichier manifeste est disponible n’importe où dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1c58e-152">The manifest file may be located anywhere in the file system.</span></span> <span data-ttu-id="1c58e-153">Le programme d’installation de l’application doit créer une clé de Registre et définir la valeur par défaut de cette clé sur le chemin d’accès complet du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="1c58e-153">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span> <span data-ttu-id="1c58e-154">Les commandes suivantes sont des exemples de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="1c58e-154">The following commands are examples of registry keys.</span></span>
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="1c58e-155">ou</span><span class="sxs-lookup"><span data-stu-id="1c58e-155">or</span></span>  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="1c58e-156">,</span><span class="sxs-lookup"><span data-stu-id="1c58e-156">,</span></span>  
    
<span data-ttu-id="1c58e-157">Exécutez la commande suivante à l’invite de commandes pour ajouter une clé de Registre dans le dossier contenant le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="1c58e-157">Run the following command at a command prompt to add a registry key to the folder with the manifest file.</span></span>
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
<span data-ttu-id="1c58e-158">Vous pouvez également copier la commande suivante dans un fichier. reg et l’exécuter pour ajouter la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="1c58e-158">Alternatively, copy the following command to a .reg file and run it to add the registry key.</span></span> 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  <span data-ttu-id="1c58e-159">Microsoft Edge interroge d’abord le registre 32, puis le registre 64 bits pour identifier les hôtes de messagerie natifs.</span><span class="sxs-lookup"><span data-stu-id="1c58e-159">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span> <span data-ttu-id="1c58e-160">Si vous exécutez le fichier. reg ci-dessus dans le cadre d’un script de commandes, assurez-vous de l’exécuter à l’aide d’une invite de commandes administrateur.</span><span class="sxs-lookup"><span data-stu-id="1c58e-160">If you run the above .reg file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>


<span data-ttu-id="1c58e-161">**MacOS**.</span><span class="sxs-lookup"><span data-stu-id="1c58e-161">**macOS**.</span></span> <span data-ttu-id="1c58e-162">Le fichier manifeste doit être stocké comme suit:</span><span class="sxs-lookup"><span data-stu-id="1c58e-162">The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="1c58e-163">Les hôtes de messagerie natif au niveau du système, qui sont disponibles pour tous les utilisateurs, sont stockés à un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="1c58e-163">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span> <span data-ttu-id="1c58e-164">Par exemple, le fichier manifeste doit être stocké dans</span><span class="sxs-lookup"><span data-stu-id="1c58e-164">For example, the manifest file must be stored in</span></span> `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. <span data-ttu-id="1c58e-165">Les hôtes de messagerie natif spécifiques à l’utilisateur, qui sont disponibles uniquement pour l’utilisateur actuel, sont situés dans le sous-répertoire NativeMessagingHosts dans le répertoire du profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c58e-165">User-specific native messaging hosts, which are available to the current user only, are located in the NativeMessagingHosts  subdirectory in the user profile directory.</span></span> <span data-ttu-id="1c58e-166">Par exemple, le fichier manifeste doit être stocké dans</span><span class="sxs-lookup"><span data-stu-id="1c58e-166">For example, the manifest file must be stored in</span></span>  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    <span data-ttu-id="1c58e-167">où `ChannelName` il est possible que la fonction Canaries, dev ou beta.</span><span class="sxs-lookup"><span data-stu-id="1c58e-167">where `ChannelName` may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="1c58e-168">N’est pas nécessaire lors de l’utilisation du canal stable `ChannelName` .</span><span class="sxs-lookup"><span data-stu-id="1c58e-168">When using the Stable channel, `ChannelName` isn't required.</span></span>


<span data-ttu-id="1c58e-169">**Linux** Le fichier manifeste doit être stocké comme suit:</span><span class="sxs-lookup"><span data-stu-id="1c58e-169">**Linux** The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="1c58e-170">Hôtes de messagerie native à l’échelle du système:  `~/.config/microsoft-edge/NativeMessagingHosts`</span><span class="sxs-lookup"><span data-stu-id="1c58e-170">System-wide native messaging hosts:  `~/.config/microsoft-edge/NativeMessagingHosts`</span></span>

1. <span data-ttu-id="1c58e-171">Hôtes de messagerie Native spécifiques de l’utilisateur:  `/etc/opt/edge/native-messaging-hosts`</span><span class="sxs-lookup"><span data-stu-id="1c58e-171">User-specific native messaging hosts:  `/etc/opt/edge/native-messaging-hosts`</span></span>


> [!NOTE]
> <span data-ttu-id="1c58e-172">Vérifiez que vous fournissez des autorisations de lecture sur le fichier manifeste et des autorisations d’exécution sur le fichier exécutable de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1c58e-172">Ensure that you provide read permissions on the manifest file, and execute permissions on the host executable.</span></span>


> [!NOTE]
> <span data-ttu-id="1c58e-173">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c58e-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1c58e-174">La page d’origine est disponible [ici](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="1c58e-174">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="1c58e-176">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c58e-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Modules complémentaires Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
