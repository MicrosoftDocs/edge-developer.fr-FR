---
ms.assetid: ''
description: Testez en toute sécurité pendant une période fixe et fournissez des commentaires sur les nouvelles fonctionnalités de la plateforme.
title: Versions d’évaluation d’origine
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, essais d’origine, développeur
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397544"
---
# <a name="use-origin-trials-in-microsoft-edge"></a><span data-ttu-id="e7ba9-104">Utiliser les essais d’origine Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e7ba9-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="e7ba9-105">Les développeurs peuvent utiliser les essais origin pour tester des API expérimentales sur des sites en direct pendant une période limitée.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="e7ba9-106">Lors de l’utilisation des essais originaux, les Microsoft Edge qui visitent votre site peuvent exécuter du code qui utilise des API expérimentales.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="e7ba9-107">Pour accéder aux API expérimentales sur chaque ordinateur utilisateur, vous n’avez pas besoin d’activer et d’activer les `edge://flags` indicateurs de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="e7ba9-108">Pour plus d’informations, accédez [aux API expérimentales.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-108">For more information, navigate to [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="e7ba9-109">En outre, vous pouvez fournir des commentaires sur la conception de l’API, vos cas d’utilisation ou votre expérience d’utilisation des API aux ingénieurs de navigateur et à la communauté web standard.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <a name="get-started-using-origin-trials"></a><span data-ttu-id="e7ba9-110">Commencer à utiliser les essais origin</span><span class="sxs-lookup"><span data-stu-id="e7ba9-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="e7ba9-111">Pour plus d’informations sur les API expérimentales disponibles dans Microsoft Edge, accédez à Microsoft Edge Console du développeur des essais [Origin.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-111">For more information about the experimental APIs available in Microsoft Edge, navigate to [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="e7ba9-112">Veillez à passer en revue la version minimale requise pour Microsoft Edge et la date de fin de la version d’évaluation pour évaluer la pertinence de l’utilisation des API expérimentales sur votre site web.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="e7ba9-113">Une expérience peut se terminer plus tôt que prévu si l’une des situations suivantes se produit.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="e7ba9-114">Incident de sécurité majeur.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-114">A major security incident.</span></span>  
> *   <span data-ttu-id="e7ba9-115">Si des commentaires suffisants sont collectés, cela indique qu’une nouvelle conception majeure est nécessaire pour répondre aux besoins des développeurs web.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="e7ba9-116">Dans les deux cas, un e-mail de notification est envoyé à tous les développeurs actuellement inscrits à l’expérience.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <a name="register-for-a-trial-of-an-experimental-api"></a><span data-ttu-id="e7ba9-117">S’inscrire à une version d’essai d’une API expérimentale</span><span class="sxs-lookup"><span data-stu-id="e7ba9-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="e7ba9-118">Utilisez les étapes suivantes pour vous inscrire à une version d’essai d’une API expérimentale.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="e7ba9-119">Visitez la page Microsoft Edge console du développeur [des essais Origin.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="e7ba9-120">Sélectionnez le bouton Enregistrer sur l’une des expériences disponibles.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="e7ba9-121">Connectez-vous à la console du développeur à l’aide GitHub nom d’utilisateur et mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="e7ba9-122">Choose **Authorize MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="e7ba9-123">Remplissez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e7ba9-124">Pour inscrire un ou tous les sous-domaine, choisissez de définir `Do you need to match all subdomains for the provided origin?` le paramètre sur `Yes` .</span><span class="sxs-lookup"><span data-stu-id="e7ba9-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="e7ba9-125">Par exemple, `https://dev.contoso.com` est un domaine unique et utilise un caractère générique pour représenter tous les `https://*.contoso.com` sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="e7ba9-126">Les formats d’origine suivants ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="e7ba9-127">Spécification d’un sous-foldeur sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="e7ba9-128">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7ba9-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="e7ba9-129">Utilisation d’une origine avec des paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="e7ba9-130">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7ba9-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="e7ba9-131">Choose **ACCEPT and REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-131">Choose **ACCEPT and REGISTER**.</span></span>  
    
### <a name="apply-your-token"></a><span data-ttu-id="e7ba9-132">Appliquer votre jeton</span><span class="sxs-lookup"><span data-stu-id="e7ba9-132">Apply your token</span></span>  

<span data-ttu-id="e7ba9-133">Un jeton est généré instantanément et affiché sur la page Microsoft Edge console du développeur des essais [Origin.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="e7ba9-134">Pour commencer à utiliser la version d’essai sur votre site web, utilisez l’une des méthodes suivantes pour appliquer le jeton à votre page.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="e7ba9-135">Ajoutez `origin-trial` la valeur d’attribut et votre jeton à la `meta` balise sur chaque page qui utilise l’API expérimentale.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="e7ba9-136">`Origin-Trial`Ajoutez-le à l’en-tête de réponse HTTP de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="e7ba9-137">Votre jeton est valide pendant 6 semaines.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="e7ba9-138">Avant la fin de votre version d’évaluation, des e-mails de rappel vous sont envoyés pour vous demander vos commentaires et vous demander de renouveler votre version d’évaluation avant l’expiration de votre jeton.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <a name="opt-out-of-an-experiment"></a><span data-ttu-id="e7ba9-139">Refuser une expérience</span><span class="sxs-lookup"><span data-stu-id="e7ba9-139">Opt out of an experiment</span></span>  

<span data-ttu-id="e7ba9-140">Pour refuser une expérience, utilisez l’une des méthodes suivantes pour supprimer votre jeton.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="e7ba9-141">Supprimez la `meta` balise de chaque page qui utilisait l’API expérimentale.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="e7ba9-142">Supprimez `Origin-Trial` de l’en-tête de réponse HTTP de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a><span data-ttu-id="e7ba9-143">Détecter les fonctionnalités expérimentales et fournir un modèle de retour</span><span class="sxs-lookup"><span data-stu-id="e7ba9-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="e7ba9-144">Lorsque vous utilisez des API expérimentales, veillez à fournir une expérience de travail à tous les visiteurs de votre site web.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="e7ba9-145">Les visiteurs peuvent utiliser des navigateurs qui ne peuvent pas prendre en charge les API expérimentales que vous avez ajoutées à votre code.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="e7ba9-146">En outre, si votre jeton expire avant de le renouveler, l’API expérimentale n’est plus disponible, ce qui peut entraîner des erreurs.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="e7ba9-147">Pour éviter cette situation, veillez à détecter les fonctionnalités disponibles dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="e7ba9-148">Pour plus d’informations, accédez à [Implémenter la détection des fonctionnalités.][MDNImplementingFeatureDetection]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-148">For more information, navigate to [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <a name="roadmap-for-allowed-origins"></a><span data-ttu-id="e7ba9-149">Feuille de route pour les origines autorisées</span><span class="sxs-lookup"><span data-stu-id="e7ba9-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="e7ba9-150">Le Microsoft Edge d’essai Origin aujourd’hui prend uniquement en charge les origines activées SSL, ce qui signifie que le protocole HTTPS doit être correctement implémenté sur les sites web pour s’inscrire à une expérience.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="e7ba9-151">À l’avenir, les origines sécurisées suivantes sont planifiées.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="e7ba9-152">`http://localhost`Inscrivez-vous comme origine de vos expériences.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="e7ba9-153">Pour utiliser `http://localhost` aujourd’hui, `edge://flags` accédez à l’expérience et définissez-la **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="e7ba9-153">To use `http://localhost` today, navigate to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="e7ba9-154">Utilisez des extensions avec `extensions://` des origines préfixées pour vous inscrire à des expériences.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Console de développement Origin Trials | Documents Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Mise en œuvre des fonctionnalités de détection | MDN"  
