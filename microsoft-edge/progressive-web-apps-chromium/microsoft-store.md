---
description: Rendre votre PWA plus découvrable en publiant dans le Microsoft Store
title: Publier votre application web progressive sur le Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: applications web progressives, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 68471535446a2270a23b32205717da225fd9e4bf
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461506"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="6050e-104">Publier votre application web progressive sur le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="6050e-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="6050e-105">La publication de votre application web progressive \(PWA\) dans le [Microsoft Store][WindowsUwpPublishIndex] offre les avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="6050e-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="6050e-106">Détectabilité</span><span class="sxs-lookup"><span data-stu-id="6050e-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="6050e-107">Les utilisateurs recherchent naturellement des applications dans l’App Store.</span><span class="sxs-lookup"><span data-stu-id="6050e-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="6050e-108">En publiant sur le Microsoft Store, des millions d’utilisateurs de Windows peuvent découvrir votre PWA avec d’autres applications Windows.</span><span class="sxs-lookup"><span data-stu-id="6050e-108">By publishing to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="6050e-109">Le Windows Store présente les applications par le biais de catégories, de collections organisées, etc.</span><span class="sxs-lookup"><span data-stu-id="6050e-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="6050e-110">Les portails de découverte d’applications offrent une expérience de navigation et d’achat facile pour les utilisateurs potentiels de votre application.</span><span class="sxs-lookup"><span data-stu-id="6050e-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="6050e-111">Vous pouvez même améliorer [votre liste dans le Store][WindowsUwpPublishAppScreenshotsImages] avec des captures d’écran, une image hero et des bandes-annonces vidéo.</span><span class="sxs-lookup"><span data-stu-id="6050e-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="6050e-112">Trustiness</span><span class="sxs-lookup"><span data-stu-id="6050e-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="6050e-113">Les clients Windows savent qu’ils peuvent faire confiance à leurs achats et téléchargements au Microsoft Store, car ils respectent les normes rigoureuses de qualité [et de sécurité de][LegalWindowsAgreementsStorePolicies]Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6050e-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="6050e-114">Installation facile</span><span class="sxs-lookup"><span data-stu-id="6050e-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="6050e-115">Le Microsoft Store offre une expérience d’installation cohérente et conviviale dans toutes [les applications Windows 10.][MicrosoftStoreAppsWindows]</span><span class="sxs-lookup"><span data-stu-id="6050e-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="6050e-116">Analyse de l’application</span><span class="sxs-lookup"><span data-stu-id="6050e-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="6050e-117">Le tableau de bord [][WindowsUwpPublishAnalytics] [de l’Partner Center Windows][WindowsUwpPublishIndex] vous fournit des analyses détaillées sur l’état, l’utilisation et bien plus encore de votre application.</span><span class="sxs-lookup"><span data-stu-id="6050e-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="6050e-118">Pour publier votre PWA sur le Microsoft Store, aucune modification de code n’est requise.</span><span class="sxs-lookup"><span data-stu-id="6050e-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="6050e-119">Au lieu de cela, vous créez une réservation d’application, créez un package PWA et soumettez votre package au Store.</span><span class="sxs-lookup"><span data-stu-id="6050e-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="6050e-120">Les sections suivantes expliquent les étapes.</span><span class="sxs-lookup"><span data-stu-id="6050e-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="6050e-121">Créer une réservation d’application</span><span class="sxs-lookup"><span data-stu-id="6050e-121">Create an app reservation</span></span>  

<span data-ttu-id="6050e-122">[L’Partner Center Windows][MicrosoftPartnerDashboardWindowsOverview] est le hub qui vous permet de soumettre votre application au Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6050e-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="6050e-123">Pour créer une réservation d’application, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="6050e-124">Pour afficher vos programmes inscrits, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="6050e-125">Connectez-vous à l’Partner Center Windows avec votre compte Microsoft et accédez au [tableau de bord de l’Centre partenaires.][MicrosoftPartnerDashboardHome]</span><span class="sxs-lookup"><span data-stu-id="6050e-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="6050e-126">Accéder à **Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="6050e-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="6050e-127">Si **Windows & Xbox** est affiché, votre application est déjà inscrite.</span><span class="sxs-lookup"><span data-stu-id="6050e-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="6050e-128">Si **Windows & Xbox** n’est pas affiché, choisissez Ajouter un **programme.**</span><span class="sxs-lookup"><span data-stu-id="6050e-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Ajouter un programme dans le tableau de bord de l’Centre de partenaires Windows" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="6050e-130">Ajouter un programme dans le tableau de bord de l’Centre de partenaires Windows</span><span class="sxs-lookup"><span data-stu-id="6050e-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="6050e-131">Pour vous inscrire au programme pour les développeurs, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="6050e-132">Accédez **à Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="6050e-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="6050e-133">Choose **Get started**.</span><span class="sxs-lookup"><span data-stu-id="6050e-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="6050e-134">Suivez les instructions.</span><span class="sxs-lookup"><span data-stu-id="6050e-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="6050e-135">À présent, votre application est inscrite au programme pour les développeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="6050e-135">Now, your app is enrolled in the app developer program.</span></span> <span data-ttu-id="6050e-136">Pour créer une réservation d’application, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="6050e-137">Accédez **à Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="6050e-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="6050e-138">Choose **Overview**  >  **Create a new app**.</span><span class="sxs-lookup"><span data-stu-id="6050e-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="6050e-139">Tapez votre nom PWA dans l’invite.</span><span class="sxs-lookup"><span data-stu-id="6050e-139">Type your PWA name in the prompt.</span></span>  
    1.  <span data-ttu-id="6050e-140">Choose `Reserve product name` .</span><span class="sxs-lookup"><span data-stu-id="6050e-140">Choose `Reserve product name`.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Créer une réservation d’application dans l’Espace partenaires Windows" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="6050e-142">Créer une réservation d’application dans l’Espace partenaires Windows</span><span class="sxs-lookup"><span data-stu-id="6050e-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="6050e-143">Pour afficher les détails de votre éditeur à utiliser dans la section [Package de votre PWA,](#package-your-pwa) choisissez **Product management**  >  **Product Identity**.</span><span class="sxs-lookup"><span data-stu-id="6050e-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copier les informations de votre éditeur à partir de l’Centre de partenaires Windows" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="6050e-145">Copier les informations de votre éditeur à partir de l’Centre de partenaires Windows</span><span class="sxs-lookup"><span data-stu-id="6050e-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="6050e-146">Copiez et enregistrez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="6050e-147">Package ID</span><span class="sxs-lookup"><span data-stu-id="6050e-147">Package ID</span></span>**  
    *   **<span data-ttu-id="6050e-148">ID de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="6050e-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="6050e-149">Nom complet de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="6050e-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa"></a><span data-ttu-id="6050e-150">Package de votre PWA</span><span class="sxs-lookup"><span data-stu-id="6050e-150">Package your PWA</span></span>  

<span data-ttu-id="6050e-151">Générez un package d’application Windows pour votre application PWA.</span><span class="sxs-lookup"><span data-stu-id="6050e-151">Generate a Windows app package for your PWA.</span></span>  

<span data-ttu-id="6050e-152">Votre package d’application est un fichier qui contient les métadonnées de votre application, notamment le nom, la description, les `.msixbundle` icônes, etc.</span><span class="sxs-lookup"><span data-stu-id="6050e-152">Your app package is an `.msixbundle` file that contains the metadata of your app including the name, description, icons, and so on.</span></span>  <span data-ttu-id="6050e-153">Il utilise le [modèle d’application hébergée,][WindowsBlogWindowsdeveloperHostedAppModel]avec Microsoft Edge qui met votre PWA sous alimentation.</span><span class="sxs-lookup"><span data-stu-id="6050e-153">It uses the [Hosted App Model][WindowsBlogWindowsdeveloperHostedAppModel], with Microsoft Edge powering your PWA.</span></span>  <span data-ttu-id="6050e-154">Dans ce modèle, votre PWA utilise des fonctionnalités web modernes tout en fonctionnant comme une application Windows.</span><span class="sxs-lookup"><span data-stu-id="6050e-154">In this model, your PWA uses modern web capabilities while functioning as a Windows app.</span></span>  <span data-ttu-id="6050e-155">Les fonctionnalités web modernes incluent le service de travail, hors connexion, les notifications Push, les mauvaises utilisations, etc.</span><span class="sxs-lookup"><span data-stu-id="6050e-155">Modern web capabilities include service worker, offline, push notifications, badging, and more.</span></span>  

<span data-ttu-id="6050e-156">Pour générer un package d’application, réalisez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-156">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="6050e-157">Accédez au [Générateur PWA.][PwabuilderMain]</span><span class="sxs-lookup"><span data-stu-id="6050e-157">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="6050e-158">Tapez l’URL de votre PWA.</span><span class="sxs-lookup"><span data-stu-id="6050e-158">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="6050e-159">Choose **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.</span><span class="sxs-lookup"><span data-stu-id="6050e-159">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="6050e-160">Collez les valeurs suivantes que vous avez enregistrées dans la section Créer une réservation [d’application.](#create-an-app-reservation)</span><span class="sxs-lookup"><span data-stu-id="6050e-160">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="6050e-161">Package ID</span><span class="sxs-lookup"><span data-stu-id="6050e-161">Package ID</span></span>**  
    *   **<span data-ttu-id="6050e-162">ID de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="6050e-162">Publisher ID</span></span>**  
    *   **<span data-ttu-id="6050e-163">Nom complet de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="6050e-163">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Coller des informations sur l’éditeur dans PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="6050e-165">Coller des informations sur l’éditeur dans PWABuilder</span><span class="sxs-lookup"><span data-stu-id="6050e-165">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6050e-166">Choisissez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="6050e-166">Choose **Done**.</span></span>  
1.  <span data-ttu-id="6050e-167">Pour télécharger votre package d’application Windows, choisissez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="6050e-167">To download your Windows app package, choose **Download**.</span></span>  <span data-ttu-id="6050e-168">Votre téléchargement est une `.zip` archive contenant un `.msixbundle` fichier.</span><span class="sxs-lookup"><span data-stu-id="6050e-168">Your download is a `.zip` archive containing an `.msixbundle` file.</span></span>  <span data-ttu-id="6050e-169">Utilisez le `.msixbundle` fichier de la section Envoyer votre package [d’application au Store.](#submit-your-app-package-to-the-store)</span><span class="sxs-lookup"><span data-stu-id="6050e-169">Use the `.msixbundle` file in the [Submit your app package to the Store](#submit-your-app-package-to-the-store) section.</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="6050e-170">Soumettre votre package d’application au Store</span><span class="sxs-lookup"><span data-stu-id="6050e-170">Submit your app package to the Store</span></span>  

<span data-ttu-id="6050e-171">Vous avez maintenant votre `.msixbundle` package d’application.</span><span class="sxs-lookup"><span data-stu-id="6050e-171">Now, you have your `.msixbundle` app package.</span></span>  <span data-ttu-id="6050e-172">Pour soumettre votre package d’application au Store, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="6050e-172">To submit your app package to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="6050e-173">Accéder à [l’Centre partenaires Windows][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="6050e-173">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="6050e-174">Choisissez votre application.</span><span class="sxs-lookup"><span data-stu-id="6050e-174">Choose your app.</span></span>  
1.  <span data-ttu-id="6050e-175">Choisissez **Démarrer votre soumission.**</span><span class="sxs-lookup"><span data-stu-id="6050e-175">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Démarrer une soumission d’application sur l’Partner Center Windows" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="6050e-177">Démarrer une soumission d’application sur l’Partner Center Windows</span><span class="sxs-lookup"><span data-stu-id="6050e-177">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6050e-178">Remplissez les invites suivantes pour obtenir des informations sur votre application.</span><span class="sxs-lookup"><span data-stu-id="6050e-178">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="6050e-179">pricing</span><span class="sxs-lookup"><span data-stu-id="6050e-179">pricing</span></span>  
    *   <span data-ttu-id="6050e-180">classification par âge</span><span class="sxs-lookup"><span data-stu-id="6050e-180">age rating</span></span>  
    *   <span data-ttu-id="6050e-181">et plus</span><span class="sxs-lookup"><span data-stu-id="6050e-181">and more</span></span>  
        
1.  <span data-ttu-id="6050e-182">À **l’invite packages,** choisissez le fichier généré dans `.msixbundle` la section Package de votre [PWA.](#package-your-pwa)</span><span class="sxs-lookup"><span data-stu-id="6050e-182">On the **Packages** prompt, choose the `.msixbundle` file your generated in the [Package your PWA](#package-your-pwa) section.</span></span>  

<span data-ttu-id="6050e-183">Une fois votre soumission terminée, votre application est examinée, généralement dans un délai de 24 à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="6050e-183">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="6050e-184">Une fois que vous avez reçu l’approbation, votre PWA est disponible dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6050e-184">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Stratégies du Microsoft Store | Documents Microsoft"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analyser les performances de l'| Documents Microsoft"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Captures d’écran, images et bandes-annonces de l’application | Documents Microsoft"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publier des applications et des jeux Windows | Documents Microsoft"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Accueil | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressources pour les partenaires | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modèle d’application hébergée | Blog des développeurs Windows"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  

