---
description: Héberger du contenu web dans vos applications Win32, .NET et UWP avec le Microsoft Edge WebView2
title: Microsoft Edge Contrôle WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Réunion
ms.openlocfilehash: 64c835d0122a1c72e610efed2c060f7921a8e2b5
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627984"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="9dae5-104">Présentation de Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="9dae5-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="9dae5-105">Le Microsoft Edge WebView2 vous permet d’incorporer des technologies web \(HTML, CSS et JavaScript\) dans vos applications natives.</span><span class="sxs-lookup"><span data-stu-id="9dae5-105">The Microsoft Edge WebView2 control allows you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="9dae5-106">Le contrôle WebView2 utilise [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] comme moteur de rendu pour afficher le contenu web dans les applications natives.</span><span class="sxs-lookup"><span data-stu-id="9dae5-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="9dae5-107">Avec WebView2, vous pouvez incorporer du code web dans différentes parties de votre application native.</span><span class="sxs-lookup"><span data-stu-id="9dae5-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="9dae5-108">Créez l’ensemble de l’application native au sein d’une instance WebView unique.</span><span class="sxs-lookup"><span data-stu-id="9dae5-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="9dae5-109">Pour plus d’informations sur la création d’une application WebView2, accédez [à Prise en main](#get-started).</span><span class="sxs-lookup"><span data-stu-id="9dae5-109">For information on how to start building a WebView2 app, navigate to [Get Started](#get-started).</span></span>  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="Qu’est-ce que WebView ?" lightbox="./media/WebView2/what-webview.png":::
   <span data-ttu-id="9dae5-111">Qu’est-ce que WebView ?</span><span class="sxs-lookup"><span data-stu-id="9dae5-111">What is WebView?</span></span>  
:::image-end:::    

## <a name="hybrid-app-approach"></a><span data-ttu-id="9dae5-112">Approche de l’application hybride</span><span class="sxs-lookup"><span data-stu-id="9dae5-112">Hybrid app approach</span></span>  

<span data-ttu-id="9dae5-113">Les développeurs doivent souvent décider entre la création d’une application web ou d’une application native.</span><span class="sxs-lookup"><span data-stu-id="9dae5-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="9dae5-114">La décision porte sur le compromis entre la portée et la puissance.</span><span class="sxs-lookup"><span data-stu-id="9dae5-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="9dae5-115">Les applications web permettent une large portée.</span><span class="sxs-lookup"><span data-stu-id="9dae5-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="9dae5-116">En tant que développeur Web, vous pouvez réutiliser la plupart de votre code sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="9dae5-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="9dae5-117">Pour accéder à toutes les fonctionnalités d’une plateforme native, utilisez une application native.</span><span class="sxs-lookup"><span data-stu-id="9dae5-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Web natif" lightbox="./media/WebView2/web-native.png":::
   <span data-ttu-id="9dae5-119">Web natif</span><span class="sxs-lookup"><span data-stu-id="9dae5-119">Web native</span></span>  
:::image-end:::    

<span data-ttu-id="9dae5-120">Les applications hybrides permettent aux développeurs de profiter du meilleur des deux mondes.</span><span class="sxs-lookup"><span data-stu-id="9dae5-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="9dae5-121">Les développeurs d’applications hybrides bénéficient des avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="9dae5-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="9dae5-122">L’omniprésence et la force de la plateforme web.</span><span class="sxs-lookup"><span data-stu-id="9dae5-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="9dae5-123">Puissance et fonctionnalités complètes de la plateforme native.</span><span class="sxs-lookup"><span data-stu-id="9dae5-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="9dae5-124">Avantages de WebView2</span><span class="sxs-lookup"><span data-stu-id="9dae5-124">WebView2 benefits</span></span>   

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="web-ecosystem--skillset"></a><span data-ttu-id="9dae5-125">Écosystème web & compétences</span><span class="sxs-lookup"><span data-stu-id="9dae5-125">Web ecosystem & skillset</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a><span data-ttu-id="9dae5-126">Innovation rapide</span><span class="sxs-lookup"><span data-stu-id="9dae5-126">Rapid innovation</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a><span data-ttu-id="9dae5-127">Windows 7, 8 et 10</span><span class="sxs-lookup"><span data-stu-id="9dae5-127">Windows 7, 8, and 10 support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9dae5-128">Utilisez l’ensemble de la plateforme web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème web.</span><span class="sxs-lookup"><span data-stu-id="9dae5-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9dae5-129">Le développement Web permet un déploiement et une itération plus rapides.</span><span class="sxs-lookup"><span data-stu-id="9dae5-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9dae5-130">Prise en charge d’une expérience utilisateur cohérente entre Windows 7, Windows 8 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9dae5-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="native-capabilities"></a><span data-ttu-id="9dae5-131">Fonctionnalités natives</span><span class="sxs-lookup"><span data-stu-id="9dae5-131">Native capabilities</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a><span data-ttu-id="9dae5-132">Partage de code</span><span class="sxs-lookup"><span data-stu-id="9dae5-132">Code-sharing</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a><span data-ttu-id="9dae5-133">Support Microsoft</span><span class="sxs-lookup"><span data-stu-id="9dae5-133">Microsoft support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9dae5-134">Accéder à l’ensemble complet des API natives.</span><span class="sxs-lookup"><span data-stu-id="9dae5-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9dae5-135">L’ajout de code web à votre codebase permet une réutilisation accrue sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="9dae5-135">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9dae5-136">Microsoft fournit une prise en charge et ajoute de nouvelles demandes de fonctionnalités lorsque WebView2 est publié à la disponibilité générale \(GA\).</span><span class="sxs-lookup"><span data-stu-id="9dae5-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="evergreen-distribution"></a><span data-ttu-id="9dae5-137">Distribution persistante</span><span class="sxs-lookup"><span data-stu-id="9dae5-137">Evergreen distribution</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a><span data-ttu-id="9dae5-138">Résolu</span><span class="sxs-lookup"><span data-stu-id="9dae5-138">Fixed</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a><span data-ttu-id="9dae5-139">Adoption incrémentielle</span><span class="sxs-lookup"><span data-stu-id="9dae5-139">Incremental adoption</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9dae5-140">Reposez-vous sur une version à jour de Chromium avec des mises à jour de plateforme régulières et des correctifs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9dae5-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9dae5-141">\(bientôt disponible\) Choisissez d’Chromium bits dans votre application.</span><span class="sxs-lookup"><span data-stu-id="9dae5-141">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9dae5-142">Ajoutez des composants web, pièce par élément, à votre application.</span><span class="sxs-lookup"><span data-stu-id="9dae5-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a><span data-ttu-id="9dae5-143">Prise en main</span><span class="sxs-lookup"><span data-stu-id="9dae5-143">Get started</span></span>  

<span data-ttu-id="9dae5-144">Pour créer et tester votre application à l’aide du contrôle WebView2, vous devez avoir</span><span class="sxs-lookup"><span data-stu-id="9dae5-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="9dae5-145">Le [SDK WebView2][NugetPackagesMicrosoftWebWebView2] est installé.</span><span class="sxs-lookup"><span data-stu-id="9dae5-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="9dae5-146">Sélectionnez l’une des options suivantes pour commencer.</span><span class="sxs-lookup"><span data-stu-id="9dae5-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="9dae5-147">Prise en main avec Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="9dae5-147">Get Started with Win32 C/C++</span></span>][Webview2GetStartedWin32]  
*   [<span data-ttu-id="9dae5-148">Prise en main avec WPF</span><span class="sxs-lookup"><span data-stu-id="9dae5-148">Get Started with WPF</span></span>][Webview2GetStartedWpf]  
*   [<span data-ttu-id="9dae5-149">Prise en main avec WinForms</span><span class="sxs-lookup"><span data-stu-id="9dae5-149">Get Started with WinForms</span></span>][Webview2GetStartedWinforms]  
*   [<span data-ttu-id="9dae5-150">Prise en main avec WinUI3</span><span class="sxs-lookup"><span data-stu-id="9dae5-150">Get Started with WinUI3</span></span>][Webview2GetStartedWinui]  
    
<span data-ttu-id="9dae5-151">Le [référentiel WebView2 Samples][GithubMicrosoftedgeWebview2samples] contient des exemples qui montrent toutes les fonctionnalités du SDK WebView2 et les modèles d’utilisation des API.</span><span class="sxs-lookup"><span data-stu-id="9dae5-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="9dae5-152">À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9dae5-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="9dae5-153">Plateformes prises en charge</span><span class="sxs-lookup"><span data-stu-id="9dae5-153">Supported platforms</span></span>  

<span data-ttu-id="9dae5-154">Une version De disponibilité générale \(GA\) ou Aperçu est disponible dans les environnements de programmation suivants.</span><span class="sxs-lookup"><span data-stu-id="9dae5-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="9dae5-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="9dae5-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="9dae5-156">.NET Framework 4.5 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9dae5-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="9dae5-157">.NET Core 3.1 ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="9dae5-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="9dae5-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="9dae5-158">.NET 5</span></span>  
*   <span data-ttu-id="9dae5-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="9dae5-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  
    
<span data-ttu-id="9dae5-160">Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.</span><span class="sxs-lookup"><span data-stu-id="9dae5-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="9dae5-161">Windows10</span><span class="sxs-lookup"><span data-stu-id="9dae5-161">Windows 10</span></span>  
*   <span data-ttu-id="9dae5-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9dae5-162">Windows 8.1</span></span>  
*   <span data-ttu-id="9dae5-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="9dae5-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="9dae5-164">Windows Server2019</span><span class="sxs-lookup"><span data-stu-id="9dae5-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="9dae5-165">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="9dae5-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="9dae5-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9dae5-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="9dae5-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9dae5-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="9dae5-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="9dae5-168">Windows Server 2008 R2 \*\*</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="9dae5-169">La prise en charge de \*\* WebView2 pour Windows 7 et Windows Server 2008 R2 possède le même cycle de prise en charge que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9dae5-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="9dae5-170">Pour plus d’informations, [accédez à Microsoft Edge systèmes d’exploitation pris en charge.][DeployedgeMicrosoftEdgeSupportedOS]</span><span class="sxs-lookup"><span data-stu-id="9dae5-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="9dae5-171">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9dae5-171">Next steps</span></span>  

<span data-ttu-id="9dae5-172">Pour plus d’informations sur la façon de créer et de déployer des applications WebView2, examinez la documentation conceptuelle et les guides de pratiques.</span><span class="sxs-lookup"><span data-stu-id="9dae5-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

### <a name="concepts"></a><span data-ttu-id="9dae5-173">Concepts</span><span class="sxs-lookup"><span data-stu-id="9dae5-173">Concepts</span></span>  

*   [<span data-ttu-id="9dae5-174">Comprendre les versions du SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="9dae5-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="9dae5-175">Distribution d’applications à l’aide de WebView2</span><span class="sxs-lookup"><span data-stu-id="9dae5-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="9dae5-176">Meilleures pratiques pour le développement d’applications WebView2 sécurisées</span><span class="sxs-lookup"><span data-stu-id="9dae5-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="9dae5-177">Gérer le dossier de données utilisateur dans les applications WebView2</span><span class="sxs-lookup"><span data-stu-id="9dae5-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a><span data-ttu-id="9dae5-178">How-To guides</span><span class="sxs-lookup"><span data-stu-id="9dae5-178">How-To guides</span></span>  

*   [<span data-ttu-id="9dae5-179">Comment déboguer avec WebView2</span><span class="sxs-lookup"><span data-stu-id="9dae5-179">How to Debug with WebView2</span></span>][Webview2HowToDebug]  
*   [<span data-ttu-id="9dae5-180">Automatisation et test de WebView2 avec Microsoft Edge pilote</span><span class="sxs-lookup"><span data-stu-id="9dae5-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="9dae5-181">Entrer en contact avec l’équipe web Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="9dae5-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribution d’applications à l’aide de WebView2 | Documents Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Meilleures pratiques pour le développement d’applications WebView2 sécurisées | Documents Microsoft"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Gérer le dossier de données utilisateur | Documents Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprendre les versions du SDK WebView2 | Documents Microsoft"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Commencer à prendre en | WebView2 Documents Microsoft"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Mise en place de WebView2 dans Windows Forms (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Mise en place de WebView2 dans WinUI3 (prévisualisation) | Documents Microsoft"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Mise en place de WebView2 dans WPF (prévisualisation) | Documents Microsoft"  
[Webview2HowToDebug]: ./how-to/debug.md "Comment déboguer avec WebView2 | Documents Microsoft"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatisation et test de WebView2 avec Microsoft Edge driver | Documents Microsoft"  
[Webview2ReleaseNotes]: ./release-notes.md "Notes de publication du SDK WebView2 | Documents Microsoft"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (juillet 2020) | Documents Microsoft"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge systèmes d’exploitation pris en charge | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Galerie"  
