---
description: Rendez votre PWA plus découvrable en publiant dans le Microsoft Store
title: Publier votre application web progressive sur le Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: applications web progressives, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 40a6b94412a0788c87f7231025809098c98f18e9
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643248"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="207f0-104">Publier votre application web progressive sur le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="207f0-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="207f0-105">La publication de votre application web progressive \(PWA\) sur le [Microsoft Store][WindowsUwpPublishIndex] apporte les avantages suivants.</span><span class="sxs-lookup"><span data-stu-id="207f0-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="207f0-106">Détectabilité</span><span class="sxs-lookup"><span data-stu-id="207f0-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="207f0-107">Les utilisateurs recherchent naturellement des applications dans l’App Store.</span><span class="sxs-lookup"><span data-stu-id="207f0-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="207f0-108">Lorsque vous publiez sur le Microsoft Store, des millions Windows utilisateurs peuvent découvrir vos PWA avec d’autres Windows applications.</span><span class="sxs-lookup"><span data-stu-id="207f0-108">When you publish to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="207f0-109">Le Windows Store présente les applications par le biais de catégories, de collections organisées, etc.</span><span class="sxs-lookup"><span data-stu-id="207f0-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="207f0-110">Les portails de découverte d’applications offrent une expérience de navigation et d’achat facile pour les utilisateurs potentiels de votre application.</span><span class="sxs-lookup"><span data-stu-id="207f0-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="207f0-111">Vous pouvez même améliorer [votre liste dans][WindowsUwpPublishAppScreenshotsImages] le Store avec des captures d’écran, une image Hero et des bandes-annonces vidéo.</span><span class="sxs-lookup"><span data-stu-id="207f0-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="207f0-112">Trustiness</span><span class="sxs-lookup"><span data-stu-id="207f0-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="207f0-113">Windows clients savent qu’ils peuvent faire confiance à leurs achats Microsoft Store et téléchargements, car ils respectent les normes rigoureuses de qualité et [de sécurité de][LegalWindowsAgreementsStorePolicies]Microsoft.</span><span class="sxs-lookup"><span data-stu-id="207f0-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="207f0-114">Installation facile</span><span class="sxs-lookup"><span data-stu-id="207f0-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="207f0-115">Le Microsoft Store offre une expérience d’installation cohérente et conviviale dans [toutes les Windows 10 applications.][MicrosoftStoreAppsWindows]</span><span class="sxs-lookup"><span data-stu-id="207f0-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="207f0-116">Analyse de l’application</span><span class="sxs-lookup"><span data-stu-id="207f0-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="207f0-117">Le [tableau Windows de l’Partner Center][WindowsUwpPublishIndex] vous fournit des analyses détaillées sur l’état, l’utilisation et bien plus encore de votre application. [][WindowsUwpPublishAnalytics]</span><span class="sxs-lookup"><span data-stu-id="207f0-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="207f0-118">Pour publier votre PWA sur le Microsoft Store, aucune modification de code n’est requise.</span><span class="sxs-lookup"><span data-stu-id="207f0-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="207f0-119">Au lieu de cela, vous créez une réservation d’application, créez un package PWA et soumettez votre package au Store.</span><span class="sxs-lookup"><span data-stu-id="207f0-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="207f0-120">Les sections suivantes expliquent les étapes.</span><span class="sxs-lookup"><span data-stu-id="207f0-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="207f0-121">Créer une réservation d’application</span><span class="sxs-lookup"><span data-stu-id="207f0-121">Create an app reservation</span></span>  

<span data-ttu-id="207f0-122">[Windows’Partner Center][MicrosoftPartnerDashboardWindowsOverview] est le hub qui vous permet de soumettre votre application au Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="207f0-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="207f0-123">Pour créer une réservation d’application, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="207f0-124">Pour afficher vos programmes inscrits, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="207f0-125">Connectez-Windows l’Partner Center avec votre compte Microsoft et accédez au tableau de bord de [l’Centre partenaires.][MicrosoftPartnerDashboardHome]</span><span class="sxs-lookup"><span data-stu-id="207f0-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="207f0-126">Accéder à **Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="207f0-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="207f0-127">Si **Windows & Xbox** est affichée, votre application est déjà inscrite.</span><span class="sxs-lookup"><span data-stu-id="207f0-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="207f0-128">Si **Windows & Xbox** n’est pas affichée, choisissez Ajouter un **programme.**</span><span class="sxs-lookup"><span data-stu-id="207f0-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Ajouter un programme dans le tableau de bord Windows l’Partner Center" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="207f0-130">Ajouter un programme dans le tableau de bord Windows l’Partner Center</span><span class="sxs-lookup"><span data-stu-id="207f0-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="207f0-131">Pour vous inscrire au programme pour les développeurs, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="207f0-132">Accédez à **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="207f0-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="207f0-133">Choose **Get started**.</span><span class="sxs-lookup"><span data-stu-id="207f0-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="207f0-134">Suivez les instructions.</span><span class="sxs-lookup"><span data-stu-id="207f0-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="207f0-135">À présent, votre compte est inscrit au programme pour les développeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="207f0-135">Now, your account is enrolled in the app developer program.</span></span> <span data-ttu-id="207f0-136">Pour créer une réservation d’application, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="207f0-137">Accédez à **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="207f0-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="207f0-138">Choose **Overview**  >  **Create a new app**.</span><span class="sxs-lookup"><span data-stu-id="207f0-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="207f0-139">Tapez le nom de votre application dans l’invite.</span><span class="sxs-lookup"><span data-stu-id="207f0-139">Type the name of your app in the prompt.</span></span>  
    1.  <span data-ttu-id="207f0-140">Choose `Reserve product name` .</span><span class="sxs-lookup"><span data-stu-id="207f0-140">Choose `Reserve product name`.</span></span>  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Créer une réservation d’application dans Windows’espace partenaires" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="207f0-142">Créer une réservation d’application dans Windows’espace partenaires</span><span class="sxs-lookup"><span data-stu-id="207f0-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="207f0-143">Pour afficher les détails de votre éditeur à utiliser dans la section Package de [votre PWA,](#package-your-pwa-for-the-store) choisissez **Product management**  >  **Product Identity**.</span><span class="sxs-lookup"><span data-stu-id="207f0-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa-for-the-store) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copier les informations de votre éditeur à partir Windows l’Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="207f0-145">Copier les informations de votre éditeur à partir Windows l’Partner Center</span><span class="sxs-lookup"><span data-stu-id="207f0-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="207f0-146">Copiez et enregistrez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="207f0-147">Package ID</span><span class="sxs-lookup"><span data-stu-id="207f0-147">Package ID</span></span>**  
    *   **<span data-ttu-id="207f0-148">Publisher ID</span><span class="sxs-lookup"><span data-stu-id="207f0-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="207f0-149">Publisher Nom complet</span><span class="sxs-lookup"><span data-stu-id="207f0-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa-for-the-store"></a><span data-ttu-id="207f0-150">Package de votre PWA pour le Store</span><span class="sxs-lookup"><span data-stu-id="207f0-150">Package your PWA for the Store</span></span> 

<span data-ttu-id="207f0-151">Maintenant que vous avez les informations de publication de votre application, générez un package Windows’application pour votre PWA.</span><span class="sxs-lookup"><span data-stu-id="207f0-151">Now that you have your app publishing information, generate a Windows app package for your PWA.</span></span>

<span data-ttu-id="207f0-152">Pour générer un package d’application, réalisez les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-152">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="207f0-153">Accédez [à PWA Générateur.][PwabuilderMain]</span><span class="sxs-lookup"><span data-stu-id="207f0-153">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="207f0-154">Tapez l’URL de votre PWA.</span><span class="sxs-lookup"><span data-stu-id="207f0-154">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="207f0-155">Choose **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.</span><span class="sxs-lookup"><span data-stu-id="207f0-155">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="207f0-156">Collez les valeurs suivantes que vous avez enregistrées dans la section Créer une réservation [d’application.](#create-an-app-reservation)</span><span class="sxs-lookup"><span data-stu-id="207f0-156">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="207f0-157">Package ID</span><span class="sxs-lookup"><span data-stu-id="207f0-157">Package ID</span></span>**  
    *   **<span data-ttu-id="207f0-158">Publisher ID</span><span class="sxs-lookup"><span data-stu-id="207f0-158">Publisher ID</span></span>**  
    *   **<span data-ttu-id="207f0-159">Publisher Nom complet</span><span class="sxs-lookup"><span data-stu-id="207f0-159">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Coller des informations sur l’éditeur dans PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="207f0-161">Coller des informations sur l’éditeur dans PWABuilder</span><span class="sxs-lookup"><span data-stu-id="207f0-161">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="207f0-162">Choisissez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="207f0-162">Choose **Done**.</span></span>  
1.  <span data-ttu-id="207f0-163">Pour télécharger votre package Windows’application, choisissez **Télécharger.**</span><span class="sxs-lookup"><span data-stu-id="207f0-163">To download your Windows app package, choose **Download**.</span></span>

<span data-ttu-id="207f0-164">Votre téléchargement est une `.zip` archive qui contient un fichier et un `.msixbundle` `.classic.appxbundle` fichier.</span><span class="sxs-lookup"><span data-stu-id="207f0-164">Your download is a `.zip` archive that contains an `.msixbundle` file and a `.classic.appxbundle` file.</span></span>  <span data-ttu-id="207f0-165">Les deux packages d’application permettent à votre PWA de s’exécuter sur un large éventail de versions Windows de l’application.</span><span class="sxs-lookup"><span data-stu-id="207f0-165">The two app packages allow your PWA to run on a wide variety of Windows versions.</span></span>  <span data-ttu-id="207f0-166">Pour plus d’informations, accédez à [Qu’est-ce qu’un package classique ?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span><span class="sxs-lookup"><span data-stu-id="207f0-166">For more information, navigate to [What is a classic package?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="207f0-167">Soumettre votre package d’application au Store</span><span class="sxs-lookup"><span data-stu-id="207f0-167">Submit your app package to the Store</span></span>  

<span data-ttu-id="207f0-168">Pour soumettre votre application au Store, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="207f0-168">To submit your app to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="207f0-169">Accédez à [Windows l’Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="207f0-169">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="207f0-170">Choisissez votre application.</span><span class="sxs-lookup"><span data-stu-id="207f0-170">Choose your app.</span></span>  
1.  <span data-ttu-id="207f0-171">Choisissez **Démarrer votre soumission.**</span><span class="sxs-lookup"><span data-stu-id="207f0-171">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Démarrer une nouvelle soumission d’application sur Windows l’Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="207f0-173">Démarrer une nouvelle soumission d’application sur Windows l’Partner Center</span><span class="sxs-lookup"><span data-stu-id="207f0-173">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="207f0-174">Remplissez les invites suivantes pour obtenir des informations sur votre application.</span><span class="sxs-lookup"><span data-stu-id="207f0-174">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="207f0-175">pricing</span><span class="sxs-lookup"><span data-stu-id="207f0-175">pricing</span></span>  
    *   <span data-ttu-id="207f0-176">classification par âge</span><span class="sxs-lookup"><span data-stu-id="207f0-176">age rating</span></span>  
    *   <span data-ttu-id="207f0-177">et plus</span><span class="sxs-lookup"><span data-stu-id="207f0-177">and more</span></span>  
        
1.  <span data-ttu-id="207f0-178">À **l’invite packages,** choisissez les fichiers que vous avez générés dans la `.msixbundle` `.classic.appxbundle` section [Packages PWA.](#package-your-pwa-for-the-store)</span><span class="sxs-lookup"><span data-stu-id="207f0-178">On the **Packages** prompt, choose the `.msixbundle` and the `.classic.appxbundle` files you generated in the [Package your PWA](#package-your-pwa-for-the-store) section.</span></span>  
    
<span data-ttu-id="207f0-179">Une fois votre soumission terminée, votre application est examinée, généralement dans un délai de 24 à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="207f0-179">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="207f0-180">Une fois que vous avez reçu l’approbation, votre PWA est disponible dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="207f0-180">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

### <a name="measure-usage-of-your-store-installed-pwa"></a><span data-ttu-id="207f0-181">Mesurer l’utilisation de vos PWA</span><span class="sxs-lookup"><span data-stu-id="207f0-181">Measure usage of your Store-installed PWA</span></span>

<span data-ttu-id="207f0-182">Lors du lancement initial de votre PWA, si le PWA a été installé à partir de l’Microsoft Store, Microsoft Edge inclut l’en-tête suivant avec la demande de la première navigation de votre application `Referer` web.</span><span class="sxs-lookup"><span data-stu-id="207f0-182">When your PWA is initially launched, if the PWA was installed from the Microsoft Store, Microsoft Edge includes the following `Referer` header with the request for the first navigation of your web app.</span></span>

```
Referer: app-info://platform/microsoft-store
```

<span data-ttu-id="207f0-183">Utilisez cette fonctionnalité pour mesurer le trafic distinct de votre PWA.</span><span class="sxs-lookup"><span data-stu-id="207f0-183">Use this feature to measure distinct traffic from your Store-installed PWA.</span></span>  <span data-ttu-id="207f0-184">En fonction du trafic, vous pouvez ajuster le contenu de votre application pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="207f0-184">Based on the traffic, you can adjust your app’s content to improve the user experience.</span></span>  <span data-ttu-id="207f0-185">Cette fonctionnalité est accessible au code client et au code serveur.</span><span class="sxs-lookup"><span data-stu-id="207f0-185">This feature is accessible to both client and server code.</span></span>

<span data-ttu-id="207f0-186">Cette fonctionnalité a été introduite dans Microsoft Edge version 91.</span><span class="sxs-lookup"><span data-stu-id="207f0-186">This feature was introduced in Microsoft Edge version 91.</span></span>

## <a name="see-also"></a><span data-ttu-id="207f0-187">Voir également</span><span class="sxs-lookup"><span data-stu-id="207f0-187">See also</span></span>  

<span data-ttu-id="207f0-188">PWABuilder fournit plus de documentation pour vous aider à obtenir votre PWA dans la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="207f0-188">PWABuilder provides more documentation to help you get your PWA in the Microsoft Store.</span></span>  

*   [<span data-ttu-id="207f0-189">Testez et soumettez votre package d PWA de messagerie un peu plus complet</span><span class="sxs-lookup"><span data-stu-id="207f0-189">Test and submit your PWA app package</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [<span data-ttu-id="207f0-190">Publier une nouvelle PWA dans le Store</span><span class="sxs-lookup"><span data-stu-id="207f0-190">Publish a new PWA to the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [<span data-ttu-id="207f0-191">Mettre à jour une application du Store existante vers une PWA</span><span class="sxs-lookup"><span data-stu-id="207f0-191">Update an existing Store app to a PWA</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [<span data-ttu-id="207f0-192">Recommandations en matière d’images pour les P PWA dans le Store</span><span class="sxs-lookup"><span data-stu-id="207f0-192">Image recommendations for PWAs in the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [<span data-ttu-id="207f0-193">Expliqueur de l’empaquetage d’application</span><span class="sxs-lookup"><span data-stu-id="207f0-193">App packaging explainer</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store Stratégies | Documents Microsoft"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analyser les performances de l'| Documents Microsoft"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Captures d’écran, images et bandes-annonces de l’application | Documents Microsoft"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publier Windows applications et jeux | Documents Microsoft"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Accueil | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressources pour les partenaires | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Applications | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modèle d’application hébergée | Windows Blog du développeur"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "Qu’est-ce qu’un package classique ? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recommandations en matière d’image Windows PWA packages | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Étapes suivantes pour obtenir votre PWA dans la Microsoft Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publier une nouvelle application dans le Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Mettre à jour une application existante dans le Store | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
