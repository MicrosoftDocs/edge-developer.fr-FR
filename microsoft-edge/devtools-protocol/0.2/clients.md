---
description: La version 0,2 du protocole Microsoft Edge DevTools prend en charge les clients d’outils suivants.
title: Clients de la version 0,2 du protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 657d594b85c47cc1d5c80b8f2ac3ecc4bd4e4502
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565481"
---
# <span data-ttu-id="30964-103">Clients de protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="30964-103">DevTools Protocol Clients</span></span>

> [!NOTE]
> <span data-ttu-id="30964-104">La version 0,2 du protocole Microsoft Edge DevTools fonctionne uniquement avec la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="30964-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>  

<span data-ttu-id="30964-105">**Devtools protocole 0,2** prend en charge les clients d’outils suivants.</span><span class="sxs-lookup"><span data-stu-id="30964-105">**DevTools Protocol 0.2** supports the following tooling clients.</span></span>

<span data-ttu-id="30964-106">[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Visual Studio code Visual](../media/visual-studio-code.png)](#visual-studio-code) Studio [ ![ 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="30964-106">[![Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [![Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [![Microsoft Visual Studio 15.8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span></span>

## <span data-ttu-id="30964-107">Microsoft Edge DevTools preview</span><span class="sxs-lookup"><span data-stu-id="30964-107">Microsoft Edge DevTools Preview</span></span>

<span data-ttu-id="30964-108">Vous pouvez utiliser l’application Windows 10 [**devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome à partir du Microsoft Store pour déboguer à distance un appareil hôte exécutant Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="30964-108">You can use the standalone [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 app from the Microsoft Store to remotely debug a host device running Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) or later).</span></span>

<span data-ttu-id="30964-109">La version 0,2 du protocole DevTools fournit de nouveaux domaines pour le débogage de style et de disposition, ainsi que les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la version 0,1.</span><span class="sxs-lookup"><span data-stu-id="30964-109">Version 0.2 of the DevTools Protocol provides new domains for style and layout debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="30964-110">Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans les panneaux [**éléments**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) et [**débogueur**](../../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="30964-110">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md) panels.</span></span> <span data-ttu-id="30964-111">Pour le moment, le débogage à distance Microsoft Edge est limité aux hôtes de bureau, avec la prise en charge d’autres appareils Windows 10 présents dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="30964-111">Currently Microsoft Edge remote debugging is limited to desktop hosts, with support for other Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="30964-112">Voici comment configurer le débogage à distance à l’aide de l’application Microsoft Edge DevTools preview.</span><span class="sxs-lookup"><span data-stu-id="30964-112">Here's how to set up remote debugging with the Microsoft Edge DevTools Preview app.</span></span> <span data-ttu-id="30964-113">La version 0,2 du protocole DevTools nécessite la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) ou une version ultérieure de Windows Insider Preview sur l’ordinateur hôte (débogueur).</span><span class="sxs-lookup"><span data-stu-id="30964-113">The DevTools Protocol version 0.2 requires [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later Windows Insider Preview build on the host (debugee) machine.</span></span> <span data-ttu-id="30964-114">L’application Edge DevTools Preview (utilisée sur la machine de débogueur) s’exécute sur Windows 10 version 16299 (Windows 10 automne Creators Update, 10/2017) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="30964-114">The Edge DevTools Preview app (used on the debugger machine) will run on Windows 10 version 16299 (Windows 10 Fall Creators Update, 10/2017) or higher.</span></span>

**<span data-ttu-id="30964-115">Sur l’ordinateur hôte (débogueur)...</span><span class="sxs-lookup"><span data-stu-id="30964-115">On the host (debugee) machine...</span></span>**

1. <span data-ttu-id="30964-116">Si vous utilisez un réseau WiFi, assurez-vous que le réseau est marqué comme **domaine** ou **privé**.</span><span class="sxs-lookup"><span data-stu-id="30964-116">If you're on a WiFi network, ensure the network is marked as either **Domain** or **Private**.</span></span> <span data-ttu-id="30964-117">Pour ce faire, ouvrez l’application [**Centre de sécurité Windows Defender**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , cliquez sur **pare-feu & protection du réseau** et vérifiez si votre réseau figure en tant que réseau de *domaine* ou *réseau privé*.</span><span class="sxs-lookup"><span data-stu-id="30964-117">You can verify this by opening the [**Windows Defender Security Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) app, clicking on **Firewall & network protection** and checking if your network is listed as a *Domain network* or *Private network*.</span></span> 

    <span data-ttu-id="30964-118">S’il est répertorié comme étant *public*, accédez à **réglages**  >  **Network & Internet**  >  **Wi-Fi**, cliquez sur votre réseau et activez le bouton *Network Network (réseau* **privé**).</span><span class="sxs-lookup"><span data-stu-id="30964-118">If its listed as *Public*, go to **Settings** > **Network & Internet** > **Wi-Fi**, click on your network and toggle the *Network profile* button to **Private**.</span></span>

2. <span data-ttu-id="30964-119">Ouvrez le panneau **de configuration pour les développeurs** dans les *paramètres* Windows (recherchez *développeur* et cliquez sur utiliser les *fonctionnalités de développement*) et:</span><span class="sxs-lookup"><span data-stu-id="30964-119">Open the **For developers** control panel in Windows *Settings* (search for *developer* and click on *Use developer features*), and:</span></span> 

    <span data-ttu-id="30964-120">a.</span><span class="sxs-lookup"><span data-stu-id="30964-120">a.</span></span> <span data-ttu-id="30964-121">Activez le **mode développeur**.</span><span class="sxs-lookup"><span data-stu-id="30964-121">Toggle on **Developer Mode**.</span></span> <span data-ttu-id="30964-122">Le package *mode développeur* s’installe, ce qui permet d’activer les outils de contrôle à distance pour le bureau.</span><span class="sxs-lookup"><span data-stu-id="30964-122">This will install the *Developer Mode* package, enabling remote tooling for desktop.</span></span>

    <span data-ttu-id="30964-123">b.</span><span class="sxs-lookup"><span data-stu-id="30964-123">b.</span></span> <span data-ttu-id="30964-124">Activez [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*activez les diagnostics à distance sur connexions au réseau local*) et la **découverte d’appareils** (*rendez votre appareil visible pour les connexions USB et votre réseau local*).</span><span class="sxs-lookup"><span data-stu-id="30964-124">Enable [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*Turn on remote diagnostics over local area network connections*) and **Device discovery** (*Make your device visible to USB connections and your local network*).</span></span>

    <span data-ttu-id="30964-125">c.</span><span class="sxs-lookup"><span data-stu-id="30964-125">c.</span></span> <span data-ttu-id="30964-126">Activez **l’authentification** et attribuez un nom d’utilisateur/mot de passe.</span><span class="sxs-lookup"><span data-stu-id="30964-126">Turn on **Authentication** and supply a username / password.</span></span>

    <span data-ttu-id="30964-127">d.</span><span class="sxs-lookup"><span data-stu-id="30964-127">d.</span></span> <span data-ttu-id="30964-128">Notez l’adresse IP et le port de connexion de l’ordinateur (50443) affichés.</span><span class="sxs-lookup"><span data-stu-id="30964-128">Note the machine IP address and connection port (50443) displayed.</span></span>

3. <span data-ttu-id="30964-129">Ouvrez les onglets dans Microsoft Edge que vous souhaitez déboguer de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="30964-129">Open tabs in Microsoft Edge that you wish to debug from the client machine.</span></span>

**<span data-ttu-id="30964-130">Sur l’ordinateur client (débogueur)...</span><span class="sxs-lookup"><span data-stu-id="30964-130">On the client (debugger) machine...</span></span>**

1.  <span data-ttu-id="30964-131">Installez et lancez l’application [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome à partir du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="30964-131">Install and launch the standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app from the Microsoft Store.</span></span>

2. <span data-ttu-id="30964-132">Ouvrez le panneau **distant** et entrez l’emplacement réseau (URL et port) de l’ordinateur hôte, puis cliquez sur **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="30964-132">Open the **Remote** panel and enter the network location (URL and port) of the host machine and click **Connect**.</span></span>

3. <span data-ttu-id="30964-133">**Installez** le certificat de l’ordinateur hôte à partir de la boîte de dialogue *certificat non approuvé* qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="30964-133">**Install** the host machine's certificate from the *Untrusted Certificate* dialog that appears.</span></span>

4. <span data-ttu-id="30964-134">Fournissez le nom d’utilisateur/mot de passe que vous avez désigné pour l’authentification Device Portal.</span><span class="sxs-lookup"><span data-stu-id="30964-134">Supply the username/password you designated for Device Portal authentication.</span></span>

5. <span data-ttu-id="30964-135">Le panneau *distant* charge une liste de cibles de pages débogageées sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="30964-135">The *Remote* panel will load a list of debuggable page targets on the host machine.</span></span> <span data-ttu-id="30964-136">Sélectionnez-en un pour démarrer le débogage.</span><span class="sxs-lookup"><span data-stu-id="30964-136">Select one to start debugging.</span></span>

6. <span data-ttu-id="30964-137">Utilisez le bouton **Actualiser** pour mettre à jour et rechargez la liste des cibles de pages distantes sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="30964-137">Use the **Refresh** button to update and reload the list of remote page targets on the host machine.</span></span> <span data-ttu-id="30964-138">Cliquez sur le bouton **déconnecter** pour revenir à l’écran *se connecter à un appareil distant* et le joindre à un autre hôte.</span><span class="sxs-lookup"><span data-stu-id="30964-138">Click the **Disconnect** button to return to the *Connect to a remote device* screen and attach to a different host.</span></span>

## <span data-ttu-id="30964-139">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="30964-139">Visual Studio Code</span></span>

<span data-ttu-id="30964-140">Avec le [débogueur pour](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) l’extension de code Edge vs, vous pouvez déboguer l’exécution du script directement dans Microsoft Edge dans le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="30964-140">With the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug script running in Microsoft Edge directly in Visual Studio Code.</span></span> <span data-ttu-id="30964-141">L’extension nécessite que vous utilisiez votre application Web à partir de localhost, que vous puissiez commencer à partir de la ligne de commande ou d’une [tâche](https://code.visualstudio.com/docs/editor/tasks).</span><span class="sxs-lookup"><span data-stu-id="30964-141">The extension requires you to be serving your web application from localhost, which you can start from either command-line or a [Task](https://code.visualstudio.com/docs/editor/tasks).</span></span>

<span data-ttu-id="30964-142">Pour commencer:</span><span class="sxs-lookup"><span data-stu-id="30964-142">To get started:</span></span>

1. <span data-ttu-id="30964-143">Installez le [débogueur pour](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) l’extension de code Edge vs.</span><span class="sxs-lookup"><span data-stu-id="30964-143">Install the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension.</span></span>

2. <span data-ttu-id="30964-144">Redémarrez le code, ouvrez le dossier contenant le projet pour lequel vous souhaitez déboguer et définir des points d’arrêt dans votre code.</span><span class="sxs-lookup"><span data-stu-id="30964-144">Restart VS Code, open the folder containing the project you wish to debug and set breakpoints in your code.</span></span>

3. <span data-ttu-id="30964-145">Configurer une [tâche de lancement](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) d’localhost pour ouvrir la page souhaitée de votre projet: **Déboguer**  >  **Ajouter une configuration...**. Par exemple:</span><span class="sxs-lookup"><span data-stu-id="30964-145">Configure a localhost [launch task](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) to open the desired page of your project: **Debug** > **Add Configuration...**. For example:</span></span>

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    <span data-ttu-id="30964-146">[*L’utilisation du débogueur*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) est plus approfondie sur les paramètres de configuration de lancement.</span><span class="sxs-lookup"><span data-stu-id="30964-146">[*Using the debugger*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) has more on launch configuration settings.</span></span> 

4. <span data-ttu-id="30964-147">Démarrez votre serveur sur localhost, puis appuyez sur le bouton **Démarrer le débogage** (lecture) ou `F5` lancer Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="30964-147">Start your server on localhost and press the **Start Debugging** (play) button or `F5` to launch Microsoft Edge.</span></span> <span data-ttu-id="30964-148">Lorsque le point d’arrêt est atteint, vous êtes interrompu dans le code VS et vous pouvez examiner et parcourir le code à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="30964-148">When a breakpoint is hit, you'll break into VS Code and can further inspect and step through code from there.</span></span>

<span data-ttu-id="30964-149">Pour plus d’informations, consultez le [code vs Debugger pour la documentation Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .</span><span class="sxs-lookup"><span data-stu-id="30964-149">For more, check out the [VS Code - Debugger for Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) documentation.</span></span>

## <span data-ttu-id="30964-150">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30964-150">Microsoft Visual Studio</span></span>

<span data-ttu-id="30964-151">À l’aide de la version la plus récente de [**Visual Studio**](https://www.visualstudio.com) (Visual Studio 15,8 ou version ultérieure) qui s’exécute sur [Windows 10 octobre 2018](/windows/uwp/whats-new/windows-10-build-17763), vous pouvez lancer et déboguer Microsoft Edge à partir de l’IDE sur n’importe quel projet ASP.net ou .net principal.</span><span class="sxs-lookup"><span data-stu-id="30964-151">Using the latest [**Visual Studio**](https://www.visualstudio.com) version (Visual Studio 15.8 or later) running on [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763), you can launch and debug Microsoft Edge from the IDE on any ASP.NET or .NET Core project.</span></span>

<span data-ttu-id="30964-152">Voici comment configurer le débogage Microsoft Edge avec Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="30964-152">Here's how to set up Microsoft Edge debugging with Visual Studio:</span></span>

1.  <span data-ttu-id="30964-153">Installez et lancez la dernière version de [**Visual Studio**](https://www.visualstudio.com/) (visual studio 15,8 ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="30964-153">Install and launch the latest [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15.8 or later).</span></span>

2. <span data-ttu-id="30964-154">Ouvrez un projet ASP.NET ou .NET principal existant, ou **créez un nouveau projet...** à l’aide de l’un des modèles **Visual C#** .net.</span><span class="sxs-lookup"><span data-stu-id="30964-154">Open an existing ASP.NET or .NET Core project or **Create new project...** using one of the **Visual C#** .NET templates.</span></span>

3. <span data-ttu-id="30964-155">Dans l' **Explorateur de solutions**du projet, ouvrez les fichiers JavaScript dont vous souhaitez déboguer et définir des points d’arrêt dans l’environnement de développement, comme vous le feriez avec du code côté serveur.</span><span class="sxs-lookup"><span data-stu-id="30964-155">In the project **Solution Explorer**, open the JavaScript files you wish to debug and set breakpoints within the IDE just as you would with server-side code.</span></span>

4. <span data-ttu-id="30964-156">Appuyez sur `F5` pour lancer Microsoft Edge exécutant le serveur devtools.</span><span class="sxs-lookup"><span data-stu-id="30964-156">Press `F5` to launch Microsoft Edge running the DevTools Server.</span></span> <span data-ttu-id="30964-157">Lorsque le point d’arrêt est atteint, vous êtes interrompu dans Visual Studio, vous pouvez le consulter et parcourir le code à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="30964-157">When a breakpoint is hit, you'll break into Visual Studio and can further inspect and step through the code from there.</span></span>
