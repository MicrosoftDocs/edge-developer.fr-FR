---
description: Héberger du contenu web dans vos applications Win32, .NET et UWP avec le contrôle Microsoft Edge WebView2
title: Contrôle Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Réunion
ms.openlocfilehash: 501b6ed3694c66e4c0882550003e636d3b390108
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470777"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="cea44-104">Présentation de Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="cea44-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="cea44-105">Le contrôle Microsoft Edge WebView2 vous permet d’incorporer des technologies web \(HTML, CSS et JavaScript\) dans vos applications natives.</span><span class="sxs-lookup"><span data-stu-id="cea44-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="cea44-106">Le contrôle WebView2 utilise [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] comme moteur de rendu pour afficher le contenu web dans les applications natives.</span><span class="sxs-lookup"><span data-stu-id="cea44-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="cea44-107">Avec WebView2, vous pouvez incorporer du code web dans différentes parties de votre application native.</span><span class="sxs-lookup"><span data-stu-id="cea44-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="cea44-108">Créez l’ensemble de l’application native au sein d’une instance WebView unique.</span><span class="sxs-lookup"><span data-stu-id="cea44-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="cea44-109">Pour plus d’informations sur la création d’une application WebView2, accédez [à Démarrer.](#getting-started)</span><span class="sxs-lookup"><span data-stu-id="cea44-109">For information on how to start building a WebView2 app, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Qu’est-ce que WebView ?" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="cea44-111">Qu’est-ce que WebView ?</span><span class="sxs-lookup"><span data-stu-id="cea44-111">What is WebView?</span></span>  
:::image-end:::  

## <a name="hybrid-app-approach"></a><span data-ttu-id="cea44-112">Approche de l’application hybride</span><span class="sxs-lookup"><span data-stu-id="cea44-112">Hybrid app approach</span></span>  

<span data-ttu-id="cea44-113">Les développeurs doivent souvent décider entre la création d’une application web ou d’une application native.</span><span class="sxs-lookup"><span data-stu-id="cea44-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="cea44-114">La décision porte sur le compromis entre la portée et la puissance.</span><span class="sxs-lookup"><span data-stu-id="cea44-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="cea44-115">Les applications web permettent une large portée.</span><span class="sxs-lookup"><span data-stu-id="cea44-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="cea44-116">En tant que développeur Web, vous pouvez réutiliser la plupart de votre code sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="cea44-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="cea44-117">Pour accéder à toutes les fonctionnalités d’une plateforme native, utilisez une application native.</span><span class="sxs-lookup"><span data-stu-id="cea44-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web natif" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="cea44-119">Web natif</span><span class="sxs-lookup"><span data-stu-id="cea44-119">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="cea44-120">Les applications hybrides permettent aux développeurs de profiter du meilleur des deux mondes.</span><span class="sxs-lookup"><span data-stu-id="cea44-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="cea44-121">Les développeurs d’applications hybrides bénéficient des avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="cea44-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="cea44-122">L’omniprésence et la force de la plateforme web.</span><span class="sxs-lookup"><span data-stu-id="cea44-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="cea44-123">Puissance et fonctionnalités complètes de la plateforme native.</span><span class="sxs-lookup"><span data-stu-id="cea44-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="cea44-124">Avantages de WebView2</span><span class="sxs-lookup"><span data-stu-id="cea44-124">WebView2 benefits</span></span>   

<!--  
:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webviewreasons.png":::
   WebView reasons  
:::image-end:::  
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **<span data-ttu-id="cea44-125">Écosystème web \& compétences</span><span class="sxs-lookup"><span data-stu-id="cea44-125">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="cea44-126">Utilisez l’ensemble de la plateforme web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème web.</span><span class="sxs-lookup"><span data-stu-id="cea44-126">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **<span data-ttu-id="cea44-127">Innovation rapide</span><span class="sxs-lookup"><span data-stu-id="cea44-127">Rapid innovation</span></span>**  
      <span data-ttu-id="cea44-128">Le développement Web permet un déploiement et une itération plus rapides.</span><span class="sxs-lookup"><span data-stu-id="cea44-128">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **<span data-ttu-id="cea44-129">Prise en charge de Windows 7, 8 et 10</span><span class="sxs-lookup"><span data-stu-id="cea44-129">Windows 7, 8, and 10 support</span></span>**  
      <span data-ttu-id="cea44-130">Prise en charge d’une expérience utilisateur cohérente dans Windows 7, Windows 8 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cea44-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **<span data-ttu-id="cea44-131">Fonctionnalités natives</span><span class="sxs-lookup"><span data-stu-id="cea44-131">Native capabilities</span></span>**  
      <span data-ttu-id="cea44-132">Accéder à l’ensemble complet des API natives.</span><span class="sxs-lookup"><span data-stu-id="cea44-132">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **<span data-ttu-id="cea44-133">Partage de code</span><span class="sxs-lookup"><span data-stu-id="cea44-133">Code-sharing</span></span>**  
      <span data-ttu-id="cea44-134">L’ajout de code web à votre codebase permet une réutilisation accrue sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="cea44-134">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **<span data-ttu-id="cea44-135">Support Microsoft</span><span class="sxs-lookup"><span data-stu-id="cea44-135">Microsoft support</span></span>**  
      <span data-ttu-id="cea44-136">Microsoft fournit une prise en charge et ajoute de nouvelles demandes de fonctionnalités lorsque WebView2 est publié à la disponibilité générale \(GA\).</span><span class="sxs-lookup"><span data-stu-id="cea44-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **<span data-ttu-id="cea44-137">Distribution persistante</span><span class="sxs-lookup"><span data-stu-id="cea44-137">Evergreen distribution</span></span>**  
      <span data-ttu-id="cea44-138">Reposez-vous sur une version à jour de Chromium avec des mises à jour de plateforme régulières et des correctifs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cea44-138">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **<span data-ttu-id="cea44-139">Résolu</span><span class="sxs-lookup"><span data-stu-id="cea44-139">Fixed</span></span>**  
      <span data-ttu-id="cea44-140">\(bientôt disponible\) Choisissez de mettre en package les bits Chromium dans votre application.</span><span class="sxs-lookup"><span data-stu-id="cea44-140">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **<span data-ttu-id="cea44-141">Adoption incrémentielle</span><span class="sxs-lookup"><span data-stu-id="cea44-141">Incremental adoption</span></span>**  
      <span data-ttu-id="cea44-142">Ajoutez des composants web, pièce par élément, à votre application.</span><span class="sxs-lookup"><span data-stu-id="cea44-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="getting-started"></a><span data-ttu-id="cea44-143">Prise en main</span><span class="sxs-lookup"><span data-stu-id="cea44-143">Getting started</span></span>  

<span data-ttu-id="cea44-144">Pour créer et tester votre application à l’aide du contrôle WebView2, vous devez avoir</span><span class="sxs-lookup"><span data-stu-id="cea44-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="cea44-145">Le [SDK WebView2][NugetPackagesMicrosoftWebWebView2] est installé.</span><span class="sxs-lookup"><span data-stu-id="cea44-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="cea44-146">Sélectionnez l’une des options suivantes pour commencer.</span><span class="sxs-lookup"><span data-stu-id="cea44-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="cea44-147">Mise en place de Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="cea44-147">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="cea44-148">Mise en place de WPF</span><span class="sxs-lookup"><span data-stu-id="cea44-148">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="cea44-149">Mise en place de WinForms</span><span class="sxs-lookup"><span data-stu-id="cea44-149">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="cea44-150">Mise en place de WinUI3</span><span class="sxs-lookup"><span data-stu-id="cea44-150">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="cea44-151">Le [référentiel WebView2 Samples][GithubMicrosoftedgeWebview2samples] contient des exemples qui montrent toutes les fonctionnalités du SDK WebView2 et les modèles d’utilisation des API.</span><span class="sxs-lookup"><span data-stu-id="cea44-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="cea44-152">À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="cea44-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="cea44-153">Plateformes prises en charge</span><span class="sxs-lookup"><span data-stu-id="cea44-153">Supported platforms</span></span>  

<span data-ttu-id="cea44-154">Une version De disponibilité générale \(GA\) ou Aperçu est disponible dans les environnements de programmation suivants.</span><span class="sxs-lookup"><span data-stu-id="cea44-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="cea44-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="cea44-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="cea44-156">.NET Framework 4.6.2 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="cea44-156">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="cea44-157">.NET Core 3.1 ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="cea44-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="cea44-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="cea44-158">.NET 5</span></span>  
*   <span data-ttu-id="cea44-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="cea44-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="cea44-160">Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.</span><span class="sxs-lookup"><span data-stu-id="cea44-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="cea44-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cea44-161">Windows 10</span></span>  
*   <span data-ttu-id="cea44-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cea44-162">Windows 8.1</span></span>  
*   <span data-ttu-id="cea44-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="cea44-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="cea44-164">Windows Server2019</span><span class="sxs-lookup"><span data-stu-id="cea44-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="cea44-165">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="cea44-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="cea44-166">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="cea44-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="cea44-167">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="cea44-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="cea44-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="cea44-168">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cea44-169">La prise en charge de WebView2 pour Windows 7 et Windows Server 2008 R2 a le même cycle de prise en charge que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cea44-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="cea44-170">Pour plus d’informations, accédez aux [systèmes d’exploitation pris en charge par Microsoft Edge.][DeployedgeMicrosoftEdgeSupportedOS]</span><span class="sxs-lookup"><span data-stu-id="cea44-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="cea44-171">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cea44-171">Next steps</span></span>  

<span data-ttu-id="cea44-172">Pour plus d’informations sur la façon de créer et de déployer des applications WebView2, examinez la documentation conceptuelle et les guides de pratiques.</span><span class="sxs-lookup"><span data-stu-id="cea44-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

#### <a name="concepts"></a><span data-ttu-id="cea44-173">Concepts</span><span class="sxs-lookup"><span data-stu-id="cea44-173">Concepts</span></span>  

*   [<span data-ttu-id="cea44-174">Comprendre les versions du SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="cea44-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="cea44-175">Distribution d’applications à l’aide de WebView2</span><span class="sxs-lookup"><span data-stu-id="cea44-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="cea44-176">Meilleures pratiques pour le développement d’applications WebView2 sécurisées</span><span class="sxs-lookup"><span data-stu-id="cea44-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="cea44-177">Gérer le dossier de données utilisateur dans les applications WebView2</span><span class="sxs-lookup"><span data-stu-id="cea44-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserdatafolder]  
 
#### <a name="how-to-guides"></a><span data-ttu-id="cea44-178">How-To guides</span><span class="sxs-lookup"><span data-stu-id="cea44-178">How-To guides</span></span>  

*   [<span data-ttu-id="cea44-179">Comment déboguer avec WebView2</span><span class="sxs-lookup"><span data-stu-id="cea44-179">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="cea44-180">Automatisation et test de WebView2 avec le pilote Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cea44-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="cea44-181">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="cea44-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Meilleures pratiques pour le développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Gestion du dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Getting started with WebView2 | Documents Microsoft"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Mise en place de WebView2 dans les applications Windows Forms (prévisualisation) | Documents Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Getting started with WebView2 in WinUI3 (Preview) | Documents Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Getting started with WebView2 in WPF (Preview) | Documents Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Comment déboguer avec WebView2 | Documents Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisation et test de WebView2 avec le pilote Microsoft Edge | Documents Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (juillet 2020) | Documents Microsoft"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Systèmes d’exploitation pris en charge par Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | Galerie NuGet"  
