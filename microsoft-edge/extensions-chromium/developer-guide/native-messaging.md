---
description: Documentation sur la messagerie native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: d9c2370d6a4f9f7cd25001c1c58ce266423af19a
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343065"
---
# <span data-ttu-id="abb04-104">Messagerie native</span><span class="sxs-lookup"><span data-stu-id="abb04-104">Native messaging</span></span>  

<span data-ttu-id="abb04-105">Les extensions communiquent avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de transmission de message.</span><span class="sxs-lookup"><span data-stu-id="abb04-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="abb04-106">L’hôte d’application natif envoie et reçoit des messages avec des extensions à l’aide de l’entrée standard et de la sortie standard.</span><span class="sxs-lookup"><span data-stu-id="abb04-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="abb04-107">Les extensions utilisant la messagerie native sont installées dans Microsoft Edge comme n’importe quelle autre extension.</span><span class="sxs-lookup"><span data-stu-id="abb04-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="abb04-108">Toutefois, les applications natives ne sont pas installées ou gérées par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abb04-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="abb04-109">Pour acquérir l’extension et l’hôte d’application native, vous avez deux modèles de distribution.</span><span class="sxs-lookup"><span data-stu-id="abb04-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="abb04-110">Rassemblez votre extension et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="abb04-110">Package your extension and the host together.</span></span>  <span data-ttu-id="abb04-111">Lorsqu’un utilisateur installe le package, l’extension et l’hôte sont installés.</span><span class="sxs-lookup"><span data-stu-id="abb04-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="abb04-112">Installez votre extension à l’aide du [magasin de modules] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]de microsoft Edge et votre extension invite les utilisateurs à installer l’hôte.</span><span class="sxs-lookup"><span data-stu-id="abb04-112">Install your extension using the [Microsoft Edge Add-ons store] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="abb04-113">Pour créer votre extension pour envoyer et recevoir des messages avec des hôtes d’application natifs, reportez-vous aux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="abb04-114">Étape 1 : ajouter des autorisations au manifeste d’extension</span><span class="sxs-lookup"><span data-stu-id="abb04-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="abb04-115">Ajoutez `nativeMessaging` l’autorisation au **manifest.jssur le** fichier de l’extension.</span><span class="sxs-lookup"><span data-stu-id="abb04-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="abb04-116">L’extrait de code suivant est un exemple \*\* d'manifest.jssur\*\*.</span><span class="sxs-lookup"><span data-stu-id="abb04-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="abb04-117">Étape 2 : créer votre fichier manifeste d’hôte de messagerie native</span><span class="sxs-lookup"><span data-stu-id="abb04-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="abb04-118">Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="abb04-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="abb04-119">Le fichier manifeste contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="abb04-120">Chemin d’accès au runtime de l’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="abb04-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="abb04-121">Méthode de communication avec l’extension.</span><span class="sxs-lookup"><span data-stu-id="abb04-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="abb04-122">Liste des extensions autorisées avec lesquelles il communique.</span><span class="sxs-lookup"><span data-stu-id="abb04-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="abb04-123">Le navigateur lit et valide le manifeste d’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="abb04-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="abb04-124">Le navigateur n’installe pas ou ne gère pas le fichier manifeste de l’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="abb04-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="abb04-125">Le fichier manifeste hôte doit être un fichier JSON valide qui contient les clés suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="abb04-126">Spécifie le nom de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="abb04-126">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="abb04-127">Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="abb04-127">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="abb04-128">Cette valeur ne doit contenir que des caractères alphanumériques en minuscules, des traits de soulignement et des points.</span><span class="sxs-lookup"><span data-stu-id="abb04-128">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="abb04-129">Cette valeur ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point.</span><span class="sxs-lookup"><span data-stu-id="abb04-129">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="abb04-130">Décrit l’application.</span><span class="sxs-lookup"><span data-stu-id="abb04-130">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="abb04-131">Spécifie le chemin d’accès au fichier binaire hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="abb04-131">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="abb04-132">Sur les appareils Windows, vous pouvez utiliser des chemins d’accès relatifs au répertoire qui contient le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="abb04-132">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="abb04-133">Sur macOS et Linux, le chemin d’accès doit être absolu.</span><span class="sxs-lookup"><span data-stu-id="abb04-133">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="abb04-134">Le processus hôte commence par le répertoire actuel qui contient le fichier binaire hôte.</span><span class="sxs-lookup"><span data-stu-id="abb04-134">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="abb04-135">Par exemple \(Windows\), si ce paramètre est paramétrage, le fichier binaire est démarré à l’aide du répertoire `C:\Application\nm_host.exe` actuel \( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="abb04-135">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="abb04-136">Spécifie le type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="abb04-136">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="abb04-137">Cette valeur indique à Microsoft Edge d’utiliser `stdin` et de communiquer avec `stdout` l’hôte.</span><span class="sxs-lookup"><span data-stu-id="abb04-137">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="abb04-138">La seule valeur acceptable est `stdio` .</span><span class="sxs-lookup"><span data-stu-id="abb04-138">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="abb04-139">Spécifie la liste des extensions qui ont accès à l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="abb04-139">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="abb04-140">Pour permettre à votre application d’identifier et de communiquer avec une extension, dans votre fichier manifeste hôte de messagerie native, définissez la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="abb04-140">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="abb04-141">Chargez une version test de votre extension pour tester la messagerie native avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="abb04-141">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="abb04-142">Pour recharger une version de votre extension pendant le développement et `microsoft_catalog_extension_id` récupérer, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-142">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="abb04-143">Accédez à , puis activer le bouton bascule `edge://extensions` du mode développeur.</span><span class="sxs-lookup"><span data-stu-id="abb04-143">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="abb04-144">Choisissez **Charger décompressé,** puis sélectionnez votre package d’extension à charger de côté.</span><span class="sxs-lookup"><span data-stu-id="abb04-144">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="abb04-145">Choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="abb04-145">Choose **OK**.</span></span>  
1.  <span data-ttu-id="abb04-146">Accédez à `edge://extensions` la page et vérifiez que votre extension est répertoriée.</span><span class="sxs-lookup"><span data-stu-id="abb04-146">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="abb04-147">Copiez la clé à partir `microsoft_catalog_extension_id` de \(ID\) à partir de la liste des extensions sur la page.</span><span class="sxs-lookup"><span data-stu-id="abb04-147">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  

<span data-ttu-id="abb04-148">Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez-la dans le magasin de modules extensions Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abb04-148">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="abb04-149">L’ID d’extension de l’extension publiée peut différer de l’ID utilisé lors du chargement de votre extension.</span><span class="sxs-lookup"><span data-stu-id="abb04-149">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="abb04-150">Si l’ID a changé, mettez à jour dans le fichier manifeste hôte avec `allowed_origins` l’ID de votre extension publiée.</span><span class="sxs-lookup"><span data-stu-id="abb04-150">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="abb04-151">Étape 3 : copier le fichier manifeste de l’hôte de messagerie native dans votre système</span><span class="sxs-lookup"><span data-stu-id="abb04-151">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="abb04-152">La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie native sur votre ordinateur et à s’assurer que le fichier manifeste est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="abb04-152">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="abb04-153">Pour vous assurer que votre fichier manifeste est placé à l’emplacement attendu, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-153">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="abb04-154">L’emplacement varie en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="abb04-154">The location varies by platform.</span></span>  

### [<span data-ttu-id="abb04-155">Windows</span><span class="sxs-lookup"><span data-stu-id="abb04-155">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="abb04-156">Le fichier manifeste peut se trouver n’importe où dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="abb04-156">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="abb04-157">Le programme d’installation d’application doit créer une clé de Registre et définir la valeur par défaut de cette clé sur le chemin d’accès complet du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="abb04-157">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="abb04-158">Les commandes suivantes sont des exemples de clés de Registre.</span><span class="sxs-lookup"><span data-stu-id="abb04-158">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="abb04-159">Pour ajouter une clé de Registre au répertoire avec la clé de manifeste.</span><span class="sxs-lookup"><span data-stu-id="abb04-159">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="abb04-160">Exécutez la commande dans l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="abb04-160">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="abb04-161">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="abb04-161">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="abb04-162">Créez `.reg` un fichier et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="abb04-162">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="abb04-163">Copiez la commande suivante dans un `.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="abb04-163">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="abb04-164">Exécutez le `.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="abb04-164">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="abb04-165">Microsoft Edge interroge la `HKEY_CURRENT_USER` clé racine suivie de `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="abb04-165">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="abb04-166">Dans les deux clés, le Registre 32 bits est recherché en premier, puis le Registre 64 bits est recherché pour identifier les hôtes de messagerie natifs.</span><span class="sxs-lookup"><span data-stu-id="abb04-166">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="abb04-167">La clé de Registre spécifie l’emplacement du manifeste d’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="abb04-167">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="abb04-168">Si Microsoft Edge trouve la clé de Registre à l’un des emplacements répertoriés précédemment, il n’interroge pas les emplacements répertoriés dans ce paragraphe.</span><span class="sxs-lookup"><span data-stu-id="abb04-168">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in this paragraph.</span></span>  <span data-ttu-id="abb04-169">Si vous exécutez le fichier ci-dessus dans le cadre d’un script de commandes, veillez à l’exécuter à l’aide d’une `.reg` invite de commandes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="abb04-169">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="abb04-170">macOS</span><span class="sxs-lookup"><span data-stu-id="abb04-170">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="abb04-171">Pour stocker le fichier manifeste, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-171">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="abb04-172">Les hôtes de messagerie native à l’échelle du système, qui sont disponibles pour tous les utilisateurs, sont stockés dans un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="abb04-172">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="abb04-173">Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="abb04-173">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="abb04-174">Les hôtes de messagerie native spécifiques à l’utilisateur, disponibles uniquement pour l’utilisateur actuel, se trouvent dans le sous-répertoire de `NativeMessagingHosts` l’annuaire de profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abb04-174">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="abb04-175">Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="abb04-175">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="abb04-176">`{Channel_Name}` `Microsoft Edge {Channel_Name}` L’in doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-176">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="abb04-177">Canary</span><span class="sxs-lookup"><span data-stu-id="abb04-177">Canary</span></span>  
    *   <span data-ttu-id="abb04-178">Dev</span><span class="sxs-lookup"><span data-stu-id="abb04-178">Dev</span></span>  
    *   <span data-ttu-id="abb04-179">Beta</span><span class="sxs-lookup"><span data-stu-id="abb04-179">Beta</span></span>  

    <span data-ttu-id="abb04-180">Lorsque vous utilisez le canal stable, `{Channel_Name}` cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="abb04-180">When using the Stable channel, `{Channel_Name}` isn't required.</span></span>  

### [<span data-ttu-id="abb04-181">Linux</span><span class="sxs-lookup"><span data-stu-id="abb04-181">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="abb04-182">Pour stocker le fichier manifeste, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="abb04-182">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="abb04-183">Les hôtes de messagerie native à l’échelle du système, qui sont disponibles pour tous les utilisateurs, sont stockés dans un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="abb04-183">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="abb04-184">Le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="abb04-184">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="abb04-185">Les hôtes de messagerie native spécifiques à l’utilisateur, disponibles uniquement pour l’utilisateur actuel, se trouvent dans le sous-répertoire de `NativeMessagingHosts` l’annuaire de profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abb04-185">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="abb04-186">Le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="abb04-186">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="abb04-187">Veillez à fournir des autorisations de lecture sur le fichier manifeste et à exécuter les autorisations sur l’runtime hôte.</span><span class="sxs-lookup"><span data-stu-id="abb04-187">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge Add-ons"

> [!NOTE]
> <span data-ttu-id="abb04-189">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="abb04-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="abb04-190">La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="abb04-190">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="abb04-192">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="abb04-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
