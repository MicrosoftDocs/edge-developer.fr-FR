---
description: Documentation sur la messagerie native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: e6233289794bc1c3ef235af46402c23173c09857
ms.sourcegitcommit: e6a4f73be57439149e3cc56491d7364831d0079e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "11475210"
---
# <a name="native-messaging"></a><span data-ttu-id="d2a01-104">Messagerie native</span><span class="sxs-lookup"><span data-stu-id="d2a01-104">Native messaging</span></span>  

<span data-ttu-id="d2a01-105">Les extensions communiquent avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de transmission de message.</span><span class="sxs-lookup"><span data-stu-id="d2a01-105">Extensions communicate with a native Win32 app installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="d2a01-106">L’hôte d’application natif envoie et reçoit des messages avec des extensions à l’aide de l’entrée standard et de la sortie standard.</span><span class="sxs-lookup"><span data-stu-id="d2a01-106">The native app host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="d2a01-107">Les extensions utilisant la messagerie native sont installées dans Microsoft Edge comme n’importe quelle autre extension.</span><span class="sxs-lookup"><span data-stu-id="d2a01-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="d2a01-108">Toutefois, les applications natives ne sont pas installées ou gérées par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d2a01-108">However, native apps are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="d2a01-109">Pour acquérir l’extension et l’hôte d’application native, vous avez deux modèles de distribution.</span><span class="sxs-lookup"><span data-stu-id="d2a01-109">To acquire the extension and native app host, you have two distribution models.</span></span>  

*   <span data-ttu-id="d2a01-110">Rassemblez votre extension et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d2a01-110">Package your extension and the host together.</span></span>  <span data-ttu-id="d2a01-111">Lorsqu’un utilisateur installe le package, l’extension et l’hôte sont installés.</span><span class="sxs-lookup"><span data-stu-id="d2a01-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="d2a01-112">Installez votre extension à l’aide du magasin [de modules][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]de microsoft Edge et votre extension invite les utilisateurs à installer l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d2a01-112">Install your extension using the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="d2a01-113">Pour créer votre extension pour envoyer et recevoir des messages avec des hôtes d’application natifs, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-113">To create your extension to send and receive messages with native app hosts, complete the following steps.</span></span>  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a><span data-ttu-id="d2a01-114">Étape 1 : ajouter des autorisations au manifeste d’extension</span><span class="sxs-lookup"><span data-stu-id="d2a01-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="d2a01-115">Ajoutez `nativeMessaging` l’autorisation au **manifest.jssur le** fichier de l’extension.</span><span class="sxs-lookup"><span data-stu-id="d2a01-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="d2a01-116">L’extrait de code suivant est un exemple \*\* d'manifest.jssur\*\*.</span><span class="sxs-lookup"><span data-stu-id="d2a01-116">The following code snippet is an example of **manifest.json**.</span></span>  

```json
{
    "name": "Native Messaging Example",
    "version": "1.0",
    "manifest_version": 2, 
    "description": "Send a message to a native app.",
    "app": { 
        "launch": { 
            "local_path": "main.html" 
        } 
    }, 
    "icons": { 
        "128": "icon-128.png"
    }, 
    "permissions": ["nativeMessaging"] 
}
```  

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a><span data-ttu-id="d2a01-117">Étape 2 : créer votre fichier manifeste d’hôte de messagerie native</span><span class="sxs-lookup"><span data-stu-id="d2a01-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="d2a01-118">Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="d2a01-118">Native apps must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="d2a01-119">Le fichier manifeste contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="d2a01-120">Chemin d’accès au runtime de l’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="d2a01-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="d2a01-121">Méthode de communication avec l’extension.</span><span class="sxs-lookup"><span data-stu-id="d2a01-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="d2a01-122">Liste des extensions autorisées avec lesquelles il communique.</span><span class="sxs-lookup"><span data-stu-id="d2a01-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="d2a01-123">Le navigateur lit et valide le manifeste d’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="d2a01-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="d2a01-124">Le navigateur n’installe pas ou ne gère pas le fichier manifeste de l’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="d2a01-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

```json
{
    "name": "com.my_company.my_app",
    "description": "My App",
    "path": "C:\\Program Files\\My App\\chrome_native_messaging_host.exe",
    "type": "stdio",
    "allowed_origins": [
        "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="d2a01-125">Le fichier manifeste hôte doit être un fichier JSON valide qui contient les clés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d2a01-126">Clé</span><span class="sxs-lookup"><span data-stu-id="d2a01-126">Key</span></span>**  
   :::column-end:::
   :::column span="3":::
      **<span data-ttu-id="d2a01-127">Détails</span><span class="sxs-lookup"><span data-stu-id="d2a01-127">Details</span></span>**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="d2a01-128">Spécifie le nom de l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="d2a01-128">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="d2a01-129">Les clients passent la chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="d2a01-129">Clients pass the string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="d2a01-130">La valeur ne doit contenir que des caractères alphanumériques en minuscules, des traits de soulignement et des points.</span><span class="sxs-lookup"><span data-stu-id="d2a01-130">The value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="d2a01-131">La valeur ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point.</span><span class="sxs-lookup"><span data-stu-id="d2a01-131">The value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="d2a01-132">Décrit l’application.</span><span class="sxs-lookup"><span data-stu-id="d2a01-132">Describes the app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="d2a01-133">Spécifie le chemin d’accès au fichier binaire hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="d2a01-133">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="d2a01-134">Sur les appareils Windows, vous pouvez utiliser des chemins d’accès relatifs au répertoire qui contient le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="d2a01-134">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="d2a01-135">Sur macOS et Linux, le chemin d’accès doit être absolu.</span><span class="sxs-lookup"><span data-stu-id="d2a01-135">On macOS and Linux, the path must be absolute.</span></span>  
          
      <span data-ttu-id="d2a01-136">Le processus hôte commence par le répertoire actuel qui contient le fichier binaire hôte.</span><span class="sxs-lookup"><span data-stu-id="d2a01-136">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="d2a01-137">Par exemple \(Windows\), si le paramètre est paramétrage, le fichier binaire est démarré à l’aide du répertoire `C:\App\nm_host.exe` actuel \( `C:\App\` \).</span><span class="sxs-lookup"><span data-stu-id="d2a01-137">For example \(Windows\), if the parameter is set to `C:\App\nm_host.exe`, the binary is started using the current directory \(`C:\App\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="d2a01-138">Spécifie le type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="d2a01-138">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="d2a01-139">La valeur indique à Microsoft Edge d’utiliser `stdin` et de communiquer avec `stdout` l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d2a01-139">The value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="d2a01-140">La seule valeur acceptable est `stdio` .</span><span class="sxs-lookup"><span data-stu-id="d2a01-140">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="d2a01-141">Spécifie la liste des extensions qui ont accès à l’hôte de messagerie natif.</span><span class="sxs-lookup"><span data-stu-id="d2a01-141">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="d2a01-142">Pour activer votre application afin d’identifier et de communiquer avec une extension, dans votre fichier manifeste hôte de messagerie native, définissez la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="d2a01-142">To turn on your app to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d2a01-143">Chargez une version test de votre extension pour tester la messagerie native avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d2a01-143">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="d2a01-144">Pour recharger une version de votre extension pendant le développement et `microsoft_catalog_extension_id` récupérer, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-144">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following actions.</span></span>  

1.  <span data-ttu-id="d2a01-145">Accédez à , puis activer le bouton bascule `edge://extensions` du mode développeur.</span><span class="sxs-lookup"><span data-stu-id="d2a01-145">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="d2a01-146">Choisissez **Charger décompressé,** puis choisissez votre package d’extension à charger de côté.</span><span class="sxs-lookup"><span data-stu-id="d2a01-146">Choose **Load unpacked**, and then choose your extension package to sideload.</span></span>  
1.  <span data-ttu-id="d2a01-147">Choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2a01-147">Choose **OK**.</span></span>  
1.  <span data-ttu-id="d2a01-148">Accédez à `edge://extensions` la page et vérifiez que votre extension est répertoriée.</span><span class="sxs-lookup"><span data-stu-id="d2a01-148">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="d2a01-149">Copiez la clé à partir `microsoft_catalog_extension_id` de \(ID\) à partir de la liste des extensions sur la page.</span><span class="sxs-lookup"><span data-stu-id="d2a01-149">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  
    
<span data-ttu-id="d2a01-150">Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez-la dans le magasin de modules extensions Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d2a01-150">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="d2a01-151">L’ID d’extension de l’extension publiée peut différer de l’ID utilisé lors du chargement de votre extension.</span><span class="sxs-lookup"><span data-stu-id="d2a01-151">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="d2a01-152">Si l’ID a changé, mettez à jour dans le fichier manifeste hôte avec `allowed_origins` l’ID de votre extension publiée.</span><span class="sxs-lookup"><span data-stu-id="d2a01-152">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a><span data-ttu-id="d2a01-153">Étape 3 : copier le fichier manifeste de l’hôte de messagerie native dans votre système</span><span class="sxs-lookup"><span data-stu-id="d2a01-153">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="d2a01-154">La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie native sur votre ordinateur et à s’assurer que le fichier manifeste est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="d2a01-154">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="d2a01-155">Pour vous assurer que votre fichier manifeste est placé à l’emplacement attendu, complétez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-155">To ensure your manifest file is placed in the expected location, complete the following the actions.</span></span>  <span data-ttu-id="d2a01-156">L’emplacement varie en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="d2a01-156">The location varies by platform.</span></span>

> [!NOTE]
> <span data-ttu-id="d2a01-157">Veillez à fournir des autorisations de lecture sur le fichier manifeste et à exécuter les autorisations sur l’runtime hôte.</span><span class="sxs-lookup"><span data-stu-id="d2a01-157">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

### [<a name="windows"></a><span data-ttu-id="d2a01-158">Windows</span><span class="sxs-lookup"><span data-stu-id="d2a01-158">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="d2a01-159">Le fichier manifeste peut se trouver n’importe où dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2a01-159">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="d2a01-160">Le programme d’installation de l’application doit créer une clé de Registre et définir la valeur par défaut de la clé sur le chemin d’accès complet du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="d2a01-160">The app installer must create a registry key and set the default value of the key to the full path of the manifest file.</span></span>  <span data-ttu-id="d2a01-161">Les emplacements suivants sont des exemples de clés de Registre.</span><span class="sxs-lookup"><span data-stu-id="d2a01-161">The following locations are examples of registry keys.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

<span data-ttu-id="d2a01-162">Pour ajouter une clé de Registre au répertoire avec la clé de manifeste, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-162">To add a registry key to the directory with the manifest key, complete one of the following actions.</span></span>  

*   <span data-ttu-id="d2a01-163">Exécutez la commande dans l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-163">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="d2a01-164">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="d2a01-164">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   <span data-ttu-id="d2a01-165">Créez `.reg` un fichier et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="d2a01-165">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="d2a01-166">Copiez la commande suivante dans un `.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="d2a01-166">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="d2a01-167">Exécutez le `.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="d2a01-167">Run the `.reg` file.</span></span>  
        
<span data-ttu-id="d2a01-168">Microsoft Edge interroge la `HKEY_CURRENT_USER` clé racine suivie de `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="d2a01-168">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="d2a01-169">Dans les deux clés, le Registre 32 bits est recherché en premier, puis le Registre 64 bits est recherché pour identifier les hôtes de messagerie natifs.</span><span class="sxs-lookup"><span data-stu-id="d2a01-169">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="d2a01-170">La clé de Registre spécifie l’emplacement du manifeste d’hôte de messagerie native.</span><span class="sxs-lookup"><span data-stu-id="d2a01-170">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="d2a01-171">Si les entrées de Registre de Microsoft Edge n’ont pas l’emplacement du manifeste hôte, les emplacements de Registre Chromium et Chrome sont utilisés comme options de base.</span><span class="sxs-lookup"><span data-stu-id="d2a01-171">If the registry entries for Microsoft Edge don't have the location of the host manifest, the Chromium and Chrome registry locations are used as fallback options.</span></span>  <span data-ttu-id="d2a01-172">Si Microsoft Edge trouve la clé de Registre à l’un des emplacements répertoriés précédemment, il n’interroge pas les emplacements répertoriés dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d2a01-172">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in the following code snippet.</span></span>  <span data-ttu-id="d2a01-173">Si vous exécutez votre fichier créé dans le cadre d’un script de commandes, veillez à l’exécuter à l’aide d’une `.reg` invite de commandes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d2a01-173">If you run your created `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>

<span data-ttu-id="d2a01-174">La liste suivante est l’ordre de recherche pour les emplacements du Registre.</span><span class="sxs-lookup"><span data-stu-id="d2a01-174">The following list is the search order for the registry locations.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\

HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\
```  
 
> [!NOTE] 
> <span data-ttu-id="d2a01-175">Si vous avez des extensions sur les extensions Microsoft Edge et chrome Webstore, vous devez ajouter les ID d’extension correspondant aux deux magasins dans le fichier manifeste de l’hôte, car seul le manifeste hôte correspondant au premier emplacement de Registre trouvé est `allowed_origins` lu.</span><span class="sxs-lookup"><span data-stu-id="d2a01-175">If you have extensions on the Microsoft Edge Add-ons and the Chrome Webstore, you must add the extension IDs corresponding to both the stores in the `allowed_origins` of the host manifest file because only the host manifest corresponding to the first registry location found is read.</span></span>  

### [<a name="macos"></a><span data-ttu-id="d2a01-176">macOS</span><span class="sxs-lookup"><span data-stu-id="d2a01-176">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="d2a01-177">Pour stocker le fichier manifeste, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-177">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="d2a01-178">Les hôtes de messagerie native à l’échelle du système, qui sont disponibles pour tous les utilisateurs, sont stockés dans un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="d2a01-178">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="d2a01-179">Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="d2a01-179">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   <span data-ttu-id="d2a01-180">Les hôtes de messagerie native spécifiques à l’utilisateur, disponibles uniquement pour l’utilisateur actuel, se trouvent dans le sous-répertoire de `NativeMessagingHosts` l’annuaire de profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2a01-180">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="d2a01-181">Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="d2a01-181">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    <span data-ttu-id="d2a01-182">`{Channel_Name}` `Microsoft Edge {Channel_Name}` L’in doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-182">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    <span data-ttu-id="d2a01-183">Lorsque vous utilisez le canal stable, ` {Channel_Name}` cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d2a01-183">When using the Stable channel, ` {Channel_Name}` isn't required.</span></span>  
    
### [<a name="linux"></a><span data-ttu-id="d2a01-184">Linux</span><span class="sxs-lookup"><span data-stu-id="d2a01-184">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="d2a01-185">Pour stocker le fichier manifeste, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2a01-185">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="d2a01-186">Les hôtes de messagerie native à l’échelle du système, qui sont disponibles pour tous les utilisateurs, sont stockés dans un emplacement fixe.</span><span class="sxs-lookup"><span data-stu-id="d2a01-186">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="d2a01-187">Le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="d2a01-187">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="d2a01-188">Les hôtes de messagerie native spécifiques à l’utilisateur, disponibles uniquement pour l’utilisateur actuel, se trouvent dans le sous-répertoire de `NativeMessagingHosts` l’annuaire de profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2a01-188">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="d2a01-189">Le fichier manifeste doit être stocké à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="d2a01-189">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge Add-ons"

> [!NOTE]
> <span data-ttu-id="d2a01-191">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d2a01-191">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d2a01-192">La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="d2a01-192">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d2a01-194">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d2a01-194">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
