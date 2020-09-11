---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Globals
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 37a7d89dbd7d13befe5a07c72fc8baa750775108
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011956"
---
# <span data-ttu-id="bd961-104">Globals</span><span class="sxs-lookup"><span data-stu-id="bd961-104">Globals</span></span> 

## <span data-ttu-id="bd961-105">Résumé</span><span class="sxs-lookup"><span data-stu-id="bd961-105">Summary</span></span>

 <span data-ttu-id="bd961-106">Ses</span><span class="sxs-lookup"><span data-stu-id="bd961-106">Members</span></span>                        | <span data-ttu-id="bd961-107">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bd961-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd961-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="bd961-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="bd961-109">Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="bd961-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="bd961-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="bd961-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="bd961-111">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="bd961-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="bd961-112">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="bd961-112">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="bd961-113">Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée d’Edge, un répertoire de données utilisateur et/ou des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bd961-113">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="bd961-114">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="bd961-114">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="bd961-115">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="bd961-115">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="bd961-116">Ses</span><span class="sxs-lookup"><span data-stu-id="bd961-116">Members</span></span>

#### <span data-ttu-id="bd961-117">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="bd961-117">CompareBrowserVersions</span></span> 

> <span data-ttu-id="bd961-118">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="bd961-118">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="bd961-119">Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="bd961-119">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="bd961-120">Il peut être utilisé pour déterminer s’il est possible d’utiliser webview2 ou certaines fonctionnalités de la version.</span><span class="sxs-lookup"><span data-stu-id="bd961-120">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="bd961-121">Définit la valeur de result sur-1, 0 ou 1 si la valeur version1 est inférieure ou égale ou supérieure à la valeur version2 respectivement.</span><span class="sxs-lookup"><span data-stu-id="bd961-121">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="bd961-122">Renvoie E_INVALIDARG s’il n’y a pas d’analyse des chaînes de version ou si aucun paramètre d’entrée n’a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bd961-122">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="bd961-123">Les données d’entrée peuvent utiliser directement le versionInfo obtenu à partir de GetAvailableCoreWebView2BrowserVersionString, les informations de canal seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="bd961-123">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="bd961-124">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="bd961-124">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="bd961-125">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="bd961-125">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span></span>

<span data-ttu-id="bd961-126">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="bd961-126">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="bd961-127">Cela équivaut à appeler CreateCoreWebView2EnvironmentWithOptions avec nullptr pour browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="bd961-127">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="bd961-128">Pour plus d’informations, consultez CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="bd961-128">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="bd961-129">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="bd961-129">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="bd961-130">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="bd961-130">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span></span>

<span data-ttu-id="bd961-131">Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée d’Edge, un répertoire de données utilisateur et/ou des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bd961-131">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="bd961-132">L’environnement WebView2 et tous les autres objets WebView2 sont des threads uniques et disposent de dépendances sur les composants Windows qui nécessitent l’initialisation d’un modèle COM pour un thread unique cloisonné.</span><span class="sxs-lookup"><span data-stu-id="bd961-132">The WebView2 environment and all other WebView2 objects are single threaded and have dependencies on Windows components that require COM to be initialized for a single-threaded apartment.</span></span> <span data-ttu-id="bd961-133">L’application est censée appeler CoInitializeEx avant d’appeler CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="bd961-133">The application is expected to call CoInitializeEx before calling CreateCoreWebView2EnvironmentWithOptions.</span></span>

```
CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED);
```

<span data-ttu-id="bd961-134">Si CoInitializeEx n’a pas été appelé ou a déjà été appelé avec COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions échoue en utilisant l’une des erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bd961-134">If CoInitializeEx was not called or has been previously called with COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions will fail with one of the following errors.</span></span>

```
CO_E_NOTINITIALIZED (if CoInitializeEx was not called)
RPC_E_CHANGED_MODE  (if CoInitializeEx was previously called with
                     COINIT_MULTITHREADED)
```

<span data-ttu-id="bd961-135">Permet `browserExecutableFolder` de spécifier si les contrôles de WebView2 utilisent une version fixe ou installée du runtime WebView2 qui existe sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="bd961-135">Use `browserExecutableFolder` to specify whether WebView2 controls use a fixed or installed version of the WebView2 Runtime that exists on a client machine.</span></span> <span data-ttu-id="bd961-136">Pour utiliser une version fixe de WebView2 Runtime, transmettez le chemin d’accès relatif du dossier qui contient la version fixe de WebView2 Runtime à `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="bd961-136">To use a fixed version of the WebView2 Runtime, pass the relative path of the folder that contains the fixed version of the WebView2 Runtime to `browserExecutableFolder`.</span></span> <span data-ttu-id="bd961-137">Pour créer des contrôles WebView2 qui utilisent la version installée de WebView2 Runtime disponible sur les ordinateurs clients, transmettez une chaîne null ou vide à `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="bd961-137">To create WebView2 controls that use the installed version of the WebView2 Runtime that exists on client machines, pass a null or empty string to `browserExecutableFolder`.</span></span> <span data-ttu-id="bd961-138">Dans ce scénario, l’API tente de rechercher une version compatible du runtime WebView2 qui est installée sur l’ordinateur client (tout d’abord au niveau de l’ordinateur, puis par utilisateur) en utilisant les préférences de canal sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="bd961-138">In this scenario, the API tries to find a compatible version of the WebView2 Runtime that is installed on the client machine (first at the machine level, and then per user) using the selected channel preference.</span></span> <span data-ttu-id="bd961-139">Le chemin d’accès à une version fixe de WebView2 Runtime ne doit pas contenir `\Edge\Application\` .</span><span class="sxs-lookup"><span data-stu-id="bd961-139">The path of fixed version of the WebView2 Runtime should not contain `\Edge\Application\`.</span></span> <span data-ttu-id="bd961-140">Lorsque ce type de chemin d’accès est utilisé, l’API ne fonctionne pas avec ERROR_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="bd961-140">When such a path is used, the API will fail with ERROR_NOT_SUPPORTED.</span></span>

<span data-ttu-id="bd961-141">Par défaut, l’ordre de recherche par canal est le WebView2 Runtime, bêta, dev et Canaries.</span><span class="sxs-lookup"><span data-stu-id="bd961-141">The default channel search order is the WebView2 Runtime, Beta, Dev, and Canary.</span></span> <span data-ttu-id="bd961-142">S’il existe une substitution WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable d’environnement ou une valeur de Registre releaseChannelPreference applicable ayant la valeur 1, l’ordre de recherche de canal est inversé.</span><span class="sxs-lookup"><span data-stu-id="bd961-142">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="bd961-143">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="bd961-143">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="bd961-144">Il peut s’agir d’un chemin d’accès absolu ou d’un chemin de fichier relatif qui est interprété comme relatif au fichier exécutable du processus actuel.</span><span class="sxs-lookup"><span data-stu-id="bd961-144">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="bd961-145">Dans le cas contraire, pour les applications UWP, le dossier de données utilisateur par défaut sera le dossier Data App pour le package. dans le cas des applications non UWP, le dossier de données utilisateur par défaut `{Executable File Name}.WebView2` sera créé dans le même répertoire en regard du fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="bd961-145">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="bd961-146">La création de WebView2 peut échouer si le fichier exécutable s’exécute dans un répertoire dans lequel le processus n’est pas autorisé à créer un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="bd961-146">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="bd961-147">Lorsque l’application est exécutée, l’application est chargée de nettoyer son dossier de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd961-147">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="bd961-148">Notez que, dans la mesure où le processus de navigateur peut être partagé entre les WebViews, la création de WebView échoue avec HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) si les options spécifiées ne correspondent pas aux options des webvues actuellement en cours d’exécution dans le processus de navigateur partagé.</span><span class="sxs-lookup"><span data-stu-id="bd961-148">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="bd961-149">environmentCreatedHandler est le résultat du gestionnaire de l’opération asynchrone qui contient le WebView2Environment qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="bd961-149">environmentCreatedHandler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="bd961-150">Le browserExecutableFolder, userDataFolder et additionalBrowserArguments du environmentOptions peut être substitué par les valeurs spécifiées dans les variables d’environnement ou dans le registre.</span><span class="sxs-lookup"><span data-stu-id="bd961-150">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="bd961-151">Lors de la création d’un WebView2Environment, les variables d’environnement suivantes sont activées:</span><span class="sxs-lookup"><span data-stu-id="bd961-151">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="bd961-152">Si une variable d’environnement de substitution est trouvée, nous utilisons les valeurs browserExecutableFolder et userDataFolder comme remplaçants pour les valeurs correspondantes des paramètres CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="bd961-152">If an override environment variable is found then we use the browserExecutableFolder and userDataFolder values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span> <span data-ttu-id="bd961-153">Si additionalBrowserArguments est spécifiée dans la variable d’environnement ou dans le registre, il est ajouté aux valeurs correspinding dans les paramètres CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="bd961-153">If additionalBrowserArguments specified in environment variable or in the registry, it will be appended to the correspinding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="bd961-154">Bien qu’il ne soit pas nécessaire de remplacer strictement, il existe d’autres variables d’environnement qui peuvent être définies:</span><span class="sxs-lookup"><span data-stu-id="bd961-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="bd961-155">Dans le cas d’une valeur non vide, cela indique que le WebView est démarré sous un débogueur de script.</span><span class="sxs-lookup"><span data-stu-id="bd961-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="bd961-156">Dans ce cas, le WebView lancera une `Page.waitForDebugger` commande CDP qui entraînera l’exécution du script à l’intérieur du WebView sur le lancement, jusqu’à ce qu’un débogueur publie une `Runtime.runIfWaitingForDebugger` commande CDP correspondante pour reprendre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bd961-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="bd961-157">Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="bd961-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="bd961-158">Dans le cas d’une valeur non vide, cela signifie que l’application WebView est lancée sous un débogueur de script qui prend également en charge les applications hébergées sur plusieurs vues Web.</span><span class="sxs-lookup"><span data-stu-id="bd961-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="bd961-159">La valeur est utilisée comme identificateur pour un canal nommé qui sera ouvert et écrit lors de la création d’un nouveau WebView par l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="bd961-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="bd961-160">La charge utile correspond à celle de la cible JSON du débogage à distance et peut être utilisée par le débogueur externe pour être attachée à une instance WebView spécifique.</span><span class="sxs-lookup"><span data-stu-id="bd961-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="bd961-161">Le format du canal créé par le débogueur doit être `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` le suivant:</span><span class="sxs-lookup"><span data-stu-id="bd961-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="bd961-162">est le nom de fichier exe de l’application hôte, par exemple WebView2Example.exe</span><span class="sxs-lookup"><span data-stu-id="bd961-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="bd961-163">est la valeur définie pour WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="bd961-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="bd961-164">Pour activer le débogage des cibles identifiées par le JSON, vous devez également définir la variable d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS à envoyer `--remote-debugging-port={port_num}` :</span><span class="sxs-lookup"><span data-stu-id="bd961-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="bd961-165">correspond au port sur lequel est lié le serveur CDP.</span><span class="sxs-lookup"><span data-stu-id="bd961-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="bd961-166">N’ayez pas à faire en sorte que la définition des variables d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS et WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER entraîne l’affichage des webvues hébergées dans votre application et de leur contenu aux applications tierces, telles que les débogueurs.</span><span class="sxs-lookup"><span data-stu-id="bd961-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="bd961-167">Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="bd961-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="bd961-168">S’il n’existe aucune de ces variables d’environnement, le Registre est examiné suivant.</span><span class="sxs-lookup"><span data-stu-id="bd961-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="bd961-169">Les valeurs de Registre suivantes sont activées:</span><span class="sxs-lookup"><span data-stu-id="bd961-169">The following registry values are checked:</span></span>

```
[{Root}]\Software\Policies\Microsoft\Edge\WebView2\browserExecutableFolder
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\releaseChannelPreference
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\additionalBrowserArguments
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\userDataFolder
"{AppId}"=""
```

<span data-ttu-id="bd961-170">browserExecutableFolder et releaseChannelPreference peuvent être configurés à l’aide d’une stratégie de groupe sous modèles d’administration > Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="bd961-170">browserExecutableFolder and releaseChannelPreference can be configured using group policy under Administrative Templates > Microsoft Edge WebView2.</span></span> <span data-ttu-id="bd961-171">L’ancien emplacement du registre sera déconseillé bientôt:</span><span class="sxs-lookup"><span data-stu-id="bd961-171">The old registry location will be deprecated soon:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="bd961-172">Dans le cas improbable où certaines instances de WebView sont ouvertes lors d’une mise à jour de navigateur, nous pouvons dès lors bloquer la suppression de anciens navigateurs de bord.</span><span class="sxs-lookup"><span data-stu-id="bd961-172">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="bd961-173">Pour éviter de manquer d’espace disque, une nouvelle création d’affichage WebView échoue avec l’erreur suivante s’il détecte qu’il existe de nombreuses versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="bd961-173">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="bd961-174">Le nombre maximal de versions Edge autorisées par défaut est 20.</span><span class="sxs-lookup"><span data-stu-id="bd961-174">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="bd961-175">Il est possible d’écraser le nombre maximal de versions latérales antérieures autorisées avec la valeur de la variable d’environnement suivante.</span><span class="sxs-lookup"><span data-stu-id="bd961-175">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="bd961-176">Si WebView dépend d’une périphérie installée et qu’elle est désinstallée, tout création ultérieure échoue avec l’erreur suivante</span><span class="sxs-lookup"><span data-stu-id="bd961-176">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="bd961-177">Tout d’abord, nous allons vérifier avec root, puis HKCU.</span><span class="sxs-lookup"><span data-stu-id="bd961-177">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="bd961-178">AppId est d’abord défini sur l’ID de modèle utilisateur de l’application du processus de l’appelant, s’il n’y a pas de clé de Registre correspondante, l’AppId est défini sur le nom exécutable du processus de l’appelant, ou si ce n’est pas une clé de Registre, ' \* '.</span><span class="sxs-lookup"><span data-stu-id="bd961-178">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="bd961-179">S’il existe une clé de registre de remplacement, nous utilisons les valeurs de Registre browserExecutableFolder et userDataFolder en tant que remplacements, puis nous ajoutons additionalBrowserArguments valeurs de Registre pour les valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="bd961-179">If an override registry key is found, then we use the browserExecutableFolder and userDataFolder registry values as replacements and append additionalBrowserArguments registry values for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="bd961-180">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="bd961-180">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="bd961-181">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="bd961-181">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="bd961-182">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="bd961-182">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="bd961-183">Les noms de canaux sont Beta, dev et Canaries.</span><span class="sxs-lookup"><span data-stu-id="bd961-183">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="bd961-184">S’il existe un remplacement pour le browserExecutableFolder ou l’option de canal, la substitution est utilisée.</span><span class="sxs-lookup"><span data-stu-id="bd961-184">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="bd961-185">S’il n’y a pas de remplacement, le paramètre transmis à GetAvailableCoreWebView2BrowserVersionString est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bd961-185">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>

