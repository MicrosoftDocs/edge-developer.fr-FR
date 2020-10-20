---
description: Héberger du contenu Web dans vos applications Win32, .NET et UWP avec le contrôle Microsoft Edge WebView2
title: Contrôle Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, contrôle de navigateur, HTML de bord, Windows Forms, WinForms, WPF, .NET, WinUI, Project REUNION
ms.openlocfilehash: 412ff112ab0eed69b63316b2916f849a32196363
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120374"
---
# <span data-ttu-id="9f41a-104">Introduction à Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="9f41a-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="9f41a-105">Le contrôle Microsoft Edge WebView2 vous permet d’incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives.</span><span class="sxs-lookup"><span data-stu-id="9f41a-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="9f41a-106">Le contrôle WebView2 utilise [Microsoft Edge (chrome)][MicrosoftedgeinsiderMain] comme moteur de rendu pour afficher le contenu Web dans les applications natives.</span><span class="sxs-lookup"><span data-stu-id="9f41a-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="9f41a-107">Avec WebView2, vous pouvez incorporer du code Web dans différentes parties de votre application native, ou générer l’application native entière au sein d’un seul WebView.</span><span class="sxs-lookup"><span data-stu-id="9f41a-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="9f41a-108">Pour plus d’informations sur la création d’une application WebView2, accédez à la section [commencer](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="9f41a-108">For information on how to start building a WebView2 application, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Présentation de WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="9f41a-110">Présentation de WebView</span><span class="sxs-lookup"><span data-stu-id="9f41a-110">What is WebView</span></span>  
:::image-end:::  

## <span data-ttu-id="9f41a-111">Approche hybride des applications</span><span class="sxs-lookup"><span data-stu-id="9f41a-111">Hybrid application approach</span></span>  

<span data-ttu-id="9f41a-112">Les développeurs doivent souvent choisir entre le bâtiment d’une application Web ou une application native.</span><span class="sxs-lookup"><span data-stu-id="9f41a-112">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="9f41a-113">La décision repose sur le compromis entre la portée et la puissance.</span><span class="sxs-lookup"><span data-stu-id="9f41a-113">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="9f41a-114">Les applications Web permettent d’offrir une large portée.</span><span class="sxs-lookup"><span data-stu-id="9f41a-114">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="9f41a-115">En tant que développeur Web, vous pouvez réutiliser la majeure partie de votre code, si ce n’est l’intégralité de votre code, sur toutes les différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="9f41a-115">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="9f41a-116">Toutefois, les applications natives utilisent les fonctionnalités de la plateforme Native entière.</span><span class="sxs-lookup"><span data-stu-id="9f41a-116">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Présentation de WebView" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="9f41a-118">Web natif</span><span class="sxs-lookup"><span data-stu-id="9f41a-118">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="9f41a-119">Les applications hybrides permettent aux développeurs de profiter au mieux de ces deux mondes.</span><span class="sxs-lookup"><span data-stu-id="9f41a-119">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="9f41a-120">Les développeurs d’applications hybrides profitent de l’omniprésence et de la puissance de la plateforme Web, ainsi que des fonctionnalités puissantes et complètes de la plateforme native.</span><span class="sxs-lookup"><span data-stu-id="9f41a-120">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="9f41a-121">Avantages de WebView2</span><span class="sxs-lookup"><span data-stu-id="9f41a-121">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Présentation de WebView" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="9f41a-123">Raisons de WebView</span><span class="sxs-lookup"><span data-stu-id="9f41a-123">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-124">& compétences du Web</span><span class="sxs-lookup"><span data-stu-id="9f41a-124">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="9f41a-125">Utiliser l’intégralité de la plateforme Web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème Web.</span><span class="sxs-lookup"><span data-stu-id="9f41a-125">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-126">Innovation rapide</span><span class="sxs-lookup"><span data-stu-id="9f41a-126">Rapid innovation</span></span>**  
      <span data-ttu-id="9f41a-127">Le développement Web permet d’accélérer le déploiement et l’itération.</span><span class="sxs-lookup"><span data-stu-id="9f41a-127">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-128">Prise en charge de Windows 7, 8 et 10</span><span class="sxs-lookup"><span data-stu-id="9f41a-128">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="9f41a-129">La prise en charge d’une interface utilisateur homogène dans Windows 7, 8 et 10.</span><span class="sxs-lookup"><span data-stu-id="9f41a-129">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-130">Fonctionnalités natives</span><span class="sxs-lookup"><span data-stu-id="9f41a-130">Native capabilities</span></span>**  
      <span data-ttu-id="9f41a-131">Accédez à l’ensemble complet d’API natives.</span><span class="sxs-lookup"><span data-stu-id="9f41a-131">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-132">Partage de code</span><span class="sxs-lookup"><span data-stu-id="9f41a-132">Code-sharing</span></span>**  
      <span data-ttu-id="9f41a-133">L’ajout d’un code Web à votre code base permet une réutilisation accrue sur plusieurs plates-formes.</span><span class="sxs-lookup"><span data-stu-id="9f41a-133">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-134">Support Microsoft</span><span class="sxs-lookup"><span data-stu-id="9f41a-134">Microsoft support</span></span>**  
      <span data-ttu-id="9f41a-135">Microsoft prend en charge l’assistance et ajoute de nouvelles demandes de fonctionnalité lorsque WebView2 est commercialisé en tant que GA.</span><span class="sxs-lookup"><span data-stu-id="9f41a-135">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-136">Distribution persistant</span><span class="sxs-lookup"><span data-stu-id="9f41a-136">Evergreen distribution</span></span>**  
      <span data-ttu-id="9f41a-137">S’appuyer sur une version de chrome à jour avec les mises à jour de plateforme et les correctifs de sécurité normaux.</span><span class="sxs-lookup"><span data-stu-id="9f41a-137">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9f41a-138">**Corrigé** \ (bientôt disponible)</span><span class="sxs-lookup"><span data-stu-id="9f41a-138">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="9f41a-139">Choisissez de conditionner les bits de chrome dans votre application.</span><span class="sxs-lookup"><span data-stu-id="9f41a-139">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9f41a-140">Adoption incrémentielle</span><span class="sxs-lookup"><span data-stu-id="9f41a-140">Incremental adoption</span></span>**  
      <span data-ttu-id="9f41a-141">Ajoutez des composants WebPart à votre application.</span><span class="sxs-lookup"><span data-stu-id="9f41a-141">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="9f41a-142">Prise en main</span><span class="sxs-lookup"><span data-stu-id="9f41a-142">Getting started</span></span>  

<span data-ttu-id="9f41a-143">Pour générer et tester votre application à l’aide du contrôle WebView2, vous devez disposer de [Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] et du [SDK WebView2][NugetPackagesMicrosoftWebWebView2] .</span><span class="sxs-lookup"><span data-stu-id="9f41a-143">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="9f41a-144">Pour commencer, sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f41a-144">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="9f41a-145">Commencer à utiliser Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="9f41a-145">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="9f41a-146">Mise en route de WPF</span><span class="sxs-lookup"><span data-stu-id="9f41a-146">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="9f41a-147">Mise en route de WinForms</span><span class="sxs-lookup"><span data-stu-id="9f41a-147">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="9f41a-148">Commencer à utiliser WinUI3</span><span class="sxs-lookup"><span data-stu-id="9f41a-148">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="9f41a-149">Le référentiel d' [exemples WebView2][GithubMicrosoftedgeWebview2samples] contient des exemples qui illustrent l’ensemble des fonctionnalités du SDK WebView2 et des modèles d’utilisation de l’API.</span><span class="sxs-lookup"><span data-stu-id="9f41a-149">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="9f41a-150">À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications seront mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9f41a-150">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="9f41a-151">Plateformes prises en charge</span><span class="sxs-lookup"><span data-stu-id="9f41a-151">Supported platforms</span></span>  

<span data-ttu-id="9f41a-152">Une disponibilité générale (GA \) ou version d’évaluation est disponible sur les environnements de programmation suivants.</span><span class="sxs-lookup"><span data-stu-id="9f41a-152">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="9f41a-153">Win32 C/C++ \ (GA \)</span><span class="sxs-lookup"><span data-stu-id="9f41a-153">Win32 C/C++ \(GA\)</span></span>
*   <span data-ttu-id="9f41a-154">.NET Framework 4.6.2 ou version ultérieure \ (Preview \)</span><span class="sxs-lookup"><span data-stu-id="9f41a-154">.NET Framework 4.6.2 or later \(Preview\)</span></span> 
*   <span data-ttu-id="9f41a-155">.NET Core 3,0 ou version ultérieure \ (Preview \)</span><span class="sxs-lookup"><span data-stu-id="9f41a-155">.NET Core 3.0 or later \(Preview\)</span></span>
*   <span data-ttu-id="9f41a-156">[WinUI 3,0][UwpToolkitsWinui3] \ (Preview \)</span><span class="sxs-lookup"><span data-stu-id="9f41a-156">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>

<span data-ttu-id="9f41a-157">Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f41a-157">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="9f41a-158">Windows10</span><span class="sxs-lookup"><span data-stu-id="9f41a-158">Windows 10</span></span>  
*   <span data-ttu-id="9f41a-159">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9f41a-159">Windows 8.1</span></span>  
*   <span data-ttu-id="9f41a-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="9f41a-160">Windows 8</span></span>  
*   <span data-ttu-id="9f41a-161">Windows7</span><span class="sxs-lookup"><span data-stu-id="9f41a-161">Windows 7</span></span>  
*   <span data-ttu-id="9f41a-162">Windows Server2019</span><span class="sxs-lookup"><span data-stu-id="9f41a-162">Windows Server 2019</span></span>  
*   <span data-ttu-id="9f41a-163">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="9f41a-163">Windows Server 2016</span></span>  
*   <span data-ttu-id="9f41a-164">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="9f41a-164">Windows Server 2012</span></span>  
*   <span data-ttu-id="9f41a-165">Windows Server 2012R2</span><span class="sxs-lookup"><span data-stu-id="9f41a-165">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="9f41a-166">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="9f41a-166">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="9f41a-167">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9f41a-167">Next steps</span></span>  

<span data-ttu-id="9f41a-168">Pour plus d’informations sur la création et le déploiement d’applications WebView2, voir la documentation conceptuelle et les guides de procédures.</span><span class="sxs-lookup"><span data-stu-id="9f41a-168">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="9f41a-169">Concepts</span><span class="sxs-lookup"><span data-stu-id="9f41a-169">Concepts</span></span>  

*   [<span data-ttu-id="9f41a-170">Comprendre les versions de kit de développement logiciel WebView2</span><span class="sxs-lookup"><span data-stu-id="9f41a-170">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="9f41a-171">Distribution d’applications à l’aide de WebView2</span><span class="sxs-lookup"><span data-stu-id="9f41a-171">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="9f41a-172">Recommandations en matière de développement d’applications WebView2 sécurisées</span><span class="sxs-lookup"><span data-stu-id="9f41a-172">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="9f41a-173">Gérer le dossier des données utilisateur dans les applications WebView2</span><span class="sxs-lookup"><span data-stu-id="9f41a-173">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="9f41a-174">Guides de How-To</span><span class="sxs-lookup"><span data-stu-id="9f41a-174">How-To guides</span></span>  

*   [<span data-ttu-id="9f41a-175">Comment déboguer avec WebView2</span><span class="sxs-lookup"><span data-stu-id="9f41a-175">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="9f41a-176">Automatisation et test de WebView2 avec le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9f41a-176">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="9f41a-177">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9f41a-177">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Recommandations en matière de développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Gestion du dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Mise en route de WebView2 | Documents Microsoft"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Commencer à utiliser WebView2 dans les applications Windows Forms (Preview) | Documents Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Commencer à utiliser WebView2 dans WinUI3 (Preview) | Documents Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Commencer à utiliser WebView2 dans WPF (Preview) | Documents Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Comment déboguer avec WebView2 | Documents Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisation et test de WebView2 avec le pilote Microsoft Edge | Documents Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Windows UI Library 3 Preview 2 (2020 de juillet) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galerie NuGet"  
