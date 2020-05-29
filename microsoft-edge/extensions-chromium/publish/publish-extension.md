---
description: Processus étape par étape de la publication d’extensions de périphérique (chrome) sur le Microsoft Store.
title: Publier une extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607377"
---
# <span data-ttu-id="9a0ff-104">Publier une extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-104">Publish An Extension</span></span>  

<span data-ttu-id="9a0ff-105">Publiez votre extension sur le catalogue Microsoft Edge addons \ (Microsoft Edge addons \).</span><span class="sxs-lookup"><span data-stu-id="9a0ff-105">Publish your Extension on Microsoft Edge Addons catalog \(Microsoft Edge Addons\).</span></span>  <span data-ttu-id="9a0ff-106">Vous devez commencer par créer une soumission dans le [Centre de partenariat][MicrosoftPartnerCenter] et la soumettre.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-106">You must first create a submission on [Partner Center][MicrosoftPartnerCenter] and submit it.</span></span>  <span data-ttu-id="9a0ff-107">Ce document recense tous les détails que vous devez fournir pour créer une soumission d’extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-107">This document lists all the details that you must provide to create an Extension submission.</span></span>  

## <span data-ttu-id="9a0ff-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9a0ff-108">Before You Begin</span></span>  

*   <span data-ttu-id="9a0ff-109">Vous devez disposer d’un compte de développeur actif dans le [Centre des partenaires][MicrosoftPartnerCenter] pour pouvoir faire votre extension dans Microsoft Edge addons.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-109">You must have an active developer account on [Partner Center][MicrosoftPartnerCenter] to submit your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="9a0ff-110">Si vous n’en avez pas, [créez un compte de développeur][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="9a0ff-110">If you do not have one, [create a new developer account][MicrosoftPartnerCenter].</span></span>  
*   <span data-ttu-id="9a0ff-111">Créez un fichier zip de votre package d’extension et assurez-vous qu’il contient les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-111">Create a zip file of your Extension package and ensure that it contains these files:</span></span>  
    *   <span data-ttu-id="9a0ff-112">Le fichier manifeste et il doit définir le nom et la version de votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-112">The manifest file and it must define the name and version of your Extension.</span></span>  
    *   <span data-ttu-id="9a0ff-113">Les images et autres fichiers requis pour votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-113">The images and other files that are required for your Extension.</span></span>  


<span data-ttu-id="9a0ff-114">Si vous n’avez pas encore créé de poste, vous pouvez consulter le didacticiel de [mise en route][ExtensionsGettingStarted] pour la création d’une extension de chrome Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-114">If you have not started building an Extension, you may refer to the [Getting Started][ExtensionsGettingStarted] tutorial for building a Microsoft Edge Chromium extension.</span></span>  

<span data-ttu-id="9a0ff-115">Pour créer une soumission d’extension dans le [Centre de partenariat][MicrosoftPartnerCenter], procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-115">To create an Extension submission on [Partner Center][MicrosoftPartnerCenter], follow these steps.</span></span>  

## <span data-ttu-id="9a0ff-116">Étape 1: commencer une nouvelle soumission</span><span class="sxs-lookup"><span data-stu-id="9a0ff-116">Step 1: Start a New Submission</span></span>  

<span data-ttu-id="9a0ff-117">Accédez au [tableau de bord][MicrosoftPartnerCenter]de votre développeur.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-117">Go to your [developer dashboard][MicrosoftPartnerCenter].</span></span>  <span data-ttu-id="9a0ff-118">Sur la page vue d’ensemble, cliquez sur **créer une nouvelle extension**.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-118">From the Overview page, click **Create new extension**.</span></span>  

## <span data-ttu-id="9a0ff-119">Étape 2: Télécharger le fichier zip de votre extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-119">Step 2: Upload Your Extension Zip File</span></span>  

<span data-ttu-id="9a0ff-120">La page **package** est l’endroit où vous chargez le fichier zip de votre soumission d’extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-120">The **Package** page is where you upload the zip file for your Extension submission.</span></span>  <span data-ttu-id="9a0ff-121">Il est possible que vous ne puissiez télécharger qu’un seul package à la fois, et si votre extension n’est pas terminée, il est possible que vous receviez un package en cours de travail et une mise à jour à tout moment avant de le publier.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-121">You may only upload one package at a time, so if your Extension is not complete you may upload a work-in-progress package and update at any time before you publish it.</span></span>  <span data-ttu-id="9a0ff-122">Assurez-vous que votre package contient le `manifest.json` fichier et qu’il fonctionne correctement sur Microsoft Edge avant de le télécharger.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-122">Be sure that your package contains the `manifest.json` file and is working fine on Microsoft Edge prior to uploading.</span></span>  
<span data-ttu-id="9a0ff-123">Téléchargez le package en le faisant glisser dans le champ de chargement ou en sélectionnant **parcourir vos fichiers**.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-123">Upload the package by dragging it into the upload field or by selecting **Browse your files**.</span></span>  <span data-ttu-id="9a0ff-124">La page package valide le fichier zip extensions et affiche l' **État de réussite ou d’échec de votre chargement**.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-124">The Package page validates the Extensions zip file and displays that **success or failure status of your upload**.</span></span>  <span data-ttu-id="9a0ff-125">Si le package est validé; Il est chargé avec succès et un message de réussite s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-125">If the package passes validation; it is uploaded successfully and you see a success message.</span></span>  <span data-ttu-id="9a0ff-126">Si la validation du package échoue; le package n’est pas accepté et un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-126">If the package fails validation; the package is not accepted and you see an error message.</span></span>  <span data-ttu-id="9a0ff-127">Si le package contient des erreurs, résolvez les problèmes et essayez de le télécharger à nouveau.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-127">If there are errors in the package, resolve the issues and try uploading it again.</span></span>  

<span data-ttu-id="9a0ff-128">Une fois le téléchargement terminé, passez en revue les détails de votre poste, puis cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-128">After successful upload, review your Extension details and click **Next** to proceed.</span></span>  

## <span data-ttu-id="9a0ff-129">Étape 3: fournir des informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="9a0ff-129">Step 3: Provide Availability details</span></span>  

### <span data-ttu-id="9a0ff-130">Définir la visibilité</span><span class="sxs-lookup"><span data-stu-id="9a0ff-130">Define Visibility</span></span>  

<span data-ttu-id="9a0ff-131">Sélectionnez une option de **visibilité** pour définir le public qui est susceptible de détecter et d’acquérir votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-131">Select a **Visibility** option to define the audience who may discover and acquire your Extension.</span></span>  <span data-ttu-id="9a0ff-132">Cela vous permet de spécifier si les utilisateurs doivent trouver votre extension dans les compléments Microsoft Edge ou consulter le contenu de la liste.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-132">This gives you the option to specify whether users should find your Extension in Microsoft Edge Addons or see the listing at all.</span></span>  <span data-ttu-id="9a0ff-133">Pour l’instant, vous avez le choix entre deux options sous Visibility:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-133">Currently, you have two options under visibility:</span></span>  

*   `Public`  
    <span data-ttu-id="9a0ff-134">Il s’agit de l’option par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-134">This is the default option.</span></span>  
    <span data-ttu-id="9a0ff-135">Si vous sélectionnez `Public` , votre extension est disponible et détectable par tout le monde dans les modules complémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-135">If you select `Public`, your Extension is available and discoverable to everyone in Microsoft Edge Addons.</span></span>  <span data-ttu-id="9a0ff-136">Laissez cette option sélectionnée si vous voulez que votre extension soit répertoriée dans les modules complémentaires Microsoft Edge pour les utilisateurs à rechercher via la recherche, la navigation et le lien direct de votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-136">Leave this option selected if you want your Extension to be listed in Microsoft Edge Addons for users to find via searching, browsing, and the direct link of your Extension.</span></span>  

*   `Hidden`  
    <span data-ttu-id="9a0ff-137">Si vous sélectionnez cette option `Hidden` , votre extension est masquée dans les modules complémentaires Microsoft Edge lors de la recherche ou de la navigation des utilisateurs; vous devez partager votre URL d’entrée pour distribuer votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-137">If you select `Hidden`, your Extension is hidden in Microsoft Edge Addons from users searching or browsing; you must share your listing URL to distribute your Extension.</span></span>  <span data-ttu-id="9a0ff-138">Les utilisateurs disposant d’un lien direct vers l’entrée peuvent télécharger l’application sur Microsoft Edge \ (il est possible que vous trouviez votre URL de référencement dans la page de **Présentation** de l’extension \).</span><span class="sxs-lookup"><span data-stu-id="9a0ff-138">Users who have the direct link to the listing may download it on Microsoft Edge \(you may find your listing URL under **Extension Overview** page of Extension submission\).</span></span>  

> [!NOTE]
> <span data-ttu-id="9a0ff-139">Si vous envoyez une extension **publique** et que vous la définissez ultérieurement sur **privée**, les utilisateurs qui ont installé l’extension quand elle était publique continuent d’avoir accès et de recevoir des mises à jour ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-139">If you submit an Extension as **Public** and later change it to **Private**, Users who installed the Extension when it was public continue to have access and receive future updates.</span></span>  

### <span data-ttu-id="9a0ff-140">Définir des marchés</span><span class="sxs-lookup"><span data-stu-id="9a0ff-140">Define markets</span></span>  

<span data-ttu-id="9a0ff-141">Vous devez définir les marchés spécifiques dans lesquels vous proposez votre extension, puis sélectionnez **afficher les options** dans la section **marchés** de la page **disponibilité** .</span><span class="sxs-lookup"><span data-stu-id="9a0ff-141">You must define the specific markets in which you are offering your Extension, select **Show options** in the **Markets** section on the **Availability** page.</span></span>  <span data-ttu-id="9a0ff-142">La fenêtre contextuelle de sélection du marché s’affiche, qui vous permet de choisir les marchés.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-142">The Market selection pop-up window is displayed, where you should choose the markets.</span></span>  <span data-ttu-id="9a0ff-143">Par défaut, tous les marchés sont sélectionnés, y compris tous les **marchés futurs** qui pourront être ajoutés plus tard.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-143">By default, all markets are selected, including any **future markets** that may be added later.</span></span>  <span data-ttu-id="9a0ff-144">Vous pouvez désélectionner des marchés spécifiques pour les exclure, ou cliquer sur **Désélectionner tout** , puis ajouter les marchés de votre choix.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-144">You may deselect individual markets to exclude them, or you may click **Unselect all** and then add individual markets of your choice.</span></span>  

> [!NOTE]
> <span data-ttu-id="9a0ff-145">Si les utilisateurs ont déjà votre extension dans un certain marché et que vous supprimez ensuite ce marché, les utilisateurs disposant déjà de l’extension sur ce marché peuvent continuer à l’utiliser, mais ils ne reçoivent pas les mises à jour que vous avez apportées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-145">If users already have your Extension in a certain market, and you later remove that market, users who already has the Extension in that market may continue to use it, but they do not get the later updates you submit.</span></span>  

<span data-ttu-id="9a0ff-146">Cliquez sur **Enregistrer** pour accéder à la section **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="9a0ff-146">Click **Save** to proceed to **Properties** section.</span></span>  

## <span data-ttu-id="9a0ff-147">Étape 4: sélectionner les propriétés pour votre extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-147">Step 4: Select Properties for Your Extension</span></span>  

### <span data-ttu-id="9a0ff-148">Propriétés d’extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-148">Extension properties</span></span>  

*   [<span data-ttu-id="9a0ff-149">Catégorie</span><span class="sxs-lookup"><span data-stu-id="9a0ff-149">Category</span></span>](#category)  
*   [<span data-ttu-id="9a0ff-150">Politique de confidentialité</span><span class="sxs-lookup"><span data-stu-id="9a0ff-150">Privacy policy requirements</span></span>](#privacy-policy-requirements)  
*   [<span data-ttu-id="9a0ff-151">URL de la politique de confidentialité</span><span class="sxs-lookup"><span data-stu-id="9a0ff-151">Privacy policy URL</span></span>](#privacy-policy-url)  
*   [<span data-ttu-id="9a0ff-152">URL du site Web</span><span class="sxs-lookup"><span data-stu-id="9a0ff-152">Website URL</span></span>](#website-url)  
*   [<span data-ttu-id="9a0ff-153">URL/adresse e-mail du support technique</span><span class="sxs-lookup"><span data-stu-id="9a0ff-153">Support URL/email address</span></span>](#support-urlemail-address)  
*   [<span data-ttu-id="9a0ff-154">Niveau d’extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-154">Extension Rating</span></span>](#extension-rating)  

#### <span data-ttu-id="9a0ff-155">Catégorie</span><span class="sxs-lookup"><span data-stu-id="9a0ff-155">Category</span></span>  

<span data-ttu-id="9a0ff-156">La liste de vos extensions dans la catégorie appropriée permet aux utilisateurs de trouver facilement votre extension et d’en savoir plus à son sujet.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-156">Listing your Extension in the right category helps users find your Extension easily and understand more about it.</span></span>  <span data-ttu-id="9a0ff-157">Sélectionnez une catégorie qui décrit le mieux votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-157">Select a Category that best describes your Extension.</span></span>  

<span data-ttu-id="9a0ff-158">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-158">**Possible Values**:</span></span>  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### <span data-ttu-id="9a0ff-159">Politique de confidentialité</span><span class="sxs-lookup"><span data-stu-id="9a0ff-159">Privacy policy requirements</span></span>  

<span data-ttu-id="9a0ff-160">Indiquez si votre extension accède à une extension, collecte ou transmet des informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-160">Indicate whether your Extension accesses, collects, or transmits any personal information.</span></span>  

> [!NOTE]
> <span data-ttu-id="9a0ff-161">Si votre extension nécessite une politique de confidentialité et que vous ne l’avez pas fournie, votre soumission risque de ne pas obtenir de certification.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-161">If your Extension requires a privacy policy and you have not provided one, your submission may fail certification.</span></span>  

<span data-ttu-id="9a0ff-162">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-162">**Possible Values**:</span></span>  

*   `No`<span data-ttu-id="9a0ff-163">: Une URL de politique de confidentialité est facultative.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-163">:  A privacy policy URL is optional.</span></span>  
*   `Yes`<span data-ttu-id="9a0ff-164">: Une URL de politique de confidentialité est requise.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-164">:  A privacy policy URL is required.</span></span>  

#### <span data-ttu-id="9a0ff-165">URL de la politique de confidentialité</span><span class="sxs-lookup"><span data-stu-id="9a0ff-165">Privacy policy URL</span></span>  

<span data-ttu-id="9a0ff-166">Le cas échéant, vous êtes responsable de la conformité de votre extension aux lois et réglementations en matière de vie privée.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-166">You are responsible for ensuring your Extension complies with privacy laws and regulations, and for providing a valid privacy policy URL, if required.</span></span>  <span data-ttu-id="9a0ff-167">Vous devez fournir une URL de politique de confidentialité si des informations personnelles sont consultées, transmises ou collectées par votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-167">You must provide a privacy policy URL if any personal information is being accessed, transmitted, or collected by your Extension.</span></span>  
<span data-ttu-id="9a0ff-168">Pour savoir si votre extension nécessite une politique de confidentialité, consultez le [contrat du développeur Microsoft Edge][MicrosoftAppDeveloperAgreement] et le document des stratégies pour les [développeurs du catalogue Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="9a0ff-168">To determine if your Extension requires a privacy policy, review the [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] and the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="9a0ff-169">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-169">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="9a0ff-170">URL du site Web</span><span class="sxs-lookup"><span data-stu-id="9a0ff-170">Website URL</span></span>  

<span data-ttu-id="9a0ff-171">Propriété facultative.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-171">This property is Optional.</span></span>  
<span data-ttu-id="9a0ff-172">URL de la page Web de votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-172">The URL of the web page for your Extension.</span></span>  <span data-ttu-id="9a0ff-173">Cette URL doit pointer vers une page de votre propre site Web, et non vers la liste des sites Web de votre extension dans les modules complémentaires Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-173">This URL must point to a page on your own website, not the web listing for your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="9a0ff-174">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-174">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="9a0ff-175">URL/adresse e-mail du support technique</span><span class="sxs-lookup"><span data-stu-id="9a0ff-175">Support URL/email address</span></span>  

<span data-ttu-id="9a0ff-176">Propriété facultative.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-176">This property is Optional.</span></span>  
<span data-ttu-id="9a0ff-177">URL de la page Web dans laquelle les utilisateurs accèdent à la prise en charge de votre extension ou une adresse de messagerie pour vous contacter.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-177">The URL of the web page where users go for support with your Extension, or an email address to contact you for support.</span></span>  <span data-ttu-id="9a0ff-178">Vous incluez des informations de support pour toutes les soumissions, de sorte que vos utilisateurs sachent comment obtenir une assistance technique.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-178">You include support information for all submissions, so that your users know how to get support from you.</span></span>  

<span data-ttu-id="9a0ff-179">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-179">**Possible Values**:</span></span>  

*   `{email_address}`  
*   `{url}`  

#### <span data-ttu-id="9a0ff-180">Niveau d’extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-180">Extension Rating</span></span>  

<span data-ttu-id="9a0ff-181">Le taux d’extension nous permet de déterminer l’âge du public cible de votre poste.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-181">Extension rating helps us determine the age of the target audience of your Extension.</span></span>  
<span data-ttu-id="9a0ff-182">Pour vous aider à déterminer si le contenu de vos extensions est mature, consultez le [document stratégies pour les développeurs du catalogue Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="9a0ff-182">To help you determine if your Extensions has a mature content, review the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="9a0ff-183">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-183">**Possible Values**:</span></span>  

*   <span data-ttu-id="9a0ff-184">Mature \ (case à cocher \): activez cette case à cocher si votre extension contient du contenu mûr.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-184">Mature \(checkbox\): Check this box if your Extension contains any mature content.</span></span>  <span data-ttu-id="9a0ff-185">Si vous avez sélectionné l’option mature pour votre extension, votre entrée est disponible avec une balise séparée pour indiquer que l’extension contient du contenu mûr.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-185">If you select mature for your Extension, your listing is available with a separate tag to indicate that the Extension contains mature content.</span></span>  

<span data-ttu-id="9a0ff-186">Cliquez sur **Enregistrer** pour accéder à la section liste.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-186">Click **Save** to proceed to listing section.</span></span>  

## <span data-ttu-id="9a0ff-187">Étape 5: ajouter des informations de référencement pour votre extension</span><span class="sxs-lookup"><span data-stu-id="9a0ff-187">Step 5: Add Listings Information for Your Extension</span></span>  

<span data-ttu-id="9a0ff-188">Voici les informations que voient les utilisateurs lors de l’affichage de votre entrée dans les compléments Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-188">This is the information that users see when viewing your listing in Microsoft Edge Addons.</span></span>  <span data-ttu-id="9a0ff-189">La plupart des champs d’une liste sont facultatifs, mais nous vous suggérons de fournir autant d’informations que possible pour faire ressortir votre annonce.  Le minimum requis pour que votre liste des modules complémentaires Microsoft Edge soit considéré comme complet est la [Description du texte](#description), le logo de l' [extension](#store-logo)et la [vignette promotionnelle de petite taille](#small-promotional-tile) dans chaque langage mentionné dans votre package d’extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-189">Many of the fields in a listing are optional, but we suggest providing as much information as possible to make your listing stand out.  The minimum required for your listing in Microsoft Edge Addons to be considered complete is the [text description](#description), [Extension logo](#store-logo), and [small promotional tile](#small-promotional-tile) in each language mentioned in your Extension package.</span></span>  

### <span data-ttu-id="9a0ff-190">Champs d’annonce dans le Windows Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-190">Store Listing fields</span></span>  

*   [<span data-ttu-id="9a0ff-191">Langues des descriptions dans le Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-191">Store listing languages</span></span>](#store-listing-languages)  
*   [<span data-ttu-id="9a0ff-192">Nom complet du Windows Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-192">Store display name</span></span>](#store-display-name)  
*   [<span data-ttu-id="9a0ff-193">Description</span><span class="sxs-lookup"><span data-stu-id="9a0ff-193">Description</span></span>](#description)  
*   [<span data-ttu-id="9a0ff-194">Logo du Windows Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-194">Store logo</span></span>](#store-logo)  
*   [<span data-ttu-id="9a0ff-195">Petite vignette promotionnelle</span><span class="sxs-lookup"><span data-stu-id="9a0ff-195">Small promotional tile</span></span>](#small-promotional-tile)  
*   [<span data-ttu-id="9a0ff-196">Support</span><span class="sxs-lookup"><span data-stu-id="9a0ff-196">Media</span></span>](#media)  
*   [<span data-ttu-id="9a0ff-197">Description courte</span><span class="sxs-lookup"><span data-stu-id="9a0ff-197">Short description</span></span>](#short-description)  
*   [<span data-ttu-id="9a0ff-198">Termes de recherche</span><span class="sxs-lookup"><span data-stu-id="9a0ff-198">Search terms</span></span>](#search-terms)  

#### <span data-ttu-id="9a0ff-199">Langues des descriptions dans le Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-199">Store listing languages</span></span>  

<span data-ttu-id="9a0ff-200">Si votre package d’extension prend en charge plusieurs langues, votre extension doit être associée à une page de listing pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-200">If your Extension package supports multiple languages, your Extension must have a listing page for each one.</span></span>  
<span data-ttu-id="9a0ff-201">Vous devez compléter les détails de la liste \ (description du texte, images, etc.) pour chaque langue séparément, même si vous utilisez le même contenu pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-201">You must complete listing details \(text description, images, and so on\) for each language separately even if you are using the same content for each language.</span></span>  <span data-ttu-id="9a0ff-202">Si votre extension est localisée dans plusieurs langues, celles-ci s’affichent en haut de la page de description.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-202">If your Extension is localized in more than one language, those languages are displayed at the top of listing page.</span></span>  

1.  <span data-ttu-id="9a0ff-203">Sélectionnez un nom de langue dans la liste déroulante **langues** .</span><span class="sxs-lookup"><span data-stu-id="9a0ff-203">Select any one language name from **Languages** drop-down list.</span></span>  
1.  <span data-ttu-id="9a0ff-204">Remplissez les détails de la liste.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-204">Fill the listing details.</span></span>  
1.  <span data-ttu-id="9a0ff-205">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-205">Click **Save**.</span></span>  
1.  <span data-ttu-id="9a0ff-206">Répétez l’opération pour toutes les langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-206">Repeat for all of your supported languages.</span></span>  

> [!NOTE]
> <span data-ttu-id="9a0ff-207">Pour ajouter ou supprimer des langues pour votre liste dans les modules complémentaires Microsoft Edge, vous devez modifier la liste des langues prises en charge par votre package d’extension et le télécharger à nouveau.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-207">To add or remove languages for your listing in Microsoft Edge Addons, you must modify the list of languages supported by your Extension package and re-upload it.</span></span>  

<span data-ttu-id="9a0ff-208">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-208">**Possible Values**:</span></span>  

*   `English (United States)`<span data-ttu-id="9a0ff-209">: Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-209">:  This is the default value.</span></span>  <span data-ttu-id="9a0ff-210">Si vous n’indiquez aucune langue dans votre package, nous définissons votre langue par défaut sur français (France), et vous devez fournir une entrée en anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="9a0ff-210">If you do not mention any language in your package, we set your default language to English \(United States\) and you must provide a listing in English \(United States\).</span></span>  
*   `{language}` <span data-ttu-id="9a0ff-211">\(`{Country}`\)</span><span class="sxs-lookup"><span data-stu-id="9a0ff-211">\(`{Country}`\)</span></span>  

#### <span data-ttu-id="9a0ff-212">Nom complet du Windows Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-212">Store display name</span></span>  

<span data-ttu-id="9a0ff-213">Nom de l’extension, tel que mentionné dans le manifeste de votre package d’extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-213">The name of Extension as mentioned in your Extension package manifest.</span></span>  

> [!NOTE]
> <span data-ttu-id="9a0ff-214">Pour modifier le nom, vous devez mettre à jour le manifeste dans votre package d’extension et le télécharger à nouveau.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-214">To edit the name, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="9a0ff-215">Description</span><span class="sxs-lookup"><span data-stu-id="9a0ff-215">Description</span></span>  

<span data-ttu-id="9a0ff-216">Ce champ est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-216">This field is required.</span></span>  
<span data-ttu-id="9a0ff-217">Description de la fonction de votre extension par vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-217">The description for your users of what your Extension does.</span></span>  

<span data-ttu-id="9a0ff-218">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-218">**Possible Values**:</span></span>  

*   <span data-ttu-id="9a0ff-219">{plain_text}: moins de 10 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-219">{plain_text}: Less than 10,000 characters.</span></span>  

#### <span data-ttu-id="9a0ff-220">Logo du Windows Store</span><span class="sxs-lookup"><span data-stu-id="9a0ff-220">Store logo</span></span>  

<span data-ttu-id="9a0ff-221">Ce champ est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-221">This field is required.</span></span>  
<span data-ttu-id="9a0ff-222">Image 1:1 du logo de votre poste.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-222">A 1:1 image for your Extension logo.</span></span>  

<span data-ttu-id="9a0ff-223">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-223">**Possible Values**:</span></span>  

*   <span data-ttu-id="9a0ff-224">128px x 128px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="9a0ff-224">128px x 128px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="9a0ff-225">150px x 140px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="9a0ff-225">150px x 140px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="9a0ff-226">300px x 300px, PNG \ (. png \): taille recommandée.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-226">300px x 300px, PNG \(.png\):  The recommended size.</span></span>  

#### <span data-ttu-id="9a0ff-227">Petite vignette promotionnelle</span><span class="sxs-lookup"><span data-stu-id="9a0ff-227">Small promotional tile</span></span>  

<span data-ttu-id="9a0ff-228">Ce champ est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-228">This field is required.</span></span>  
<span data-ttu-id="9a0ff-229">Vignette promotionnelle de petite taille.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-229">A small size promotional tile.</span></span>  <span data-ttu-id="9a0ff-230">Votre entrée est affichée sur cette vignette.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-230">Your listing is displayed on this tile.</span></span>  

<span data-ttu-id="9a0ff-231">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-231">**Possible Values**:</span></span>  

*   <span data-ttu-id="9a0ff-232">440px x 280x, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="9a0ff-232">440px x 280x, PNG \(.png\)</span></span>  

#### <span data-ttu-id="9a0ff-233">Support</span><span class="sxs-lookup"><span data-stu-id="9a0ff-233">Media</span></span>  

<span data-ttu-id="9a0ff-234">Il est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-234">This field is optional.</span></span>  
<span data-ttu-id="9a0ff-235">Nous vous conseillons de fournir ces ressources pour vous aider à optimiser l’affichage de votre produit.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-235">You should provide these assets to help display your product more effectively.</span></span>  

*   <span data-ttu-id="9a0ff-236">Captures d’écran</span><span class="sxs-lookup"><span data-stu-id="9a0ff-236">Screenshots</span></span>  
    <span data-ttu-id="9a0ff-237">Les images de votre extension qui décrivent ce que fait votre extension.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-237">The images of your Extension that describe what your Extension does.</span></span>  
    
*   <span data-ttu-id="9a0ff-238">Tuiles de grande promotion</span><span class="sxs-lookup"><span data-stu-id="9a0ff-238">Large promotion tiles</span></span>  
    <span data-ttu-id="9a0ff-239">Une vignette promotionnelle de grande taille pour pouvoir présenter plus clairement votre extension dans les compléments Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-239">A large promotional tile to be feature your Extension more prominently in Microsoft Edge Addons.</span></span>  
    
*   <span data-ttu-id="9a0ff-240">URL de la vidéo YouTube</span><span class="sxs-lookup"><span data-stu-id="9a0ff-240">YouTube video URL</span></span>  
    <span data-ttu-id="9a0ff-241">[URL vidéo YouTube valide pour votre extension][MicrosoftEdgeAddonsUploadYouTubeVideo].</span><span class="sxs-lookup"><span data-stu-id="9a0ff-241">A valid [YouTube video URL for your Extension][MicrosoftEdgeAddonsUploadYouTubeVideo].</span></span>  <span data-ttu-id="9a0ff-242">Votre vidéo devrait être de bonne qualité et de longueur minimale.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-242">Your video should be good quality and minimal length.</span></span>  <span data-ttu-id="9a0ff-243">Votre vidéo YouTube doit réussir la certification avant de publier votre extension dans les compléments Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-243">Your YouTube video must pass certification before publishing your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="9a0ff-244">Vérifiez que votre vidéo YouTube est compatible avec le [document des stratégies du développeur Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="9a0ff-244">Verify that your YouTube video complies with the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="9a0ff-245">**Valeurs possibles**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-245">**Possible Values**:</span></span>  

*   <span data-ttu-id="9a0ff-246">10 captures d’écran maximum.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-246">10 Screenshots maximum.</span></span>  
    *   <span data-ttu-id="9a0ff-247">640 pixels x 480px, PNG \ (. png \): captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-247">640px x 480px, PNG \(.png\):  Screenshots.</span></span>  
    *   <span data-ttu-id="9a0ff-248">1280px x 800px, PNG \ (. png \): captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-248">1280px x 800px, PNG \(.png\):  Screenshots.</span></span>  
*   <span data-ttu-id="9a0ff-249">1400px x 560px, PNG \ (. png \): grande vignette de promotion.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-249">1400px x 560px, PNG \(.png\):  Large promotion tiles.</span></span>  
*   <span data-ttu-id="9a0ff-250">URL de la vidéo YouTube de 60 secondes ou courtes de 2 Go ou moins.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-250">60 seconds or shorter and 2GB or smaller, YouTube video URL.</span></span>  

#### <span data-ttu-id="9a0ff-251">Description courte</span><span class="sxs-lookup"><span data-stu-id="9a0ff-251">Short description</span></span>  

<span data-ttu-id="9a0ff-252">Brève description qui est susceptible d’être utilisée en haut de la liste pour votre produit.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-252">A short, catchy description that may be used at the top of the listing for your product.</span></span>  <span data-ttu-id="9a0ff-253">Si ce n’est pas le cas, les premières lignes de votre description plus longue seront utilisées à la place.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-253">If not provided, the first few lines from your longer description are used instead.</span></span>  <span data-ttu-id="9a0ff-254">Dans la mesure où votre description apparaît également sous ce texte, vous devez fournir une courte description contenant un texte différent de sorte que votre liste soit moins répétitive.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-254">Because your description also appears below this text, you should provide a short description with different text so that your listing is less repetitive.</span></span>  <span data-ttu-id="9a0ff-255">La brève description de votre extension est choisie directement dans le fichier manifeste de votre package.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-255">The Short description of your Extension is picked directly from the manifest file of your package.</span></span>  

> [!NOTE]
> <span data-ttu-id="9a0ff-256">Pour modifier la brève description, vous devez mettre à jour le manifeste dans votre package d’extension et le télécharger à nouveau.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-256">To edit the short description, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="9a0ff-257">Termes de recherche</span><span class="sxs-lookup"><span data-stu-id="9a0ff-257">Search terms</span></span>  

<span data-ttu-id="9a0ff-258">Les termes de recherche sont des mots uniques ou des phrases courtes qui ne sont pas visibles pour les utilisateurs, mais aident à rendre votre extension détectable par les modules complémentaires Microsoft Edge lorsque les utilisateurs effectuent des recherches en utilisant ces termes.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-258">Search terms are single words or short phrases that are not displayed to users but help make your Extension discoverable in Microsoft Edge Addons when users search using those terms.</span></span>  

<span data-ttu-id="9a0ff-259">**Configuration requise**:</span><span class="sxs-lookup"><span data-stu-id="9a0ff-259">**Requirements**:</span></span>  

*   <span data-ttu-id="9a0ff-260">7 ou moins termes de recherche</span><span class="sxs-lookup"><span data-stu-id="9a0ff-260">7 or fewer search terms</span></span>  
*   <span data-ttu-id="9a0ff-261">30 caractères au maximum par critère de recherche</span><span class="sxs-lookup"><span data-stu-id="9a0ff-261">30 or fewer characters per search term</span></span>  
*   <span data-ttu-id="9a0ff-262">21 ou moins de mots pour les termes de recherche combinés</span><span class="sxs-lookup"><span data-stu-id="9a0ff-262">21 or fewer words for combined search terms</span></span>  

<span data-ttu-id="9a0ff-263">Cliquez sur **Enregistrer** pour continuer pour enregistrer la section de votre annonce.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-263">Click **Save** to proceed to save your listing section.</span></span>  <span data-ttu-id="9a0ff-264">Cliquez sur **publier** pour fournir des informations de soumission.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-264">Click **Publish** to provide submission details.</span></span>  

## <span data-ttu-id="9a0ff-265">Étape 6: terminer votre soumission et cliquer sur publier</span><span class="sxs-lookup"><span data-stu-id="9a0ff-265">Step 6: Complete your submission and click Publish</span></span>  

<span data-ttu-id="9a0ff-266">La page d’options de soumission du processus de soumission d’extension vous permet de fournir des informations supplémentaires pour nous aider à tester correctement votre produit.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-266">The Submission options page of the Extension submission process is where you provide more information to help us test your product properly.</span></span>  <span data-ttu-id="9a0ff-267">Il s’agit d’une étape facultative, mais elle est recommandée pour de nombreux envois.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-267">This is an optional step, but it is recommended for many submissions.</span></span>  

### <span data-ttu-id="9a0ff-268">Options de mise en attente de publication</span><span class="sxs-lookup"><span data-stu-id="9a0ff-268">Publishing hold options</span></span>  

<span data-ttu-id="9a0ff-269">Par défaut, votre soumission est publiée dès qu’elle passe une certification.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-269">By default, your submission is published as soon as it passes certification.</span></span>  <span data-ttu-id="9a0ff-270">Vous pouvez décider de mettre en attente la publication de votre soumission jusqu’à une date spécifique.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-270">You may choose to place a hold on publishing your submission until a specific date.</span></span>  <span data-ttu-id="9a0ff-271">Les options disponibles dans cette section sont décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-271">The options in this section are described below.</span></span>  

*   **<span data-ttu-id="9a0ff-272">Publier votre soumission dès qu’elle passe la certification</span><span class="sxs-lookup"><span data-stu-id="9a0ff-272">Publish your submission as soon as it passes certification</span></span>**  

    <span data-ttu-id="9a0ff-273">Il s’agit de la sélection par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-273">This is the default selection.</span></span>  <span data-ttu-id="9a0ff-274">Cela signifie que votre soumission commence le processus de publication dès qu’il passe une certification.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-274">It means that your submission begins the publishing process as soon as it passes certification</span></span>  

*   **<span data-ttu-id="9a0ff-275">Démarrer la publication de votre soumission à une date donnée</span><span class="sxs-lookup"><span data-stu-id="9a0ff-275">Start publishing your submission on a certain date</span></span>**  

    <span data-ttu-id="9a0ff-276">Pour vous assurer que la soumission ne sera pas publiée avant une date spécifique, sélectionnez **commencer la publication de votre soumission à une date donnée** .</span><span class="sxs-lookup"><span data-stu-id="9a0ff-276">Choose **Start publishing your submission on a certain date** to ensure that the submission is not published until a specific date.</span></span>  <span data-ttu-id="9a0ff-277">Avec cette option, votre soumission est publiée aussitôt que possible à la date spécifiée ou après.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-277">With this option, your submission is released as soon as possible on or after the date you specify.</span></span>  <span data-ttu-id="9a0ff-278">La date doit être postérieure de 24 heures au moins.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-278">The date must be at least 24 hours in the future.</span></span>  <span data-ttu-id="9a0ff-279">Parallèlement à la date, vous pouvez spécifier l’heure à laquelle la publication de la soumission doit commencer.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-279">Along with the date, you may specify the time at which the submission should begin to be published.</span></span>  

### <span data-ttu-id="9a0ff-280">Remarques pour la certification</span><span class="sxs-lookup"><span data-stu-id="9a0ff-280">Notes for certification</span></span>  

<span data-ttu-id="9a0ff-281">Lorsque vous envoyez votre extension, vous avez la possibilité d’utiliser la page remarques pour la certification pour fournir des informations supplémentaires aux testeurs de certification.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-281">As you submit your Extension, you have the option to use the Notes for certification page to provide additional information to the certification testers.</span></span>  <span data-ttu-id="9a0ff-282">Ces informations permettent de vérifier que votre extension est testée correctement.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-282">This information helps ensure that your Extension is tested correctly.</span></span>  <span data-ttu-id="9a0ff-283">Si nous ne sommes pas en mesure d’effectuer un test total de votre soumission, la certification peut échouer.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-283">If we are not able to fully test your submission, it may fail certification.</span></span>  

<span data-ttu-id="9a0ff-284">Veillez à inclure les éléments suivants (le cas échéant):</span><span class="sxs-lookup"><span data-stu-id="9a0ff-284">Make sure to include the following \(if applicable for your Extension\):</span></span>  

*   <span data-ttu-id="9a0ff-285">Noms d’utilisateurs et mots de passe pour les comptes de test.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-285">User names and passwords for test accounts.</span></span>  
*   <span data-ttu-id="9a0ff-286">Étapes à suivre pour accéder aux fonctionnalités masquées ou verrouillées.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-286">Steps to access hidden or locked features.</span></span>  
*   <span data-ttu-id="9a0ff-287">Différences attendues du comportement en fonction de la région ou d’autres paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-287">Expected differences in behavior based on region or other user settings.</span></span>  
*   <span data-ttu-id="9a0ff-288">Informations sur les modifications apportées à la mise à jour d’une application.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-288">Information about what changed in an app update.</span></span>  
*   <span data-ttu-id="9a0ff-289">Tout d’abord, vous pensez que les testeurs doivent comprendre votre soumission.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-289">Anything else you think testers must understand about your submission.</span></span>  

<span data-ttu-id="9a0ff-290">Après avoir rempli les informations ci-dessus, cliquez sur **publier** pour valider votre extension dans les compléments Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-290">After completing the above details, click **Publish** to submit your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="9a0ff-291">Lorsque vous avez terminé de créer la soumission pour votre extension et cliqué sur **publier**, la soumission entre dans l’étape de certification.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-291">When you finish creating the submission for your Extension and click **Publish**, the submission enters the certification step.</span></span>  <span data-ttu-id="9a0ff-292">Ce processus s’effectue généralement dans un délai de deux jours, mais dans certains cas cela peut prendre jusqu’à 7 jours ouvrables.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-292">This process usually is completed within a couple of days, though in some cases it may take up to 7 business days.</span></span>  <span data-ttu-id="9a0ff-293">Une fois votre soumission certifiée, votre extension est publiée dans les modules complémentaires Microsoft Edge, sauf si vous avez sélectionné les options de conservation de publication pour spécifier qu’elle ne doit pas être publiée avant une date donnée.</span><span class="sxs-lookup"><span data-stu-id="9a0ff-293">After your submission passes certification, your Extension is published in Microsoft Edge Addons unless you selected the Publishing hold options to specify that it should not be released until a certain date.</span></span>  <span data-ttu-id="9a0ff-294">Vous êtes averti lorsque votre soumission est publiée et que le statut de votre extension dans le tableau de bord devient `In the Store` .</span><span class="sxs-lookup"><span data-stu-id="9a0ff-294">You are notified when your submission is published, and the status of your Extension in the dashboard changes to `In the Store`.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Mise en route des extensions Microsoft Edge \ (chrome \) | Documents Microsoft"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Télécharger une vidéo YouTube | Documents Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Stratégies développeurs de catalogue Microsoft Edge addons | Documents Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrat du développeur de l’application | Documents Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centre de partenariat"  
