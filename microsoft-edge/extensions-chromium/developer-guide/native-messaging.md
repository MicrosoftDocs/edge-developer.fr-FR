---
description: Documentation de messagerie Native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100251"
---
# <span data-ttu-id="8078b-104">Messagerie native</span><span class="sxs-lookup"><span data-stu-id="8078b-104">Native messaging</span></span>  

<span data-ttu-id="8078b-105">Les extensions communiquent avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de passage de messages.</span><span class="sxs-lookup"><span data-stu-id="8078b-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="8078b-106">L’hôte d’application natif envoie et reçoit des messages avec des extensions à l’aide d’une entrée standard et d’une sortie standard.</span><span class="sxs-lookup"><span data-stu-id="8078b-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="8078b-107">Les extensions utilisant la messagerie Native sont installées dans Microsoft Edge de la même façon que dans n’importe quelle autre extension.</span><span class="sxs-lookup"><span data-stu-id="8078b-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="8078b-108">Toutefois, les applications natives ne sont pas installées ni gérées par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8078b-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="8078b-109">Pour acquérir l’extension et l’hôte d’application native, vous avez deux modèles de distribution.</span><span class="sxs-lookup"><span data-stu-id="8078b-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="8078b-110">Emportez votre extension et l’hôte ensemble.</span><span class="sxs-lookup"><span data-stu-id="8078b-110">Package your extension and the host together.</span></span>  <span data-ttu-id="8078b-111">Lorsqu’un utilisateur installe le package, l’extension et l’hôte sont installés.</span><span class="sxs-lookup"><span data-stu-id="8078b-111">When a user installs the package, both the extension and the host are installed.</span></span>
*   <span data-ttu-id="8078b-112">Installez votre extension à l’aide du [magasin de modules complémentaires Microsoft Edge][EdgeAddons]et votre extension invite les utilisateurs à installer l’hôte.</span><span class="sxs-lookup"><span data-stu-id="8078b-112">Install your extension using the [Microsoft Edge Add-ons store][EdgeAddons], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="8078b-113">Pour créer votre extension et envoyer et recevoir des messages avec des hôtes d’application natifs, reportez-vous aux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8078b-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="8078b-114">Étape 1: ajouter des autorisations au manifeste de l’extension</span><span class="sxs-lookup"><span data-stu-id="8078b-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="8078b-115">Ajoutez l' `nativeMessaging` autorisation à la **manifest.jssur** le fichier de l’extension.</span><span class="sxs-lookup"><span data-stu-id="8078b-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="8078b-116">L’extrait de code suivant est un exemple de **manifest.jsactivé**.</span><span class="sxs-lookup"><span data-stu-id="8078b-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="8078b-117">Étape 2: créer le fichier de manifeste de votre hôte de messagerie natif</span><span class="sxs-lookup"><span data-stu-id="8078b-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="8078b-118">Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="8078b-119">Le fichier manifeste contient le chemin d’accès au service d’exécution de l’hôte de messagerie natif, la méthode de communication avec l’extension et la liste des extensions autorisées auxquelles il communique.</span><span class="sxs-lookup"><span data-stu-id="8078b-119">The manifest file contains the path to the native messaging host runtime, the method of communication with the extension, and a list of allowed extensions to which it communicates.</span></span>  <span data-ttu-id="8078b-120">Le navigateur lit et valide le manifeste de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-120">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="8078b-121">Le navigateur ne peut pas installer ou gérer le fichier manifeste de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-121">The browser does not install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="8078b-122">Le fichier de manifeste hôte doit être un fichier JSON valide contenant les clés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8078b-122">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8078b-123">Spécifie le nom de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-123">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="8078b-124">Les clients passent cette chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="8078b-124">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="8078b-125">Cette valeur doit uniquement contenir des caractères alphanumériques minuscules, des traits de soulignement et des points.</span><span class="sxs-lookup"><span data-stu-id="8078b-125">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="8078b-126">Cette valeur ne doit pas commencer ou se terminer par un point, et un point ne doit pas être suivi d’un autre point.</span><span class="sxs-lookup"><span data-stu-id="8078b-126">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8078b-127">Décrit l’application.</span><span class="sxs-lookup"><span data-stu-id="8078b-127">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8078b-128">Spécifie le chemin d’accès au fichier binaire de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-128">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="8078b-129">Sur les appareils Windows, vous pouvez utiliser des chemins d’accès relatifs à l’annuaire qui contient le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="8078b-129">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="8078b-130">Sur macOS et Linux, le chemin d’accès doit être absolu.</span><span class="sxs-lookup"><span data-stu-id="8078b-130">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="8078b-131">Le processus hôte commence par le répertoire actif défini sur le répertoire contenant le fichier binaire hôte.</span><span class="sxs-lookup"><span data-stu-id="8078b-131">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="8078b-132">Par exemple, \ (Windows \), si ce paramètre est défini sur `C:\Application\nm_host.exe` , le fichier binaire est démarré à l’aide du répertoire actif \ ( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="8078b-132">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8078b-133">Spécifie le type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-133">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="8078b-134">Cette valeur indique à Microsoft Edge d’utiliser `stdin` et `stdout` de communiquer avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="8078b-134">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="8078b-135">La seule valeur acceptable est `stdio` .</span><span class="sxs-lookup"><span data-stu-id="8078b-135">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8078b-136">Spécifie la liste des extensions ayant accès à l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="8078b-136">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="8078b-137">Pour permettre à votre application d’identifier et de communiquer avec une extension, dans votre fichier de manifeste d’hôte de messagerie natif, définissez la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="8078b-137">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8078b-138">Charger-xxxxxxx xxxx xxxx xxxx xxxx xxxx xxxxxxx.</span><span class="sxs-lookup"><span data-stu-id="8078b-138">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="8078b-139">Pour charger votre extension lors du développement et de la récupération `microsoft_catalog_extension_id` , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8078b-139">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="8078b-140">Accédez à `edge://extensions` , puis activez le bouton bascule mode développeur.</span><span class="sxs-lookup"><span data-stu-id="8078b-140">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="8078b-141">Sélectionnez **charger**le fichier non emballé, puis sélectionnez votre package d’extension pour charger.</span><span class="sxs-lookup"><span data-stu-id="8078b-141">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="8078b-142">Choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8078b-142">Choose **OK**.</span></span>
1.  <span data-ttu-id="8078b-143">Naviguez jusqu’à `edge://extensions` la page et vérifiez que votre extension figure dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8078b-143">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="8078b-144">Copiez la clé à partir de `microsoft_catalog_extension_id` \ (ID \) à partir de la liste d’extensions sur la page.</span><span class="sxs-lookup"><span data-stu-id="8078b-144">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>

<span data-ttu-id="8078b-145">Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez votre extension sur le magasin des modules complémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8078b-145">When you are ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="8078b-146">L’ID d’extension de l’extension publiée risque de différer de l’ID utilisé lors de la chargement indépendant de votre extension.</span><span class="sxs-lookup"><span data-stu-id="8078b-146">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="8078b-147">Si l’ID a changé, mettez à jour `allowed_origins` le fichier de manifeste hôte avec l’ID de votre extension publiée.</span><span class="sxs-lookup"><span data-stu-id="8078b-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="8078b-148">Étape 3: copier le fichier manifeste de l’hôte de messagerie natif sur votre système</span><span class="sxs-lookup"><span data-stu-id="8078b-148">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="8078b-149">La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie natif sur votre ordinateur et à vérifier qu’il est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="8078b-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it is configured correctly.</span></span>  <span data-ttu-id="8078b-150">Pour vous assurer que le fichier de votre manifeste est placé à l’emplacement attendu, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8078b-150">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="8078b-151">L’emplacement varie en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="8078b-151">The location varies by platform.</span></span>  

### [<span data-ttu-id="8078b-152">Windows</span><span class="sxs-lookup"><span data-stu-id="8078b-152">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="8078b-153">Le fichier manifeste est disponible n’importe où dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8078b-153">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="8078b-154">Le programme d’installation de l’application doit créer une clé de Registre et définir la valeur par défaut de cette clé sur le chemin d’accès complet du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="8078b-154">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="8078b-155">Les commandes suivantes sont des exemples de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="8078b-155">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="8078b-156">Pour ajouter une clé de Registre à l’annuaire à l’aide de la clé de manifeste.</span><span class="sxs-lookup"><span data-stu-id="8078b-156">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="8078b-157">Commande exécuter dans l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8078b-157">Run command in command prompt.</span></span>    
    
    1.  <span data-ttu-id="8078b-158">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="8078b-158">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="8078b-159">Créer un `.reg` fichier et l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="8078b-159">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="8078b-160">Copiez la commande suivante dans un `.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="8078b-160">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="8078b-161">Exécutez le `.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="8078b-161">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="8078b-162">Microsoft Edge interroge d’abord le registre 32, puis le registre 64 bits pour identifier les hôtes de messagerie natifs.</span><span class="sxs-lookup"><span data-stu-id="8078b-162">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span>  <span data-ttu-id="8078b-163">Si vous exécutez le fichier ci-dessus `.reg` dans le cadre d’un script de commandes, assurez-vous de l’exécuter à l’aide d’une invite de commandes administrateur.</span><span class="sxs-lookup"><span data-stu-id="8078b-163">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="8078b-164">macOS</span><span class="sxs-lookup"><span data-stu-id="8078b-164">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="8078b-165">Pour stocker le fichier manifeste, effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8078b-165">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="8078b-166">Les hôtes de messagerie natif au niveau du système, qui sont disponibles pour tous les utilisateurs, sont stockés à un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="8078b-166">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="8078b-167">Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="8078b-167">For example, the manifest file must be stored in following location.</span></span> 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="8078b-168">Les hôtes de messagerie natif spécifiques à l’utilisateur, qui sont disponibles uniquement pour l’utilisateur actuel, sont situés dans le `NativeMessagingHosts` sous-répertoire dans le répertoire du profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8078b-168">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="8078b-169">Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="8078b-169">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="8078b-170">La  `{Channel_Name}` `Microsoft Edge {Channel_Name}` figure de doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8078b-170">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="8078b-171">Canary</span><span class="sxs-lookup"><span data-stu-id="8078b-171">Canary</span></span>  
    *   <span data-ttu-id="8078b-172">Dev</span><span class="sxs-lookup"><span data-stu-id="8078b-172">Dev</span></span>  
    *   <span data-ttu-id="8078b-173">Beta</span><span class="sxs-lookup"><span data-stu-id="8078b-173">Beta</span></span>  

    <span data-ttu-id="8078b-174">Lors de l’utilisation du canal stable, `{Channel_Name}` n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8078b-174">When using the Stable channel, `{Channel_Name}` is not required.</span></span>  

### [<span data-ttu-id="8078b-175">Linux</span><span class="sxs-lookup"><span data-stu-id="8078b-175">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="8078b-176">Pour stocker le fichier manifeste, effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8078b-176">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="8078b-177">Les hôtes de messagerie natif au niveau du système, qui sont disponibles pour tous les utilisateurs, sont stockés à un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="8078b-177">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="8078b-178">Le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="8078b-178">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="8078b-179">Les hôtes de messagerie natif spécifiques à l’utilisateur, qui sont disponibles uniquement pour l’utilisateur actuel, sont situés dans le `NativeMessagingHosts` sous-répertoire dans le répertoire du profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8078b-179">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="8078b-180">Le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="8078b-180">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="8078b-181">Vérifiez que vous fournissez des autorisations de lecture sur le fichier manifeste et des autorisations d’exécution sur le runtime hôte.</span><span class="sxs-lookup"><span data-stu-id="8078b-181">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="8078b-182">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8078b-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8078b-183">La page d’origine est disponible [ici](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="8078b-183">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="8078b-185">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8078b-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Modules complémentaires Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
