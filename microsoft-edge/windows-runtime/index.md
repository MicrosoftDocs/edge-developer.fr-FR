---
description: Utilisez Windows Runtime (WinRT) pour appeler des API Windows natives à partir de votre application JavaScript.
title: Windows Runtime (WinRT) pour JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Windows Runtime, WinRT, PWA, JavaScript
ms.openlocfilehash: 4ca92323a85a1e90896b4de26778f7cf7dfc9a11
ms.sourcegitcommit: e07de36ee9fbe20422ffc2c62b98839851e1b02b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2020
ms.locfileid: "10604019"
---
# <span data-ttu-id="f3240-104">Windows Runtime (WinRT) pour JavaScript</span><span class="sxs-lookup"><span data-stu-id="f3240-104">Windows Runtime (WinRT) for JavaScript</span></span>  

<span data-ttu-id="f3240-105">[Windows Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \ (ou simplement WinRT \) est l’ensemble d’API natives qui alimentent les applications de [plateforme Windows universelle](/windows/uwp/get-started/universal-application-platform-guide) (UWP) qui s’exécutent sur toutes les [familles d’appareils Windows 10](/uwp/extension-sdks/device-families-overview).</span><span class="sxs-lookup"><span data-stu-id="f3240-105">The [Windows Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \(or simply WinRT\) is the collection of native APIs that power the [Universal Windows Platform](/windows/uwp/get-started/universal-application-platform-guide) \(UWP\) apps that run across all [Windows 10 device families](/uwp/extension-sdks/device-families-overview).</span></span>  <span data-ttu-id="f3240-106">Les API WinRT sont projetées dans plusieurs langues, notamment C#, C++, Visual Basic et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3240-106">WinRT APIs are projected into a number of different languages, including C#, C++, Visual Basic, and JavaScript.</span></span>  

<span data-ttu-id="f3240-107">En tant que développeur Web, vous pouvez demander ces API Windows natives à JavaScript lorsque votre application Web s' [exécute sous la forme d’une application Windows 10 installée](../progressive-web-apps-edgehtml/windows-features.md#set-up-and-run-your-universal-windows-app) (lancée à partir du `wwahost.exe` processus, plutôt que du navigateur.).</span><span class="sxs-lookup"><span data-stu-id="f3240-107">As a web developer, you may request these native Windows APIs from JavaScript when your web app is [running as an installed Windows 10 app](../progressive-web-apps-edgehtml/windows-features.md#set-up-and-run-your-universal-windows-app) \(launched from the `wwahost.exe` process, rather than the browser\).</span></span>  <span data-ttu-id="f3240-108">De plus, votre site Web sous la forme d’une application Windows 10 pourra également utiliser le contrôle [WebView Microsoft Edge](#webview) pour afficher du contenu Web distant et local et des API [MSApp](#msapp) pour la gestion de BLOB et de flux, entre autres choses.</span><span class="sxs-lookup"><span data-stu-id="f3240-108">Additionally, your website running as a Windows 10 app may also use the [Microsoft Edge webview](#webview) control to display remote and local web content and [MSApp](#msapp) APIs for blob and stream handling, among other things.</span></span>  

<span data-ttu-id="f3240-109">Voici les zones d’espaces de noms WinRT de niveau supérieur disponibles pour toutes les applications Windows 10:</span><span class="sxs-lookup"><span data-stu-id="f3240-109">Here are the top-level WinRT namespace areas available to all Windows 10 apps:</span></span>  

| <span data-ttu-id="f3240-110">Espace de noms WinRT</span><span class="sxs-lookup"><span data-stu-id="f3240-110">WinRT Namespace</span></span> | <span data-ttu-id="f3240-111">Description</span><span class="sxs-lookup"><span data-stu-id="f3240-111">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f3240-112">[Ai](/uwp/api/windows.AI.MachineLearning.Preview) \ (Preview \)</span><span class="sxs-lookup"><span data-stu-id="f3240-112">[AI](/uwp/api/windows.AI.MachineLearning.Preview) \(Preview\)</span></span> | <span data-ttu-id="f3240-113">Contient des classes qui permettent aux applications de charger les modèles d’apprentissage d’ordinateur, de lier les données en tant qu’entrées et d’évaluer les résultats.</span><span class="sxs-lookup"><span data-stu-id="f3240-113">Contains classes that enable apps to load machine learning models, bind data as inputs, and evaluate the results.</span></span>  |  
| [<span data-ttu-id="f3240-114">ApplicationModel</span><span class="sxs-lookup"><span data-stu-id="f3240-114">ApplicationModel</span></span>](/uwp/api/windows.applicationmodel) | <span data-ttu-id="f3240-115">Fournit à une application un accès aux fonctionnalités principales du système et aux informations d’exécution relatives au package d’application, et gère les opérations de suspension.</span><span class="sxs-lookup"><span data-stu-id="f3240-115">Provides an app with access to core system functionality and run-time information about the app package, and handles suspend operations.</span></span>  |  
| [<span data-ttu-id="f3240-116">Données</span><span class="sxs-lookup"><span data-stu-id="f3240-116">Data</span></span>](/uwp/api/windows.data.html) | <span data-ttu-id="f3240-117">Fournit des classes d’utilitaire pour l’utilisation de divers formats de données, notamment HTML, JSON, PDF, texte et XML.</span><span class="sxs-lookup"><span data-stu-id="f3240-117">Provides utility classes for working with various data formats, including HTML, JSON, PDF, text, and XML.</span></span>  |  
| [<span data-ttu-id="f3240-118">Périphériques</span><span class="sxs-lookup"><span data-stu-id="f3240-118">Devices</span></span>](/uwp/api/windows.devices) | <span data-ttu-id="f3240-119">Cet espace de noms donne accès aux fournisseurs de périphériques de faible niveau, notamment ADC, GPIO, I2 C, PWM et SPI.</span><span class="sxs-lookup"><span data-stu-id="f3240-119">This namespace provides access to the low level device providers, including ADC, GPIO, I2 C, PWM, and SPI.</span></span>  |  
| [<span data-ttu-id="f3240-120">Foundation</span><span class="sxs-lookup"><span data-stu-id="f3240-120">Foundation</span></span>](/uwp/api/windows.foundation) | <span data-ttu-id="f3240-121">Active les fonctionnalités fondamentales du Windows Runtime, notamment la gestion des opérations asynchrones et l’accès aux magasins de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f3240-121">Enables fundamental Windows Runtime functionality, including managing asynchronous operations and accessing property stores.</span></span>  <span data-ttu-id="f3240-122">Cet espace de noms définit également les types de valeur courants qui représentent l’URI (Uniform Resource Identifier), les dates et les heures, les mesures 2D et d’autres valeurs de base.</span><span class="sxs-lookup"><span data-stu-id="f3240-122">This namespace also defines common value types that represent Uniform Resource Identifier \(URI\), dates and times, 2-D measurements, and other basic values.</span></span>  |  
| [<span data-ttu-id="f3240-123">Jeux</span><span class="sxs-lookup"><span data-stu-id="f3240-123">Gaming</span></span>](/uwp/api/windows.gaming.input) |<span data-ttu-id="f3240-124">Donne accès à la saisie du contrôleur de jeu, à la barre de jeux, à la surveillance du jeu et à la discussion de jeu.</span><span class="sxs-lookup"><span data-stu-id="f3240-124">Provides access to game controller input, the Game bar, game monitoring, and game chat.</span></span>  |  
| [<span data-ttu-id="f3240-125">Globalisation</span><span class="sxs-lookup"><span data-stu-id="f3240-125">Globalization</span></span>](/uwp/api/windows.globalization) | <span data-ttu-id="f3240-126">Offre une prise en charge de la globalisation des profils de langue, des régions géographiques et des calendriers internationaux.</span><span class="sxs-lookup"><span data-stu-id="f3240-126">Provides globalization support for language profiles, geographic regions, and international calendars.</span></span>  |  
| [<span data-ttu-id="f3240-127">Graphiques</span><span class="sxs-lookup"><span data-stu-id="f3240-127">Graphics</span></span>](/uwp/api/windows.graphics) | <span data-ttu-id="f3240-128">Fournit des types de données de base contenant des informations sur la façon de dessiner des graphiques.</span><span class="sxs-lookup"><span data-stu-id="f3240-128">Provides basic data types that contain info on how to draw graphics.</span></span>  <span data-ttu-id="f3240-129">Ces structures de données sont couramment utilisées pour définir le mode de dessin des surfaces de grande taille lors de l’utilisation de la classe CompositionVirtualDrawingSurface.</span><span class="sxs-lookup"><span data-stu-id="f3240-129">These data structs are commonly used to define how large surfaces are drawn when using the CompositionVirtualDrawingSurface class.</span></span>  |  
| [<span data-ttu-id="f3240-130">Gestion</span><span class="sxs-lookup"><span data-stu-id="f3240-130">Management</span></span>](/uwp/api/windows.management) | <span data-ttu-id="f3240-131">Fournit des fonctionnalités permettant d’imposer une synchronisation à partir d’un appareil de gestion des périphériques mobiles (GPM) sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f3240-131">Provides capabilities to force a sync from an Mobile Device Management \(MDM\) device to the server.</span></span>  <span data-ttu-id="f3240-132">Ce protocole de synchronisation GPM est basé sur Open Mobile Alliance-Device Management standard.</span><span class="sxs-lookup"><span data-stu-id="f3240-132">This MDM sync protocol is based on the Open Mobile Alliance - Device Management standard.</span></span>  |  
| [<span data-ttu-id="f3240-133">Support</span><span class="sxs-lookup"><span data-stu-id="f3240-133">Media</span></span>](/uwp/api/windows.media) |<span data-ttu-id="f3240-134">Fournit des classes permettant de créer et d’utiliser des éléments multimédias, tels que des photos, des enregistrements audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="f3240-134">Provides classes for creating and working with media such as photos, audio recordings and videos.</span></span>  |  
| [<span data-ttu-id="f3240-135">Réseaux</span><span class="sxs-lookup"><span data-stu-id="f3240-135">Networking</span></span>](/uwp/api/windows.networking) |<span data-ttu-id="f3240-136">Donne accès aux noms d’hôtes et aux points de terminaison utilisés par les applications réseau.</span><span class="sxs-lookup"><span data-stu-id="f3240-136">Provides access to hostnames and endpoints used by network apps.</span></span>  |  
| [<span data-ttu-id="f3240-137">Reçue</span><span class="sxs-lookup"><span data-stu-id="f3240-137">Perception</span></span>](/uwp/api/windows.perception) |<span data-ttu-id="f3240-138">Contient des classes permettant de percevoir l’environnement de l’utilisateur, ce qui permet aux applications de rechercher et de raison de l’appareil par rapport aux surfaces et aux hologrammes de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3240-138">Contains classes for perceiving the user's surroundings, letting apps locate and reason about the device relative to the surfaces and holograms around the user.</span></span>  |  
| [<span data-ttu-id="f3240-139">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f3240-139">Security</span></span>](/uwp/api/windows.security.authentication.identity) | <span data-ttu-id="f3240-140">Fournit des classes pour l’authentification des utilisateurs, la gestion des informations d’identification, les opérations de chiffrement et les fonctionnalités de protection des données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f3240-140">Provides classes for user authentication, credentials management, cryptographic operations and enterprise data protection features.</span></span>  |  
| [<span data-ttu-id="f3240-141">Services</span><span class="sxs-lookup"><span data-stu-id="f3240-141">Services</span></span>](/uwp/api/windows.services.cortana) |<span data-ttu-id="f3240-142">Donne accès à des services Microsoft pour Cortana, cartes, Microsoft Store et le contenu ciblé \ (abonnement \).</span><span class="sxs-lookup"><span data-stu-id="f3240-142">Provides access to Microsoft services for Cortana, Maps, Microsoft Store and Targeted \(subscription\) content.</span></span>  |  
| [<span data-ttu-id="f3240-143">Stockage</span><span class="sxs-lookup"><span data-stu-id="f3240-143">Storage</span></span>](/uwp/api/windows.storage) |<span data-ttu-id="f3240-144">Fournit des classes pour la gestion des fichiers, des dossiers et des paramètres d’application.</span><span class="sxs-lookup"><span data-stu-id="f3240-144">Provides classes for managing files, folders, and application settings.</span></span>  |  
| [<span data-ttu-id="f3240-145">Système</span><span class="sxs-lookup"><span data-stu-id="f3240-145">System</span></span>](/uwp/api/windows.system) |<span data-ttu-id="f3240-146">Active les fonctionnalités système telles que le lancement d’applications, l’obtention d’informations sur un utilisateur et le profilage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3240-146">Enables system functionality such as launching apps, obtaining information about a user, and memory profiling.</span></span>  |  
| [<span data-ttu-id="f3240-147">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="f3240-147">UI</span></span>](/uwp/api/windows.ui) | <span data-ttu-id="f3240-148">Fournit une application ayant accès à la fonctionnalité système principale et aux informations d’exécution relatives à l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3240-148">Provides an app with access to core system functionality and run-time information about the UI.</span></span>  <span data-ttu-id="f3240-149">**Remarque**: les API dans l' `Windows.UI.Xaml` espace de noms ne sont pas disponibles pour les applications JavaScript (qui peuvent utiliser les technologies basées sur des normes Web équivalentes).</span><span class="sxs-lookup"><span data-stu-id="f3240-149">**NOTE**:  APIs in the `Windows.UI.Xaml` namespace are not available for JavaScript apps \(which may use the equivalent web standards-based technologies\).</span></span>  |  
| [<span data-ttu-id="f3240-150">Web</span><span class="sxs-lookup"><span data-stu-id="f3240-150">Web</span></span>](/uwp/api/windows.web) | <span data-ttu-id="f3240-151">Fournit des informations sur les erreurs provenant des opérations de service Web.</span><span class="sxs-lookup"><span data-stu-id="f3240-151">Provides information on errors resulting from web service operations.</span></span>  |  

<span data-ttu-id="f3240-152">Pour plus d’informations sur l’utilisation, voir [utilisation de Windows Runtime en JavaScript](./using-the-windows-runtime-in-javascript.md).</span><span class="sxs-lookup"><span data-stu-id="f3240-152">For more details on usage, check out [Using the Windows Runtime in JavaScript](./using-the-windows-runtime-in-javascript.md).</span></span>  <span data-ttu-id="f3240-153">Pour plus d’informations sur l’exécution de votre site Web en tant qu’application Windows, essayez le didacticiel [de personnalisation de Windows](../progressive-web-apps/windows-features.md) .</span><span class="sxs-lookup"><span data-stu-id="f3240-153">To learn how to run your website as a Windows app, try the [Tailor your PWA for Windows](../progressive-web-apps/windows-features.md) tutorial.</span></span>  

## <span data-ttu-id="f3240-154">WebView</span><span class="sxs-lookup"><span data-stu-id="f3240-154">WebView</span></span>  

<span data-ttu-id="f3240-155">Le contrôle [WebView Microsoft Edge](../webview.md) vous permet d’héberger le contenu Web dans votre application Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f3240-155">The [Microsoft Edge WebView](../webview.md) control enables you to host web content within your Windows 10 app.</span></span>  <span data-ttu-id="f3240-156">Ce type d’utilisation est semblable à l’utilisation d’un `<iframe>` , mais offre de nombreuses [fonctionnalités et contrôle](../hosting/webview.md#webview-versus-iframe) de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f3240-156">This is similar to using an `<iframe>`, but provides a lot [more features and control](../hosting/webview.md#webview-versus-iframe) over the experience.</span></span>  

## <span data-ttu-id="f3240-157">MSApp</span><span class="sxs-lookup"><span data-stu-id="f3240-157">MSApp</span></span>  

<span data-ttu-id="f3240-158">L’objet global [MSApp](./reference/msapp.md) \ ( `window.MSApp` \) fournit des fonctions d’assistance assorties pour les applications Windows 10 basées sur JavaScript, telles que les utilitaires de conversion entre les types d’objets WinRT basés sur le Web et équivalents.</span><span class="sxs-lookup"><span data-stu-id="f3240-158">The [MSApp](./reference/msapp.md) global object \(`window.MSApp`\) provides assorted helper functions for JavaScript-based Windows 10 apps, such as utilities for converting between web standards-based and equivalent WinRT object types.</span></span>  