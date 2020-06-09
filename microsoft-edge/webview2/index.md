---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Contrôle Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: 1b140d9f644c7a864cac4966bb4cfdd400feeb0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697741"
---
# <span data-ttu-id="fb7d2-104">Introduction à Microsoft Edge WebView2 (Preview)</span><span class="sxs-lookup"><span data-stu-id="fb7d2-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="fb7d2-105">Le contrôle Microsoft Edge WebView2 vous permet d’incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="fb7d2-106">Le contrôle WebView2 utilise [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com) comme moteur de rendu pour afficher le contenu Web dans les applications natives.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-106">The WebView2 control uses [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com) as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="fb7d2-107">Avec WebView2, vous pouvez incorporer du code Web dans différentes parties de votre application native, ou générer l’application native entière au sein d’un seul WebView.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="fb7d2-108">Pour plus d’informations sur la création d’une application WebView2, voir [commencer.](./index.md#getting-started)</span><span class="sxs-lookup"><span data-stu-id="fb7d2-108">For information on how to start building a WebView2 application, see [Get Started](./index.md#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Présentation de WebView":::
   <span data-ttu-id="fb7d2-110">Présentation de WebView</span><span class="sxs-lookup"><span data-stu-id="fb7d2-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="fb7d2-111">La version préliminaire de WebView2 est conçue pour le prototype initial et rassembler des commentaires pour vous aider à établir la forme de l’API.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help to shape the API.</span></span>  <span data-ttu-id="fb7d2-112">L’équipe WebView de Microsoft Edge ne recommande pas d’utiliser l’aperçu dans vos applications de production en raison de [modifications éventuelles](./releasenotes.md).</span><span class="sxs-lookup"><span data-stu-id="fb7d2-112">The Microsoft Edge WebView team does not recommend that you use the preview in your production apps because there may be [breaking changes](./releasenotes.md).</span></span>  

## <span data-ttu-id="fb7d2-113">Approche hybride des applications</span><span class="sxs-lookup"><span data-stu-id="fb7d2-113">Hybrid application approach</span></span>  

<span data-ttu-id="fb7d2-114">Les développeurs doivent souvent choisir entre créer une application Web ou une application native.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-114">Developers often have to choose between building a web application or a native application.</span></span>  <span data-ttu-id="fb7d2-115">La décision repose sur le compromis entre la portée et la puissance.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-115">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="fb7d2-116">Les applications Web permettent d’offrir une large portée.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-116">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="fb7d2-117">En tant que développeur Web, vous pouvez réutiliser la majeure partie de votre code, si ce n’est l’intégralité de votre code, sur toutes les différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-117">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="fb7d2-118">Toutefois, les applications natives utilisent les fonctionnalités de la plateforme Native entière.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-118">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web natif":::
   <span data-ttu-id="fb7d2-120">Web natif</span><span class="sxs-lookup"><span data-stu-id="fb7d2-120">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="fb7d2-121">Les applications hybrides permettent aux développeurs de profiter au mieux de ces deux mondes.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-121">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="fb7d2-122">Les développeurs d’applications hybrides profitent de l’omniprésence et de la puissance de la plateforme Web, ainsi que des fonctionnalités puissantes et complètes de la plateforme native.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-122">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="fb7d2-123">Avantages de WebView2</span><span class="sxs-lookup"><span data-stu-id="fb7d2-123">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Raisons de WebView":::
   <span data-ttu-id="fb7d2-125">Raisons de WebView</span><span class="sxs-lookup"><span data-stu-id="fb7d2-125">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-126">& compétences du Web</span><span class="sxs-lookup"><span data-stu-id="fb7d2-126">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="fb7d2-127">Utiliser l’intégralité de la plateforme Web, des bibliothèques, des outils et des talents qui existent au sein de l’écosystème Web.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-127">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-128">Innovation rapide</span><span class="sxs-lookup"><span data-stu-id="fb7d2-128">Rapid innovation</span></span>**  
      <span data-ttu-id="fb7d2-129">Le développement Web permet d’accélérer le déploiement et l’itération.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-130">Prise en charge de Windows 7, 8 et 10</span><span class="sxs-lookup"><span data-stu-id="fb7d2-130">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="fb7d2-131">La prise en charge d’une interface utilisateur homogène dans Windows 7, 8 et 10.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-131">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-132">Fonctionnalités natives</span><span class="sxs-lookup"><span data-stu-id="fb7d2-132">Native capabilities</span></span>**  
      <span data-ttu-id="fb7d2-133">Accédez à l’ensemble complet d’API natives.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-133">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-134">Partage de code</span><span class="sxs-lookup"><span data-stu-id="fb7d2-134">Code-sharing</span></span>**  
      <span data-ttu-id="fb7d2-135">L’ajout d’un code Web à votre code base permet une réutilisation accrue sur plusieurs plates-formes.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-135">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-136">Support Microsoft</span><span class="sxs-lookup"><span data-stu-id="fb7d2-136">Microsoft support</span></span>**  
      <span data-ttu-id="fb7d2-137">Microsoft prend en charge l’assistance et ajoute de nouvelles demandes de fonctionnalité lorsque WebView2 est commercialisé en tant que GA.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-137">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-138">Distribution persistant</span><span class="sxs-lookup"><span data-stu-id="fb7d2-138">Evergreen distribution</span></span>**  
      <span data-ttu-id="fb7d2-139">S’appuyer sur une version de chrome à jour avec les mises à jour de plateforme et les correctifs de sécurité normaux.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-139">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="fb7d2-140">**Corrigé** \ (bientôt disponible)</span><span class="sxs-lookup"><span data-stu-id="fb7d2-140">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="fb7d2-141">Choisissez de conditionner les bits de chrome dans votre application.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-141">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="fb7d2-142">Adoption incrémentielle</span><span class="sxs-lookup"><span data-stu-id="fb7d2-142">Incremental adoption</span></span>**  
      <span data-ttu-id="fb7d2-143">Ajoutez des composants WebPart à votre application.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-143">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="fb7d2-144">Prise en main</span><span class="sxs-lookup"><span data-stu-id="fb7d2-144">Getting started</span></span>  

<span data-ttu-id="fb7d2-145">Pour générer et tester votre application à l’aide du contrôle WebView2, vous devez disposer de [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download) et du [SDK WebView2](https://aka.ms/webviewnuget) .</span><span class="sxs-lookup"><span data-stu-id="fb7d2-145">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download) and the [WebView2 SDK](https://aka.ms/webviewnuget) installed.</span></span>  <span data-ttu-id="fb7d2-146">Pour commencer, sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="fb7d2-147">Commencer à utiliser Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="fb7d2-147">Getting Started with Win32 C/C++</span></span>](./gettingstarted/win32.md)  
*   [<span data-ttu-id="fb7d2-148">Mise en route de WPF</span><span class="sxs-lookup"><span data-stu-id="fb7d2-148">Getting Started with WPF</span></span>](./gettingstarted/wpf.md)  
*   [<span data-ttu-id="fb7d2-149">Mise en route de WinForms</span><span class="sxs-lookup"><span data-stu-id="fb7d2-149">Getting Started with WinForms</span></span>](./gettingstarted/winforms.md)  

<span data-ttu-id="fb7d2-150">Le référentiel d' [exemples WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contient des exemples qui illustrent l’ensemble des fonctionnalités du SDK WebView2 et des modèles d’utilisation de l’API.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-150">The [WebView2 Samples](https://github.com/MicrosoftEdge/WebView2Samples) repository contains samples that demonstrate all of the WebView2 SDKs features and API usage patterns.</span></span> <span data-ttu-id="fb7d2-151">À mesure que d’autres fonctionnalités sont ajoutées au SDK WebView2, les exemples d’applications seront mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-151">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>   

## <span data-ttu-id="fb7d2-152">Plateformes prises en charge</span><span class="sxs-lookup"><span data-stu-id="fb7d2-152">Supported platforms</span></span>  

<span data-ttu-id="fb7d2-153">Un aperçu du développeur est disponible sur les environnements de programmation suivants.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-153">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="fb7d2-154">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="fb7d2-154">Win32 C/C++</span></span>  
*   <span data-ttu-id="fb7d2-155">.NET Framework 4.6.2 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fb7d2-155">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="fb7d2-156">.NET Core 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fb7d2-156">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="fb7d2-157">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="fb7d2-157">WinUI 3.0</span></span>](/uwp/toolkits/winui3/)  

<span data-ttu-id="fb7d2-158">Vous pouvez exécuter des applications WebView2 sur les versions suivantes de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-158">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="fb7d2-159">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fb7d2-159">Windows 10</span></span>  
*   <span data-ttu-id="fb7d2-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fb7d2-160">Windows 8.1</span></span>  
*   <span data-ttu-id="fb7d2-161">Windows8</span><span class="sxs-lookup"><span data-stu-id="fb7d2-161">Windows 8</span></span>  
*   <span data-ttu-id="fb7d2-162">Windows7</span><span class="sxs-lookup"><span data-stu-id="fb7d2-162">Windows 7</span></span>  
*   <span data-ttu-id="fb7d2-163">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="fb7d2-163">Windows Server 2016</span></span>  
*   <span data-ttu-id="fb7d2-164">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="fb7d2-164">Windows Server 2012</span></span>  
*   <span data-ttu-id="fb7d2-165">Windows Server 2012R2</span><span class="sxs-lookup"><span data-stu-id="fb7d2-165">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="fb7d2-166">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="fb7d2-166">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="fb7d2-167">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fb7d2-167">Next steps</span></span>  

<span data-ttu-id="fb7d2-168">Pour obtenir des informations plus détaillées sur la création et le déploiement d’applications WebView2, consultez la documentation conceptuelle et les guides de procédures.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-168">For more detailed information on how to build and deploy WebView2 applications, checkout the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="fb7d2-169">Concepts</span><span class="sxs-lookup"><span data-stu-id="fb7d2-169">Concepts</span></span>  

*   [<span data-ttu-id="fb7d2-170">Kit de développement logiciel (SDK) WebView2 et contrôle de version Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fb7d2-170">WebView2 SDK and Microsoft Edge versioning</span></span>](./concepts/versioning.md)
*   [<span data-ttu-id="fb7d2-171">Distribution d’applications WebView2</span><span class="sxs-lookup"><span data-stu-id="fb7d2-171">Distributing WebView2 applications</span></span>](./concepts/distribution.md)  
 
#### <span data-ttu-id="fb7d2-172">Guides de procédure</span><span class="sxs-lookup"><span data-stu-id="fb7d2-172">How-To guides</span></span>  

*   [<span data-ttu-id="fb7d2-173">Débogage de WebView2 avec DevTools et le débogage de script Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb7d2-173">Debugging WebView2 with DevTools and Visual Studio script debugging</span></span>](./howto/debug.md)  
*   [<span data-ttu-id="fb7d2-174">Automatisation et débogage de WebView2 avec Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="fb7d2-174">Automating and debugging WebView2 with Microsoft EdgeDriver</span></span>](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## <span data-ttu-id="fb7d2-175">Contacter l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="fb7d2-175">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="fb7d2-176">Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-176">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="fb7d2-177">Rendez-vous sur le site Web de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-177">Visit the WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  <span data-ttu-id="fb7d2-178">C’est également le bon endroit où rechercher des problèmes connus.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-178">It is also a good place to search for known issues.</span></span>  

> [!NOTE]
> <span data-ttu-id="fb7d2-179">Dans le cadre de l’aperçu du développeur, l’équipe WebView Microsoft Edge recueille également des données pour vous aider à créer un meilleur affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-179">During developer preview, the Microsoft Edge WebView team also collects data to help build a better WebView.</span></span>  <span data-ttu-id="fb7d2-180">Les utilisateurs peuvent désactiver la collecte des données de WebView en naviguant `edge://settings/privacy` dans le navigateur Microsoft Edge et en désactivant la collecte des données du navigateur.</span><span class="sxs-lookup"><span data-stu-id="fb7d2-180">Users may turn off WebView data collection by navigating to `edge://settings/privacy` in the Microsoft Edge browser and turning off browser data collection.</span></span>  
