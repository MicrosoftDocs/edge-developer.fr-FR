---
description: Vue d’ensemble de la création et de la publication Microsoft Edge (Chromium) Extensions.
title: Vue d’ensemble Microsoft Edge (Chromium) extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur, extensions chromium
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327525"
---
# <span data-ttu-id="4fe5d-104">Vue d’ensemble Microsoft Edge (Chromium) extensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-104">Overview of Microsoft Edge (Chromium) Extensions</span></span>  

<span data-ttu-id="4fe5d-105">Une extension est un petit programme que vous \(un développeur\) utilisez pour ajouter ou modifier des fonctionnalités pour Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="4fe5d-105">An extension is a small program that you \(a developer\) use to add or modify features for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4fe5d-106">Une extension est destinée à améliorer l’expérience de navigation quotidienne d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-106">An extension is intended to improve a user's day-to-day browsing experience.</span></span>  <span data-ttu-id="4fe5d-107">Il fournit des fonctionnalités ciblées qui sont importantes pour un public cible.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-107">It provides niche functionality that is important to a target audience.</span></span>  

<span data-ttu-id="4fe5d-108">Vous pouvez créer une extension si vous avez une idée ou un produit basé sur l’une des conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-108">You may create an extension if you have an idea or product that is based upon either of the following conditions.</span></span>  

*   <span data-ttu-id="4fe5d-109">Navigateur web spécifique.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-109">A specific web browser.</span></span>  
*   <span data-ttu-id="4fe5d-110">Améliorations apportées aux fonctionnalités de pages web spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-110">Improvements to features of specific webpages.</span></span>  
    
<span data-ttu-id="4fe5d-111">Les bloqueurs de mots de passe et les gestionnaires de mots de passe sont des exemples d’expériences complémentaires.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-111">Examples of companion experiences include ad blockers and password managers.</span></span>  

<span data-ttu-id="4fe5d-112">Une extension est structurée comme une application web normale.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-112">An extension is structured similar to a regular web app.</span></span>  <span data-ttu-id="4fe5d-113">Au minimum, il doit inclure les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-113">At a minimum, it should include the following features.</span></span>

*   <span data-ttu-id="4fe5d-114">Fichier JSON de manifeste d’application qui contient des informations de plateforme de base.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-114">An app manifest JSON file that contains basic platform information.</span></span>  
*   <span data-ttu-id="4fe5d-115">Fichier JavaScript qui définit les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-115">A JavaScript file that define functionality.</span></span>  
*   <span data-ttu-id="4fe5d-116">Fichiers HTML et CSS qui définissent l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-116">HTML and CSS files that define the user interface.</span></span>  

<span data-ttu-id="4fe5d-117">Pour travailler directement avec une partie du navigateur, telle qu’une fenêtre ou un onglet, vous devez envoyer des demandes d’API et référencer souvent le navigateur par son nom.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-117">To work directly with part of the browser, such as a window or tab, you must send API requests and often reference the browser by name.</span></span>  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Une extension Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  <span data-ttu-id="4fe5d-119">Une extension Microsoft Edge \(Chromium\)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-119">A Microsoft Edge \(Chromium\) extension</span></span>  
:::image-end:::  

## <span data-ttu-id="4fe5d-120">Conseils de base</span><span class="sxs-lookup"><span data-stu-id="4fe5d-120">Basic guidance</span></span>  

<span data-ttu-id="4fe5d-121">Certains des navigateurs les plus populaires pour créer des extensions incluent Safari, Firefox, Chrome, Opera, Firefox et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-121">Some of the most popular browsers to build extensions for include Safari, Firefox, Chrome, Opera, Brave, and Microsoft Edge.</span></span>  <span data-ttu-id="4fe5d-122">L’emplacement idéal pour commencer vos didacticiels de développement d’extension et la recherche de documentation sont les sites hébergés par les organisations de navigateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-122">Great places to begin your extension development tutorials and documentation research are sites hosted by the browser organizations.</span></span>  <span data-ttu-id="4fe5d-123">Le tableau suivant n’est pas définitif et peut servir de point de départ.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-123">The following table isn't definitive, and may be used as a starting point.</span></span>  

| <span data-ttu-id="4fe5d-124">Navigateur web</span><span class="sxs-lookup"><span data-stu-id="4fe5d-124">Web browser</span></span> | <span data-ttu-id="4fe5d-125">Chromium base de données ?</span><span class="sxs-lookup"><span data-stu-id="4fe5d-125">Chromium-based?</span></span> | <span data-ttu-id="4fe5d-126">Page web de développement d’extensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-126">Extension development webpage</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4fe5d-127">Safari</span><span class="sxs-lookup"><span data-stu-id="4fe5d-127">Safari</span></span> | <span data-ttu-id="4fe5d-128">Non</span><span class="sxs-lookup"><span data-stu-id="4fe5d-128">No</span></span> | [<span data-ttu-id="4fe5d-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span></span>][AppleDeveloperSafariservicesAppExtensions] |  
| <span data-ttu-id="4fe5d-130">Firefox</span><span class="sxs-lookup"><span data-stu-id="4fe5d-130">Firefox</span></span> | <span data-ttu-id="4fe5d-131">Non</span><span class="sxs-lookup"><span data-stu-id="4fe5d-131">No</span></span> | [<span data-ttu-id="4fe5d-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span></span>][MDNWebextensions] |  
| <span data-ttu-id="4fe5d-133">Chrome</span><span class="sxs-lookup"><span data-stu-id="4fe5d-133">Chrome</span></span> | <span data-ttu-id="4fe5d-134">Oui</span><span class="sxs-lookup"><span data-stu-id="4fe5d-134">Yes</span></span> | [<span data-ttu-id="4fe5d-135">developer.chrome.com/extensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-135">developer.chrome.com/extensions</span></span>][ChromeDeveloperExtensions] |  
| <span data-ttu-id="4fe5d-136">Opera</span><span class="sxs-lookup"><span data-stu-id="4fe5d-136">Opera</span></span> | <span data-ttu-id="4fe5d-137">Oui</span><span class="sxs-lookup"><span data-stu-id="4fe5d-137">Yes</span></span> | [<span data-ttu-id="4fe5d-138">dev.opera.com/extensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-138">dev.opera.com/extensions</span></span>][OperaDevExtensions] |  
| <span data-ttu-id="4fe5d-139">Vér.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-139">Brave</span></span> | <span data-ttu-id="4fe5d-140">Oui</span><span class="sxs-lookup"><span data-stu-id="4fe5d-140">Yes</span></span> | <span data-ttu-id="4fe5d-141">Utilise [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span><span class="sxs-lookup"><span data-stu-id="4fe5d-141">Uses [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span></span> |  
| <span data-ttu-id="4fe5d-142">nouvelle Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4fe5d-142">new Microsoft Edge</span></span> | <span data-ttu-id="4fe5d-143">Oui</span><span class="sxs-lookup"><span data-stu-id="4fe5d-143">Yes</span></span> | [<span data-ttu-id="4fe5d-144">developer.microsoft.com/microsoft-edge/extensions</span><span class="sxs-lookup"><span data-stu-id="4fe5d-144">developer.microsoft.com/microsoft-edge/extensions</span></span>][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> <span data-ttu-id="4fe5d-145">La plupart des didacticiels des sites utilisent des API spécifiques au navigateur qui peuvent ne pas correspondre au navigateur pour lequel vous développez.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-145">Many of the tutorials of the sites use browser-specific APIs that may not match the browser for which you develop.</span></span>  <span data-ttu-id="4fe5d-146">Dans la plupart des cas, une extension Chromium fonctionne tel quel dans différents navigateurs Chromium et les API fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-146">In most cases, a Chromium extension works as-is in different Chromium browsers and the APIs work as expected.</span></span>  <span data-ttu-id="4fe5d-147">Seules certaines API moins courantes peuvent être strictement spécifiques au navigateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-147">Only some less common APIs may be strictly browser-specific.</span></span>  <span data-ttu-id="4fe5d-148">Pour obtenir des liens vers les didacticiels, [accédez à Voir aussi](#see-also).</span><span class="sxs-lookup"><span data-stu-id="4fe5d-148">For links to the tutorials, navigate to [See also](#see-also).</span></span>  

## <span data-ttu-id="4fe5d-149">Pourquoi Chromium ?</span><span class="sxs-lookup"><span data-stu-id="4fe5d-149">Why Chromium?</span></span>  

<span data-ttu-id="4fe5d-150">Si votre objectif est de publier votre extension dans le magasin d’extensions pour chaque navigateur, elle doit être modifiée pour que chaque version cible et s’exécute dans chaque environnement de navigateur distinct.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-150">If your goal is to publish your extension in the extensions store for each browser, it must be modified for each version to target and run in each distinct browser environment.</span></span>  <span data-ttu-id="4fe5d-151">Par exemple, les [extensions Safari peuvent][AppleDeveloperSafariservicesAppExtensions] utiliser du code web et natif pour communiquer avec des applications natives homologues.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-151">For example, [Safari extensions][AppleDeveloperSafariservicesAppExtensions] may use both web and native code to communicate with counterpart native applications.</span></span>  <span data-ttu-id="4fe5d-152">Les quatre derniers navigateurs du tableau précédent utilisent le même package de code et réduisent la nécessité de conserver des versions parallèles.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-152">The last four browsers in the previous table use the same code package, and minimizes the requirement to maintain parallel versions.</span></span>  <span data-ttu-id="4fe5d-153">Ces navigateurs sont basés sur le [Chromium open source.][|::ref1::|Home]</span><span class="sxs-lookup"><span data-stu-id="4fe5d-153">These browsers are based on the [Chromium open-source project][|::ref1::|Home].</span></span>  

<span data-ttu-id="4fe5d-154">Créez une extension Chromium pour écrire le moins de code.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-154">Create a Chromium extension to write the least amount of code.</span></span>  <span data-ttu-id="4fe5d-155">Il cible également le nombre maximal de magasins d’extensions et, en fin de compte, le nombre maximal d’utilisateurs qui trouvent et achètent votre extension.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-155">It also targets the maximum number of extension stores and ultimately the maximum number of users who find and acquire your extension.</span></span>  

<span data-ttu-id="4fe5d-156">Le contenu suivant se concentre principalement sur Chromium extensions.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-156">The following content focuses mostly on Chromium extensions.</span></span>  

## <span data-ttu-id="4fe5d-157">Test de compatibilité et d’extension du navigateur</span><span class="sxs-lookup"><span data-stu-id="4fe5d-157">Browser compatibility and extension testing</span></span>  

<span data-ttu-id="4fe5d-158">Parfois, la parité d’API n’existe pas entre Chromium navigateurs.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-158">Occasionally, API parity doesn't exist between Chromium browsers.</span></span>  <span data-ttu-id="4fe5d-159">Par exemple, il existe des différences dans les API d’identité et de paiement.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-159">For example, there are differences in the identity and payment APIs.</span></span>  <span data-ttu-id="4fe5d-160">Pour vous assurer que votre extension répond aux attentes des clients, examinez l’état de l’API via les documents officiels suivants du navigateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-160">To ensure your extension meets customer expectations, review API status through the following official browser docs.</span></span>  

*   [<span data-ttu-id="4fe5d-161">API Chrome</span><span class="sxs-lookup"><span data-stu-id="4fe5d-161">Chrome APIs</span></span>][ChromeDeveloperExtensionsApiIndex]  
*   [<span data-ttu-id="4fe5d-162">API d’extension prise en charge dans Opera</span><span class="sxs-lookup"><span data-stu-id="4fe5d-162">Extension APIs supported in Opera</span></span>][OperaDevExtensionsApis]  
*   [<span data-ttu-id="4fe5d-163">Portage de l’extension Chrome Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-163">Port Chrome extension to Microsoft Edge (Chromium)</span></span>][ExtensionsChromiumDeveloperGuidePortChrome]  
    
<span data-ttu-id="4fe5d-164">Les API dont vous avez besoin définissent les modifications que vous devez apporter pour résoudre les différences entre chaque navigateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-164">The APIs you require define the changes you must make to address the differences between each browser.</span></span>  <span data-ttu-id="4fe5d-165">Cela peut signifier que vous devez créer des packages de code légèrement différents avec de petites différences pour chaque magasin.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-165">It may mean that you must create slightly different code packages with small differences for each store.</span></span>  

<span data-ttu-id="4fe5d-166">Pour tester votre extension dans différents environnements avant de l’envoyer à un magasin de navigateurs, chargez-la dans votre navigateur pendant que vous la développez.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-166">To test your extension in different environments before you submit it to a browser store, sideload it into your browser while you develop it.</span></span>  

## <span data-ttu-id="4fe5d-167">Publier votre extension dans les magasins de navigateurs</span><span class="sxs-lookup"><span data-stu-id="4fe5d-167">Publish your extension to browser stores</span></span>  

<span data-ttu-id="4fe5d-168">Vous pouvez soumettre et rechercher des extensions de navigateur dans les magasins de navigateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-168">You may submit and seek browser extensions in the following browser stores.</span></span>  

*   [<span data-ttu-id="4fe5d-169">Modules de modules de navigateur Firefox</span><span class="sxs-lookup"><span data-stu-id="4fe5d-169">Firefox Browser Add-ons</span></span>][MozillaAddonsFirefoxExtensions]  
*   [<span data-ttu-id="4fe5d-170">Chrome Web Store</span><span class="sxs-lookup"><span data-stu-id="4fe5d-170">Chrome Web Store</span></span>][GoogleChromeWebstoreCategoryExtensions]  
*   [<span data-ttu-id="4fe5d-171">Addons d’opéra</span><span class="sxs-lookup"><span data-stu-id="4fe5d-171">Opera addons</span></span>][OperaAddonsExtensions]  
*   [<span data-ttu-id="4fe5d-172">Microsoft Edge Modules de modules</span><span class="sxs-lookup"><span data-stu-id="4fe5d-172">Microsoft Edge Add-ons</span></span>][MicrosoftEdgeAddonsCategoryExtensions]  

<span data-ttu-id="4fe5d-173">Certaines magasins vous permettent de télécharger des extensions répertoriées à partir d’autres navigateurs.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-173">Some stores allow you to download listed extensions from other browsers.</span></span>  <span data-ttu-id="4fe5d-174">Toutefois, l’accès entre navigateurs n’est pas garanti par les magasins de navigateurs.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-174">However, cross-browser access is not guaranteed by browser stores.</span></span>  <span data-ttu-id="4fe5d-175">Pour vous assurer que vos utilisateurs trouvent votre extension dans différents navigateurs, vous devez conserver une liste sur chaque magasin d’extensions de navigateur.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-175">To ensure your users find your extension in different browsers, you should maintain a listing on each browser extension store.</span></span>  

<span data-ttu-id="4fe5d-176">Les utilisateurs devront peut-être installer votre extension dans différents navigateurs.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-176">Users may need to install your extension in different browsers.</span></span> <span data-ttu-id="4fe5d-177">Dans ce scénario, vous pouvez migrer des extensions Chromium existantes d’un navigateur à un autre.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-177">In this scenario, you may migrate existing Chromium extensions from one browser to another.</span></span>  

### <span data-ttu-id="4fe5d-178">Migrer une extension existante vers Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4fe5d-178">Migrate an existing extension to Microsoft Edge</span></span>  

<span data-ttu-id="4fe5d-179">Si vous avez déjà développé une extension pour un autre navigateur Chromium, vous pouvez la soumettre au magasin Microsoft Edge de modules.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-179">If you've already developed an extension for another Chromium browser, you may submit it to the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="4fe5d-180">Vous n’avez pas besoin de réécrire votre extension et devez vérifier qu’elle fonctionne dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-180">You don't need to rewrite your extension, and must verify it works in Microsoft Edge.</span></span>  <span data-ttu-id="4fe5d-181">Lorsque vous migrez une extension Chromium existante vers d’autres navigateurs Chromium, assurez-vous que les mêmes API ou alternatives sont disponibles pour votre navigateur cible.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-181">When you migrate an existing Chromium extension to other Chromium browsers, ensure the same APIs or alternatives are available for your target browser.</span></span>  

<span data-ttu-id="4fe5d-182">Pour plus d’informations sur le portage de votre extension Chrome vers Microsoft Edge, accédez aux [extensions Port Chrome vers Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome]</span><span class="sxs-lookup"><span data-stu-id="4fe5d-182">For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span></span> <span data-ttu-id="4fe5d-183">Une fois que vous avez porté votre extension vers le navigateur cible, l’étape suivante consiste à la publier.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-183">After you port your extension to the target browser, the next step is to publish it.</span></span>  

### <span data-ttu-id="4fe5d-184">Publier sur le site modules complémentaires Microsoft Edge web</span><span class="sxs-lookup"><span data-stu-id="4fe5d-184">Publish to the Microsoft Edge add-ons website</span></span>  

<span data-ttu-id="4fe5d-185">Pour commencer à publier votre extension sur [][MicrosoftDeveloperRegistration] Microsoft Edge, vous devez vous inscrire à un compte de développeur auprès d’un compte de messagerie MSA pour soumettre votre liste d’extensions au Store.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-185">To start publishing your extension to Microsoft Edge, you must [register for a developer account][MicrosoftDeveloperRegistration] with an MSA email account to submit your extension listing to the store.</span></span>  <span data-ttu-id="4fe5d-186">Un compte de messagerie MSA `@outlook.com` `@live.com` inclut, etc.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-186">An MSA email account includes `@outlook.com`, `@live.com`, and so on.</span></span>  <span data-ttu-id="4fe5d-187">Lorsque vous choisissez une adresse de messagerie à inscrire, pensez à transférer ou partager la propriété de l’extension avec d’autres personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-187">When you choose an email address to register, consider if you must transfer or share ownership of the extension with others in your organization.</span></span>  <span data-ttu-id="4fe5d-188">Une fois l’inscription terminée, vous pouvez créer une soumission d’extension au Store.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-188">After registration is complete, you may create a new extension submission to the store.</span></span>  

<span data-ttu-id="4fe5d-189">Pour envoyer votre extension au Store, veillez à fournir les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-189">To submit your extension to the store, ensure you provide the following items.</span></span>  

*   <span data-ttu-id="4fe5d-190">Fichier d’archivage `.zip` \( \) qui contient vos fichiers de code.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-190">An archive \(`.zip`\) file that contains your code files.</span></span>  
*   <span data-ttu-id="4fe5d-191">Toutes les ressources visuelles requises, qui incluent un logo et une petite vignette promotionnelle.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-191">All required visual assets, which include a logo and small promotional tile.</span></span>  
*   <span data-ttu-id="4fe5d-192">Médias promotionnels facultatifs, tels que des captures d’écran, des vignettes promotionnelles et une URL vidéo.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-192">Optional promotional media, such as screenshots, promotional tiles, and a video URL.</span></span>  
*   <span data-ttu-id="4fe5d-193">Informations qui décrivent votre extension, telles que le nom, la description courte et un lien de stratégie de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-193">Information that describes your extension such as the name, short description, and a privacy policy link.</span></span>  

> [!NOTE]
> <span data-ttu-id="4fe5d-194">Différents magasins peuvent avoir des exigences d’envoi différentes.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-194">Different stores may have different submission requirements.</span></span>  <span data-ttu-id="4fe5d-195">La liste ci-dessus récapitule les [conditions requises][ExtensionsChromiumPublish] pour publier une extension pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-195">The above list summarizes the [requirements][ExtensionsChromiumPublish] to publish an extension for Microsoft Edge.</span></span>  

<span data-ttu-id="4fe5d-196">Une fois que vous avez envoyé votre extension, elle est soumise à un processus de révision et réussit ou échoue au processus de certification.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-196">After you've successfully submitted your extension, your extension undergoes a review process and either passes or fails the certification process.</span></span>  <span data-ttu-id="4fe5d-197">Les propriétaires sont avertis du résultat et doivent suivre les étapes suivantes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-197">Owners are notified of the outcome and given next steps as required.</span></span>  <span data-ttu-id="4fe5d-198">Si vous soumettez une mise à jour d’extension au Store, un nouveau processus de révision est démarré.</span><span class="sxs-lookup"><span data-stu-id="4fe5d-198">If you submit an extension update to the store, a new review process is started.</span></span>  

## <span data-ttu-id="4fe5d-199">Articles associés</span><span class="sxs-lookup"><span data-stu-id="4fe5d-199">See also</span></span>  

*   [<span data-ttu-id="4fe5d-200">Portage d’une extension Google Chrome</span><span class="sxs-lookup"><span data-stu-id="4fe5d-200">Port a Google Chrome extension</span></span>][ExtensionworkshopPorting]  
*   [<span data-ttu-id="4fe5d-201">Créer une extension d’application Safari</span><span class="sxs-lookup"><span data-stu-id="4fe5d-201">Build a Safari App extension</span></span>][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [<span data-ttu-id="4fe5d-202">Votre première extension (Firefox)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-202">Your first extension (Firefox)</span></span>][MDNWebextensionsYourFirst]  
*   [<span data-ttu-id="4fe5d-203">Didacticiel de mise en place (Chrome)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-203">Get started tutorial (Chrome)</span></span>][ChromeDeveloperExtensionsGetstarted]  
*   [<span data-ttu-id="4fe5d-204">Get started (Opera)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-204">Get started (Opera)</span></span>][OperaDevExtensionsGettingStarted]  
*   [<span data-ttu-id="4fe5d-205">Commencer avec les extensions Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="4fe5d-205">Get started with Microsoft Edge (Chromium) extensions</span></span>][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Portage de l’extension Chrome Microsoft Edge (Chromium) | Documents Microsoft"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Getting Started With Microsoft Edge (Chromium) Extensions | Documents Microsoft"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publier une extension | Documents Microsoft"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Développer des extensions pour Microsoft Edge | Développeur Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Développeur Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensions pour Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensions d’application Safari | Développeur Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Création d’une extension d’application Safari | Développeur Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Que sont les extensions ? | Développeur Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Api Chrome | Développeur Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Didacticiel de mise en | Développeur Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portage d’une extension Google Chrome | Atelier d’extension"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensions | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensions de navigateur | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Votre première extension | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensions | Modules de modules pour Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensions | Opéra Addons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentation sur les extensions | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API d’extension prise en charge dans Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Mise en | Dev. Opera"  
