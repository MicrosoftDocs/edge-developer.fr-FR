---
ms.assetid: ''
description: Expérimentez en toute sécurité un laps de temps fixe et envoyez des commentaires sur les nouvelles fonctionnalités de la plateforme.
title: Premières versions d’essai
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, html, CSS, essais d’origine, développeur
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846525"
---
# <span data-ttu-id="44c51-104">Utiliser des essais d’origine dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="44c51-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="44c51-105">Les développeurs peuvent utiliser des essais d’origine pour tester des API expérimentales sur les sites dynamiques pendant une durée limitée.</span><span class="sxs-lookup"><span data-stu-id="44c51-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="44c51-106">Lorsque vous utilisez des versions d’évaluation, les utilisateurs de Microsoft Edge qui accèdent à votre site peuvent exécuter du code qui utilise des API expérimentales.</span><span class="sxs-lookup"><span data-stu-id="44c51-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="44c51-107">Pour accéder aux API expérimentales de chaque ordinateur utilisateur, vous n’avez pas besoin d' `edge://flags` activer ou de désactiver les indicateurs de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="44c51-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="44c51-108">Pour plus d’informations, reportez-vous à la rubrique [API expérimentales][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="44c51-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="44c51-109">De plus, vous pouvez fournir des commentaires sur la conception de l’API, de vos cas d’utilisation ou de votre utilisation de l’API aux ingénieurs du navigateur et à la communauté Web standard.</span><span class="sxs-lookup"><span data-stu-id="44c51-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <span data-ttu-id="44c51-110">Commencer à utiliser les essais d’origine</span><span class="sxs-lookup"><span data-stu-id="44c51-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="44c51-111">Pour plus d’informations sur les API expérimentales disponibles dans Microsoft Edge, consultez la rubrique [Microsoft Edge Origin expérimentation console][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="44c51-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="44c51-112">Veillez à consulter la configuration minimale requise pour la version de Microsoft Edge et la date de fin de la période d’évaluation pour vérifier que vous utilisez les API expérimentales sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="44c51-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="44c51-113">Une expérience risque de terminer plus tôt que prévu si l’une des situations suivantes se produit.</span><span class="sxs-lookup"><span data-stu-id="44c51-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="44c51-114">Un incident de sécurité majeur.</span><span class="sxs-lookup"><span data-stu-id="44c51-114">A major security incident.</span></span>  
> *   <span data-ttu-id="44c51-115">Si des commentaires suffisants sont collectés et indiquent qu’une nouvelle conception est nécessaire pour répondre aux besoins des développeurs Web.</span><span class="sxs-lookup"><span data-stu-id="44c51-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="44c51-116">Dans les deux cas, un message électronique de notification est envoyé à tous les développeurs actuellement inscrits au cours de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="44c51-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <span data-ttu-id="44c51-117">S’inscrire à une version d’évaluation d’une API expérimentale</span><span class="sxs-lookup"><span data-stu-id="44c51-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="44c51-118">Procédez comme suit pour vous inscrire à une version d’évaluation d’une API expérimentale.</span><span class="sxs-lookup"><span data-stu-id="44c51-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="44c51-119">Rendez-vous sur la page des [essais d’origine Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="44c51-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="44c51-120">Cliquez sur le bouton de Registre dans les expériences disponibles.</span><span class="sxs-lookup"><span data-stu-id="44c51-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="44c51-121">Connectez-vous à la console du développeur en utilisant votre nom d’utilisateur et votre mot de passe GitHub.</span><span class="sxs-lookup"><span data-stu-id="44c51-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="44c51-122">Sélectionnez **autoriser MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="44c51-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="44c51-123">Remplissez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="44c51-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="44c51-124">Pour inscrire un ou plusieurs sous-domaines, sélectionnez définir le `Do you need to match all subdomains for the provided origin?` paramètre sur `Yes` .</span><span class="sxs-lookup"><span data-stu-id="44c51-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="44c51-125">Par exemple, `https://dev.contoso.com` est un domaine unique et `https://*.contoso.com` utilise un caractère générique pour représenter tous les sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="44c51-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="44c51-126">Les formats d’origine suivants ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="44c51-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="44c51-127">Spécifiant un sous-dossier dans l’origine.</span><span class="sxs-lookup"><span data-stu-id="44c51-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="44c51-128">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="44c51-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="44c51-129">Utilisation d’une Origin avec des paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="44c51-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="44c51-130">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="44c51-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="44c51-131">Sélectionnez **accepter et inscrivez**.</span><span class="sxs-lookup"><span data-stu-id="44c51-131">Choose **ACCEPT and REGISTER**.</span></span>  

### <span data-ttu-id="44c51-132">Appliquer votre jeton</span><span class="sxs-lookup"><span data-stu-id="44c51-132">Apply your token</span></span>  

<span data-ttu-id="44c51-133">Un jeton est généré instantanément et affiché dans la page de la [console développeurs essais d’origine Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="44c51-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="44c51-134">Pour commencer à utiliser la version d’évaluation de votre site Web, appliquez l’une des méthodes suivantes pour appliquer le jeton à votre page.</span><span class="sxs-lookup"><span data-stu-id="44c51-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="44c51-135">Ajoutez la `origin-trial` valeur d’attribut et votre jeton à la `meta` balise sur chaque page qui utilise l’API expérimentale.</span><span class="sxs-lookup"><span data-stu-id="44c51-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="44c51-136">Ajoutez `Origin-Trial` l’en-tête de réponse http de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="44c51-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="44c51-137">Votre jeton est valide pour 6 semaines.</span><span class="sxs-lookup"><span data-stu-id="44c51-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="44c51-138">Avant la fin de la période d’évaluation, vous recevez des messages de rappel qui vous demandent vos commentaires et vous invite à envisager le renouvellement de votre version d’évaluation avant l’expiration de votre jeton.</span><span class="sxs-lookup"><span data-stu-id="44c51-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <span data-ttu-id="44c51-139">Désactiver une expérience</span><span class="sxs-lookup"><span data-stu-id="44c51-139">Opt out of an experiment</span></span>  

<span data-ttu-id="44c51-140">Pour désactiver une expérience, utilisez l’une des méthodes suivantes pour supprimer votre jeton.</span><span class="sxs-lookup"><span data-stu-id="44c51-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="44c51-141">Supprimez la `meta` balise de chaque page qui a utilisé l’API expérimentale.</span><span class="sxs-lookup"><span data-stu-id="44c51-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="44c51-142">Supprimer `Origin-Trial` de l’en-tête de réponse http de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="44c51-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <span data-ttu-id="44c51-143">Détecter les fonctionnalités expérimentales et fournir une reprise</span><span class="sxs-lookup"><span data-stu-id="44c51-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="44c51-144">Lorsque vous utilisez des API expérimentales, assurez-vous de fournir une expérience d’utilisation à tous les visiteurs de votre site Web.</span><span class="sxs-lookup"><span data-stu-id="44c51-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="44c51-145">Les visiteurs ne pourront pas utiliser les navigateurs qui ne prennent pas en charge les API expérimentales que vous avez ajoutées à votre code.</span><span class="sxs-lookup"><span data-stu-id="44c51-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="44c51-146">De plus, si votre jeton expire avant de le renouveler, l’API expérimentale n’est plus disponible, ce qui peut entraîner des erreurs.</span><span class="sxs-lookup"><span data-stu-id="44c51-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="44c51-147">Pour éviter ce problème, assurez-vous de détecter les fonctionnalités disponibles dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="44c51-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="44c51-148">Pour plus d’informations, reportez-vous à implémentation de la [détection de fonctionnalités][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="44c51-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <span data-ttu-id="44c51-149">Introduction aux origines autorisées</span><span class="sxs-lookup"><span data-stu-id="44c51-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="44c51-150">Le portail essais d’origine Microsoft Edge ne prend en charge que les origines SSL, ce qui signifie que les sites Web doivent être implémentés de manière appropriée pour s’inscrire à une expérience.</span><span class="sxs-lookup"><span data-stu-id="44c51-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="44c51-151">À l’avenir, les origines sécurisées suivantes sont planifiées.</span><span class="sxs-lookup"><span data-stu-id="44c51-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="44c51-152">Enregistrez-vous `http://localhost` comme origine de vos expériences.</span><span class="sxs-lookup"><span data-stu-id="44c51-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="44c51-153">Pour utiliser `http://localhost` la version actuelle, accédez à, `edge://flags` puis définissez l’expérience sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="44c51-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="44c51-154">Utiliser des extensions avec des `extensions://` origines prédéfinies pour s’inscrire à des expériences.</span><span class="sxs-lookup"><span data-stu-id="44c51-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin-version d’évaluation console de développement | Documents Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Mise en œuvre de la détection de fonctionnalités | MDN"  
