---
description: Dernières fonctionnalités expérimentales de Microsoft Edge pour les applications web
title: Fonctionnalités expérimentales | Applications web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, expérimentation, applications web progressives, applications web, PWA
ms.openlocfilehash: 20bc4c90c1fe30be360b44294966415823f9b3a6
ms.sourcegitcommit: 4c6b74b9cdfca73c410d9eba9b42d229b695ee4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11482442"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="8bb01-104">Fonctionnalités expérimentales dans les applications web progressives (P.A.S.)</span><span class="sxs-lookup"><span data-stu-id="8bb01-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="8bb01-105">Microsoft Edge permet d'accéder aux fonctionnalités expérimentales qui sont toujours en développement.</span><span class="sxs-lookup"><span data-stu-id="8bb01-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="8bb01-106">Pour déterminer si chaque fonctionnalité est prête et quand publier chacune d'elles, testez [et fournissez des commentaires.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="8bb01-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="8bb01-107">Les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, mais les dernières fonctionnalités expérimentales sont disponibles uniquement dans le canal Canary de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="8bb01-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="8bb01-108">Turn on experimental features</span></span>  

<span data-ttu-id="8bb01-109">Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bb01-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="8bb01-110">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="8bb01-111">Veillez à utiliser une version de Microsoft Edge dont l'expérience est répertoriée dans cet article.</span><span class="sxs-lookup"><span data-stu-id="8bb01-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="8bb01-112">Accédez aux [fonctionnalités expérimentales.](#features-that-are-available-to-test)</span><span class="sxs-lookup"><span data-stu-id="8bb01-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="8bb01-113">Accédez `edge://flags` à .</span><span class="sxs-lookup"><span data-stu-id="8bb01-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="8bb01-114">Accédez à l'expérience pertinente.</span><span class="sxs-lookup"><span data-stu-id="8bb01-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="8bb01-115">Choisissez le menu déroulant en face de la description de l'expérience et choisissez `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Choose Enabled to turn on an experiment" lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="8bb01-117">Choose **Enabled** to turn on an experiment</span><span class="sxs-lookup"><span data-stu-id="8bb01-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="8bb01-118">Chaque expérience possède généralement un menu déroulant pour choisir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bb01-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="8bb01-119">Si une fonctionnalité expérimentale ne dispose pas d'une entrée dans **Expériences,** des instructions sont fournies pour démarrer Microsoft Edge avec cette fonctionnalité à l'aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8bb01-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="8bb01-120">Redémarrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="8bb01-121">Versions d’évaluation d’origine</span><span class="sxs-lookup"><span data-stu-id="8bb01-121">Origin Trials</span></span>  

<span data-ttu-id="8bb01-122">Microsoft Edge utilise parfois des essais d'origine pour tester des fonctionnalités pour des domaines ou des sites web spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8bb01-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="8bb01-123">Vous pouvez utiliser une version d'essai d'origine pour votre site web afin d'appliquer une fonctionnalité spécifique.</span><span class="sxs-lookup"><span data-stu-id="8bb01-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="8bb01-124">Si vous êtes propriétaire d'un site web, vous pouvez vous inscrire à une version d'essai d'origine.</span><span class="sxs-lookup"><span data-stu-id="8bb01-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="8bb01-125">Une version d'essai d'origine fournit des fonctionnalités à un pourcentage d'utilisateurs de Microsoft Edge qui visitent votre site web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="8bb01-126">Pour plus d'informations sur les essais d'origine, accédez à la console du développeur des essais [d'origine De Microsoft Edge.][MicrosoftDeveloperMicrosoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="8bb01-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="8bb01-127">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="8bb01-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="8bb01-128">Pour désactiver une fonctionnalité expérimentale, accédez à Activer [les](#turn-on-experimental-features)fonctionnalités expérimentales, accédez à l'expérience, puis choisissez `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="8bb01-129">Fonctionnalités disponibles pour le test</span><span class="sxs-lookup"><span data-stu-id="8bb01-129">Features that are available to test</span></span>  

<span data-ttu-id="8bb01-130">La liste suivante décrit les nouvelles fonctionnalités expérimentales d'application web disponibles pour le test et la validation sur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="8bb01-131">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8bb01-131">Feature</span></span> | <span data-ttu-id="8bb01-132">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bb01-132">Microsoft Edge version</span></span> | <span data-ttu-id="8bb01-133">Plateforme</span><span class="sxs-lookup"><span data-stu-id="8bb01-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="8bb01-134">Gestion du protocole URI</span><span class="sxs-lookup"><span data-stu-id="8bb01-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="8bb01-135">91 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bb01-135">91 or later</span></span> | <span data-ttu-id="8bb01-136">Windows</span><span class="sxs-lookup"><span data-stu-id="8bb01-136">Windows</span></span> |    
| [<span data-ttu-id="8bb01-137">Gestion des liens d'URL</span><span class="sxs-lookup"><span data-stu-id="8bb01-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="8bb01-138">91 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bb01-138">91 or later</span></span> | <span data-ttu-id="8bb01-139">Windows</span><span class="sxs-lookup"><span data-stu-id="8bb01-139">Windows</span></span>|
| [<span data-ttu-id="8bb01-140">Superposition des contrôles de fenêtre pour les applications de bureau</span><span class="sxs-lookup"><span data-stu-id="8bb01-140">Window Controls Overlay for Desktop Apps</span></span>](#window-controls-overlay-for-installed-desktop-web-apps) | <span data-ttu-id="8bb01-141">91 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bb01-141">91 or later</span></span> | <span data-ttu-id="8bb01-142">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8bb01-142">Windows 10</span></span>|   
| [<span data-ttu-id="8bb01-143">Exécuter sur la connexion au système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="8bb01-143">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="8bb01-144">88 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bb01-144">88 or later</span></span> | <span data-ttu-id="8bb01-145">Tous</span><span class="sxs-lookup"><span data-stu-id="8bb01-145">All</span></span> |  
| [<span data-ttu-id="8bb01-146">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="8bb01-146">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="8bb01-147">87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bb01-147">87 or later</span></span> | <span data-ttu-id="8bb01-148">Tous</span><span class="sxs-lookup"><span data-stu-id="8bb01-148">All</span></span> |  
| [<span data-ttu-id="8bb01-149">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="8bb01-149">File Handling</span></span>](#file-handling) | <span data-ttu-id="8bb01-150">83 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bb01-150">83 or later</span></span> | <span data-ttu-id="8bb01-151">Tous les ordinateurs de bureau</span><span class="sxs-lookup"><span data-stu-id="8bb01-151">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="8bb01-152">Gestion du protocole URI</span><span class="sxs-lookup"><span data-stu-id="8bb01-152">URI Protocol Handling</span></span>  

<span data-ttu-id="8bb01-153">Un identificateur de ressource uniforme \(URI\) peut être utilisé pour définir plus que des liens vers des pages web et du contenu web à l'aide du protocole HTTP ou FTP.</span><span class="sxs-lookup"><span data-stu-id="8bb01-153">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="8bb01-154">Les UR peuvent être utilisés pour décrire les liens vers tout ce que vous codifiez dans un schéma.</span><span class="sxs-lookup"><span data-stu-id="8bb01-154">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="8bb01-155">Par exemple, le protocole est utilisé pour décrire un lien de messagerie et le système d'exploitation \(OS\) ou le navigateur décide quelle page web ou application doit gérer `mailto://` ce protocole.</span><span class="sxs-lookup"><span data-stu-id="8bb01-155">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="8bb01-156">Pour plus d'informations sur la prise en charge existante basée sur le navigateur, accédez aux serveurs de protocole [web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]</span><span class="sxs-lookup"><span data-stu-id="8bb01-156">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="8bb01-157">Cette fonctionnalité vous permet d'effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bb01-157">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="8bb01-158">Inscrire votre PWA auprès du système d'exploitation hôte à l'aide du manifeste de votre application web</span><span class="sxs-lookup"><span data-stu-id="8bb01-158">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="8bb01-159">Déclarer qu'un PWA gère un protocole URI spécifique</span><span class="sxs-lookup"><span data-stu-id="8bb01-159">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="8bb01-160">Après avoir inscrit un PWA en tant que programme de traitement de protocole, lorsqu'un utilisateur choisit un lien hypertexte avec un schéma spécifique tel qu'un navigateur ou une application native, l'application PWA enregistrée est activée par le système d'exploitation et reçoit `mailto://` `web+music://` l'URI.</span><span class="sxs-lookup"><span data-stu-id="8bb01-160">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="8bb01-161">Cette fonctionnalité nécessite que vous mettez à jour le manifeste de l'application web pour inclure un tableau, dans le tableau, vous devez `protocol_handlers` spécifier deux champs :</span><span class="sxs-lookup"><span data-stu-id="8bb01-161">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="8bb01-162">: protocole de traitement de la demande, par exemple `mailto` ou `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-162">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="8bb01-163">: URI HTTPS dans l'étendue de l'application qui gère le protocole.</span><span class="sxs-lookup"><span data-stu-id="8bb01-163">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="8bb01-164">À l'avenir, l'URI commençant par le schéma de handlers de protocole est prévu pour remplacer le `%s` jeton.</span><span class="sxs-lookup"><span data-stu-id="8bb01-164">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="8bb01-165">Mettez à jour votre manifeste pour prendre en charge le protocole que vous souhaitez inscrire.</span><span class="sxs-lookup"><span data-stu-id="8bb01-165">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="8bb01-166">Une fois que vous avez mis en place cette fonctionnalité, Microsoft Edge termine les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bb01-166">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="8bb01-167">Détecte les modifications dans le manifeste</span><span class="sxs-lookup"><span data-stu-id="8bb01-167">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="8bb01-168">Enregistre l'application pour le protocole</span><span class="sxs-lookup"><span data-stu-id="8bb01-168">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="8bb01-169">Si plusieurs applications inscrivent un protocole, une invite s'est présentée à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8bb01-169">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="8bb01-170">L'utilisateur choisit l'application appropriée dans la liste présentée par le système d'exploitation ou le navigateur.</span><span class="sxs-lookup"><span data-stu-id="8bb01-170">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="8bb01-171">Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des protocoles dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et à activer la gestion du protocole **PWA de bureau.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-171">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA Protocol handling**.</span></span>  

<span data-ttu-id="8bb01-172">Pour plus d'informations sur l'essai d'origine est en cours d'exécution pour les responsables de protocole, accédez à [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span><span class="sxs-lookup"><span data-stu-id="8bb01-172">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="8bb01-173">Exemple de manifeste</span><span class="sxs-lookup"><span data-stu-id="8bb01-173">Example Manifest</span></span>

<span data-ttu-id="8bb01-174">Dans cet exemple, un manifeste d'application web déclare que l'application doit être enregistrée pour gérer les protocoles `web+jngl` et `web+jnglstore` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-174">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a><span data-ttu-id="8bb01-175">Gestion des liens d'URL</span><span class="sxs-lookup"><span data-stu-id="8bb01-175">URL Link Handling</span></span>  

<span data-ttu-id="8bb01-176">Un localisateur de ressources uniforme \(URL\) est un type d'URI.</span><span class="sxs-lookup"><span data-stu-id="8bb01-176">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="8bb01-177">Créez une expérience plus attrayante lorsque les applications web progressives \(PWAs\) s'inscrivent en tant que handleurs pour les URIs https.</span><span class="sxs-lookup"><span data-stu-id="8bb01-177">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="8bb01-178">Les URS associés peuvent demander à être lancés lorsque les URIs associés sont activés.</span><span class="sxs-lookup"><span data-stu-id="8bb01-178">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="8bb01-179">Par exemple, si un utilisateur choisit un lien vers un article d'actualités dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="8bb01-179">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="8bb01-180">Un PWA associé pour afficher des articles d'actualités est automatiquement lancé pour gérer l'activation du lien.</span><span class="sxs-lookup"><span data-stu-id="8bb01-180">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="8bb01-181">Cette fonctionnalité vous permet d'inscrire un PWA auprès du navigateur à l'aide du manifeste de l'application web et de déclarer que le navigateur gère des liens spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8bb01-181">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="8bb01-182">Pour inscrire un PWA avec le navigateur, ajoutez le `url_handlers` membre facultatif au fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="8bb01-182">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="8bb01-183">Le membre est un groupe qui groupe les origines des `url_handlers` `object[]` URIs que l'application souhaite gérer.</span><span class="sxs-lookup"><span data-stu-id="8bb01-183">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="8bb01-184">La gestion des liens est validée par le navigateur à l'aide d'un `web-app-origin-association` fichier JSON situé sur l'origine.</span><span class="sxs-lookup"><span data-stu-id="8bb01-184">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="8bb01-185">Le fichier d'origine affinera davantage les chemins d'accès inclus ou exclus à l'origine.</span><span class="sxs-lookup"><span data-stu-id="8bb01-185">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="8bb01-186">Pour obtenir des instructions détaillées sur le test du handler d'URL, accédez à [pwAs en tant que handleurs d'URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]</span><span class="sxs-lookup"><span data-stu-id="8bb01-186">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="8bb01-187">Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des liens d'URL dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et activer la gestion des **URL PWA de bureau.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-187">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL  Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="8bb01-188">Exemple de la url_handlers dans le manifeste</span><span class="sxs-lookup"><span data-stu-id="8bb01-188">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="8bb01-189">L'extrait de code suivant est un exemple de manifeste d'application web avec le `url_handlers` membre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-189">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

<span data-ttu-id="8bb01-190">Un PWA correspond à un URI pour la gestion des URL si l'URI correspond à l'une des chaînes d'origine dans et que le navigateur confirme que l'origine accepte d'autoriser cette application à gérer un tel `url_handlers` URI.</span><span class="sxs-lookup"><span data-stu-id="8bb01-190">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="8bb01-191">Le membre contient une origine qui englobe l'étendue et d'autres `url_handlers` origines non liées de l'application PWA à l'origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="8bb01-191">The `url_handlers` member contains an origin that encompasses the scope and other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="8bb01-192">Si vous ne limitez pas les URIs à la même étendue ou domaine que pWA à la demande, vous pouvez utiliser des noms de domaine différents pour le même contenu, mais les gérer avec le même PWA.</span><span class="sxs-lookup"><span data-stu-id="8bb01-192">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="8bb01-193">Correspondance de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="8bb01-193">Wildcard matching</span></span>  

<span data-ttu-id="8bb01-194">Utilisez le caractère générique \( `*` \) pour faire correspondre un ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="8bb01-194">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="8bb01-195">Un préfixe générique est utilisé dans les chaînes d'origine du membre à mettre en `url_handlers` correspondance pour différents sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="8bb01-195">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="8bb01-196">Le préfixe doit être `*.` pour cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="8bb01-196">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="8bb01-197">Le `https` schéma est supposé lorsque vous utilisez un préfixe générique.</span><span class="sxs-lookup"><span data-stu-id="8bb01-197">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="8bb01-198">Par exemple, la `url_handlers` valeur de membre est définie sur `*.contoso.com` correspondances et , mais ne `tenant.contoso.com` correspond pas `www.tenant.contoso.com` `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-198">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a><span data-ttu-id="8bb01-199">Superposition des contrôles de fenêtre pour les applications web de bureau installées</span><span class="sxs-lookup"><span data-stu-id="8bb01-199">Window Controls Overlay for installed desktop web apps</span></span>  

<span data-ttu-id="8bb01-200">Pour créer une barre de titre immersive comme une application native pour votre application web installée sur le bureau, la fonctionnalité Superposition des contrôles **de fenêtre** permet d'effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bb01-200">To create an immersive title bar like a native app for your desktop installed web app, the **Window Controls Overlay** feature completes the following actions.</span></span>  
    
1.  <span data-ttu-id="8bb01-201">Supprime la barre de titre réservée système.</span><span class="sxs-lookup"><span data-stu-id="8bb01-201">Removes the system reserved title bar.</span></span>  <span data-ttu-id="8bb01-202">Elle s'étend généralement sur la largeur du cadre client.</span><span class="sxs-lookup"><span data-stu-id="8bb01-202">It usually spans the width of the client frame.</span></span>  
1.  <span data-ttu-id="8bb01-203">La remplace par une superposition.</span><span class="sxs-lookup"><span data-stu-id="8bb01-203">Replaces it with an overlay.</span></span>  <span data-ttu-id="8bb01-204">Il contient uniquement les contrôles de fenêtre nécessaires au système critique nécessaires pour qu'un utilisateur contrôle la fenêtre elle-même.</span><span class="sxs-lookup"><span data-stu-id="8bb01-204">It contains just the critical system required window controls necessary for a user to control the window itself.</span></span>  
    
<span data-ttu-id="8bb01-205">Une fois qu'elle fournit une superposition, vous pouvez utiliser l'intégralité de la zone du client web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-205">After it provides an overlay, the entire web client area is available for you to use.</span></span>  <span data-ttu-id="8bb01-206">Cette fonctionnalité inclut une mise à jour du manifeste.</span><span class="sxs-lookup"><span data-stu-id="8bb01-206">This feature includes a manifest update.</span></span>  <span data-ttu-id="8bb01-207">Il vous permet de déterminer la taille et la position de la superposition pour vous aider à organiser le contenu.</span><span class="sxs-lookup"><span data-stu-id="8bb01-207">It provides ways for you to determine the size and position of the overlay to help you arrange content.</span></span>  

<span data-ttu-id="8bb01-208">Pour afficher un aperçu des superpositions de contrôles [](#turn-on-experimental-features) de fenêtre dans Microsoft Edge pour Windows 10, accédez à Activer les fonctionnalités expérimentales et accédez à Superposition des contrôles de fenêtre PWA de **bureau.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-208">To preview the Window Controls Overlays in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.</span></span>   

### <a name="examples-of-title-bar-area-customization"></a><span data-ttu-id="8bb01-209">Exemples de personnalisation de la zone de barre de titre</span><span class="sxs-lookup"><span data-stu-id="8bb01-209">Examples of title bar area customization</span></span>  

<span data-ttu-id="8bb01-210">Cette fonctionnalité est basée sur la possibilité dans les applications natives de personnaliser la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-210">This feature is based on the ability in native apps to customize the title bar.</span></span>  <span data-ttu-id="8bb01-211">Vous pouvez personnaliser une barre de titre pour les actions ou notifications d'application importantes.</span><span class="sxs-lookup"><span data-stu-id="8bb01-211">You may customize a title bar for important app actions or notifications.</span></span>  <span data-ttu-id="8bb01-212">Examinez les exemples suivants pour Microsoft Visual Studio Code et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8bb01-212">Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.</span></span>  

#### <a name="visual-studio-code"></a><span data-ttu-id="8bb01-213">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="8bb01-213">Visual Studio Code</span></span>  

<span data-ttu-id="8bb01-214">Microsoft Visual Studio Code est un éditeur populaire créé sur Le Monde et qui est intégré sur plusieurs plateformes de bureau.</span><span class="sxs-lookup"><span data-stu-id="8bb01-214">Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.</span></span>  

<span data-ttu-id="8bb01-215">L'exemple suivant montre comment Visual Studio Code utilise la barre de titre pour optimiser l'espace disponible à l'écran afin d'inclure le nom de fichier actuel et la structure de menu de niveau supérieur dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-215">The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.</span></span>  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Exemple de barre de titre dans Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   <span data-ttu-id="8bb01-217">Exemple de barre de titre dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="8bb01-217">An example of the title bar in Visual Studio Code</span></span>  
:::image-end:::  

#### <a name="microsoft-teams"></a><span data-ttu-id="8bb01-218">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8bb01-218">Microsoft Teams</span></span>  

<span data-ttu-id="8bb01-219">L'outil de collaboration et de communication de l'espace de travail Microsoft Teams est également créé avec Le Poste de travail et disponible sur plusieurs plateformes de bureau.</span><span class="sxs-lookup"><span data-stu-id="8bb01-219">Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.</span></span>  <span data-ttu-id="8bb01-220">Dans l'exemple suivant, Microsoft Teams affiche et les boutons de navigation, une zone de `back` `forward` recherche et les contrôles de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8bb01-220">In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.</span></span>  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Exemple de barre de titre dans Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   <span data-ttu-id="8bb01-222">Exemple de barre de titre dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8bb01-222">An example of the title bar in Microsoft Teams</span></span>  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a><span data-ttu-id="8bb01-223">Overlay Window Controls on a Frameless Window</span><span class="sxs-lookup"><span data-stu-id="8bb01-223">Overlay Window Controls on a Frameless Window</span></span>  

<span data-ttu-id="8bb01-224">Pour optimiser la zone adressaçable du contenu web, le navigateur crée une fenêtre sans cadre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-224">To maximize the addressable area for web content, the browser creates a frameless window.</span></span>  <span data-ttu-id="8bb01-225">Une fenêtre sans cadre supprime toutes les interfaces utilisateur du navigateur, à l'exception des contrôles de fenêtre fournis en tant que superposition.</span><span class="sxs-lookup"><span data-stu-id="8bb01-225">A frameless window removes all browser UI, except for the window controls provided as an overlay.</span></span>  <span data-ttu-id="8bb01-226">La fenêtre contrôle la superposition permet aux utilisateurs de réduire, d'optimiser, de restaurer et de fermer l'application.</span><span class="sxs-lookup"><span data-stu-id="8bb01-226">The window controls overlay allows users to still minimize, maximize, restore, and close the app.</span></span>  <span data-ttu-id="8bb01-227">Il permet également d'accéder aux contrôles de navigateur pertinents à l'aide du menu de l'application web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-227">It also provides access to relevant browser controls using the web app menu.</span></span>  <span data-ttu-id="8bb01-228">Pour les navigateurs basés sur Chromium, la superposition inclut les contrôles suivants.</span><span class="sxs-lookup"><span data-stu-id="8bb01-228">For Chromium-based browsers, the overlay includes the following controls.</span></span>  

*   <span data-ttu-id="8bb01-229">Zone draggable de la même largeur et hauteur de chacun des boutons de contrôle de fenêtre</span><span class="sxs-lookup"><span data-stu-id="8bb01-229">A draggable region the same width and height of each of the window control buttons</span></span>  
*   <span data-ttu-id="8bb01-230">Le **bouton Paramètres et plus** \(...\)</span><span class="sxs-lookup"><span data-stu-id="8bb01-230">The **Settings and more** \(...\) button</span></span>  
*   <span data-ttu-id="8bb01-231">Les boutons de contrôle de fenêtre réduisent, agrandissent, restaurent et ferment</span><span class="sxs-lookup"><span data-stu-id="8bb01-231">The window control buttons minimize, maximize, restore, and close</span></span>  
    
<span data-ttu-id="8bb01-232">Outre les contrôles répertoriés précédemment, l'interface utilisateur affichée dans la superposition est resserée dynamiquement dans les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="8bb01-232">Besides the previously listed controls, the UI displayed in the overlay is dynamically resized in the following scenarios.</span></span>  

*   <span data-ttu-id="8bb01-233">Lorsqu'une application web installée est lancée, l'origine de la page web s'affiche à gauche du menu Paramètres et plus \(...\) pendant quelques **secondes,** puis disparaît.</span><span class="sxs-lookup"><span data-stu-id="8bb01-233">When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.</span></span>  
*   <span data-ttu-id="8bb01-234">Si un utilisateur interagit avec une extension à l'aide du menu **Paramètres** et plus \(...\), l'icône de l'extension s'affiche dans la superposition à gauche du menu à trois points.</span><span class="sxs-lookup"><span data-stu-id="8bb01-234">If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.</span></span>  <span data-ttu-id="8bb01-235">Une fois que vous avez quitté une boîte de dialogue d'extension, l'icône est supprimée de la superposition.</span><span class="sxs-lookup"><span data-stu-id="8bb01-235">After you exit any extension dialog, the icon is removed from the overlay.</span></span>  
    
| <span data-ttu-id="8bb01-236">Sens de la langue</span><span class="sxs-lookup"><span data-stu-id="8bb01-236">Language direction</span></span> | <span data-ttu-id="8bb01-237">Emplacement de superposition</span><span class="sxs-lookup"><span data-stu-id="8bb01-237">Overlay location</span></span> | <span data-ttu-id="8bb01-238">Détails</span><span class="sxs-lookup"><span data-stu-id="8bb01-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8bb01-239">De gauche à droite \(LTR\)</span><span class="sxs-lookup"><span data-stu-id="8bb01-239">Left-to-right \(LTR\)</span></span> | <span data-ttu-id="8bb01-240">Partie supérieure gauche de la zone cliente</span><span class="sxs-lookup"><span data-stu-id="8bb01-240">Upper left of the client area</span></span> | <span data-ttu-id="8bb01-241">Les contrôles sont retournés</span><span class="sxs-lookup"><span data-stu-id="8bb01-241">The controls are flipped</span></span> |  
| <span data-ttu-id="8bb01-242">De droite à gauche \(RTL\)</span><span class="sxs-lookup"><span data-stu-id="8bb01-242">Right-to-left \(RTL\)</span></span> | <span data-ttu-id="8bb01-243">Coin supérieur droit de la zone cliente</span><span class="sxs-lookup"><span data-stu-id="8bb01-243">Upper right corner of the client area</span></span> |  |  

> [!IMPORTANT]
> <span data-ttu-id="8bb01-244">La superposition se trouve toujours au-dessus de l'index Z du contenu web et accepte toutes les entrées de l'utilisateur sans les faire passer au contenu web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-244">The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.</span></span>  

### <a name="working-around-the-window-controls-overlay"></a><span data-ttu-id="8bb01-245">Contourner la superposition des contrôles de fenêtre</span><span class="sxs-lookup"><span data-stu-id="8bb01-245">Working around the Window Controls Overlay</span></span>  

<span data-ttu-id="8bb01-246">Votre contenu web doit connaître la zone réservée pour la superposition des contrôles.</span><span class="sxs-lookup"><span data-stu-id="8bb01-246">Your web content must be aware of the reserved area for the controls overlay.</span></span>  <span data-ttu-id="8bb01-247">Assurez-vous que la zone réservée ne s'attend pas à une interaction de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8bb01-247">Ensure the reserved area doesn't expect user interaction.</span></span>  <span data-ttu-id="8bb01-248">Interrogez le navigateur pour le rectangle de limite et la visibilité de la superposition des contrôles.</span><span class="sxs-lookup"><span data-stu-id="8bb01-248">Query the browser for the bounding rectangle and visibility of the controls overlay.</span></span>  <span data-ttu-id="8bb01-249">Les informations vous sont fournies par le biais des API JavaScript et des variables d'environnement CSS.</span><span class="sxs-lookup"><span data-stu-id="8bb01-249">The information is provided to you through JavaScript APIs and CSS environment variables.</span></span>  

#### <a name="javascript-apis"></a><span data-ttu-id="8bb01-250">API JavaScript</span><span class="sxs-lookup"><span data-stu-id="8bb01-250">JavaScript APIs</span></span>  

<span data-ttu-id="8bb01-251">Un nouvel objet sur la propriété vous permet d'interroger le rectangle de `windowControlsOverlay` `window.navigator` limite des contrôles de superposition.</span><span class="sxs-lookup"><span data-stu-id="8bb01-251">A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.</span></span>  

<span data-ttu-id="8bb01-252">`windowControlsOverlay`L'objet possède les deux objets suivants.</span><span class="sxs-lookup"><span data-stu-id="8bb01-252">The `windowControlsOverlay` object has the following two objects.</span></span>  

*   `getBoundingClientRect()` <span data-ttu-id="8bb01-253">renvoie un `DOMRect` objet.</span><span class="sxs-lookup"><span data-stu-id="8bb01-253">returns a `DOMRect` object.</span></span>  <span data-ttu-id="8bb01-254">`DOMRect`L'objet représente la zone sous la superposition des contrôles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-254">The `DOMRect` object represents the area under the window controls overlay.</span></span>  
*   `visible` <span data-ttu-id="8bb01-255">est un booléen qui indique que la superposition des contrôles est affichée et affichée.</span><span class="sxs-lookup"><span data-stu-id="8bb01-255">is a boolean that indicates that the controls overlay is rendered and displayed.</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="8bb01-256">Pour des raisons de confidentialité, `windowControlsOverlay` l'élément n'est pas accessible aux `iframe` éléments du contenu web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-256">For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.</span></span>  

<span data-ttu-id="8bb01-257">Chaque fois que la superposition est recalculée, un événement s'exécute sur l'objet pour avertir le `geometrychange` `navigator.windowControlsOverlay` client de recalculer la disposition de contenu.</span><span class="sxs-lookup"><span data-stu-id="8bb01-257">Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.</span></span>  <span data-ttu-id="8bb01-258">La disposition de contenu recalculée est basée sur le nouveau rectangle de limite de la superposition.</span><span class="sxs-lookup"><span data-stu-id="8bb01-258">The recalculated content layout is based on the new bounding rectangle of the overlay.</span></span>  

#### <a name="css-environment-variables"></a><span data-ttu-id="8bb01-259">Variables d'environnement CSS</span><span class="sxs-lookup"><span data-stu-id="8bb01-259">CSS Environment Variables</span></span>  

<span data-ttu-id="8bb01-260">Outre l'API JavaScript, vous pouvez utiliser CSS pour interroger le rectangle de limite de la superposition des contrôles.</span><span class="sxs-lookup"><span data-stu-id="8bb01-260">Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.</span></span>  <span data-ttu-id="8bb01-261">Utilisez les quatre nouvelles variables d'environnement CSS suivantes pour effectuer une requête.</span><span class="sxs-lookup"><span data-stu-id="8bb01-261">Use the following four new CSS environment variables to accomplish to query.</span></span>  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a><span data-ttu-id="8bb01-262">Définir des régions draggables dans le contenu Web</span><span class="sxs-lookup"><span data-stu-id="8bb01-262">Define Draggable Regions in Web Content</span></span>  

<span data-ttu-id="8bb01-263">Les utilisateurs s'attendent à récupérer et faire glisser la zone supérieure d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-263">Users expect to grab and drag the upper region of a window.</span></span>  <span data-ttu-id="8bb01-264">Pour répondre aux attentes, déclarez des parties spécifiques du contenu web comme pouvant être draggables.</span><span class="sxs-lookup"><span data-stu-id="8bb01-264">To accommodate the expectation, declare specific parts of the web content as draggable.</span></span>  
<span data-ttu-id="8bb01-265">Pour spécifier qu'un élément peut être draggable, utilisez la propriété CSS propriétaire de `-webkit-app-region` WebKit.</span><span class="sxs-lookup"><span data-stu-id="8bb01-265">To specify an element is draggable, use the WebKit-proprietary `-webkit-app-region` CSS property.</span></span>  <span data-ttu-id="8bb01-266">Le groupe de travail CSS poursuit ses efforts pour normaliser la `app-region` propriété.</span><span class="sxs-lookup"><span data-stu-id="8bb01-266">The CSS working group continues efforts to standardize the `app-region` property.</span></span>  

### <a name="custom-title-bar-example"></a><span data-ttu-id="8bb01-267">Exemple de barre de titre personnalisée</span><span class="sxs-lookup"><span data-stu-id="8bb01-267">Custom title bar example</span></span>  

<span data-ttu-id="8bb01-268">L'exemple suivant montre comment les nouvelles fonctionnalités créent une application web avec une barre de titre personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8bb01-268">The following example displays how the new features create a web app with a custom title bar.</span></span>  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Exemple de barre de titre personnalisée dans Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   <span data-ttu-id="8bb01-270">Exemple de barre de titre personnalisée dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8bb01-270">Example of a custom title bar in Microsoft Teams</span></span>  
:::image-end:::  

#### <a name="manifestwebmanifest"></a><span data-ttu-id="8bb01-271">manifest.webmanifest</span><span class="sxs-lookup"><span data-stu-id="8bb01-271">manifest.webmanifest</span></span>  

<span data-ttu-id="8bb01-272">Dans le manifeste, définissez `display_override` le tableau sur  `window-controls-overlay` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-272">In the manifest, set `display_override` array to  `window-controls-overlay`.</span></span>  <span data-ttu-id="8bb01-273">Définissez `theme_color` la couleur de votre choix pour la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-273">Set the `theme_color` to your choice of color for the title bar.</span></span>  <span data-ttu-id="8bb01-274">Définissez le mode d'affichage sur un mode de retour approprié lorsque `display_override` `window-controls-overlay` l'un ou l'autre n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-274">Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.</span></span>  

<span data-ttu-id="8bb01-275">L'extrait de code suivant inclut les mises à jour de manifeste recommandées.</span><span class="sxs-lookup"><span data-stu-id="8bb01-275">The following code snippet includes the recommended manifest updates.</span></span>  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### <a name="indexhtml"></a><span data-ttu-id="8bb01-276">index.html</span><span class="sxs-lookup"><span data-stu-id="8bb01-276">index.html</span></span>  

<span data-ttu-id="8bb01-277">Les ID suivants représentent les deux principales régions de la page web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-277">The following IDs represent the two main regions of the webpage.</span></span>  

*   `titleBarContainer`  
*   `mainContent`  
    
<span data-ttu-id="8bb01-278">`div`L'élément avec `titleBar` l'ID est définie sur et l'élément enfant de la zone de recherche `draggable` est définie sur `input` `nonDraggable` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-278">The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.</span></span>  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

<span data-ttu-id="8bb01-279">Dans `div` l'élément avec `titleBarContainer` l'ID, l'ID représente la partie visible de la zone de `div` `titleBar` barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-279">In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.</span></span>  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a><span data-ttu-id="8bb01-280">style.css</span><span class="sxs-lookup"><span data-stu-id="8bb01-280">style.css</span></span>  

<span data-ttu-id="8bb01-281">Les régions draggables et non draggables sont définies à `-webkit-app-region: drag` l'aide et `-webkit-app-region: no-drag` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-281">The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.</span></span>  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

<span data-ttu-id="8bb01-282">Pour l'élément, les marges sont définies pour garantir que la barre de titre atteint les `body` `0` bords de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-282">For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.</span></span>  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

<span data-ttu-id="8bb01-283">L'ID utilise et définit le , qui joint le conteneur en `titleBarContainer` haut de la page `position: absolute` `top` `titlebar-area-inset-top` web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-283">The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.</span></span>  <span data-ttu-id="8bb01-284">Est `bottom` définie sur et revient à si la fenêtre contrôle la `titlebar-area-inset-bottom` `100% - var(--fallback-title-bar-height)` superposition n'est pas visible.</span><span class="sxs-lookup"><span data-stu-id="8bb01-284">The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.</span></span>  <span data-ttu-id="8bb01-285">La couleur d'arrière-plan `titleBarContainer` de l'ID est identique à la `theme_color` couleur .</span><span class="sxs-lookup"><span data-stu-id="8bb01-285">The background color of the `titleBarContainer` ID is the same as the `theme_color`.</span></span>  <span data-ttu-id="8bb01-286">La largeur est définie sur , de sorte que l'élément remplit la largeur de la page web et se trouve sous la superposition lorsqu'il est visible pour une `100%` `div` apparence contiguë.</span><span class="sxs-lookup"><span data-stu-id="8bb01-286">The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.</span></span>  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

<span data-ttu-id="8bb01-287">`titleBar`L'ID `position: absolute` l'utilise `top: titlebar-area-inset-top` également et l'attache en haut de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-287">The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.</span></span>  <span data-ttu-id="8bb01-288">Par défaut, il utilise toute la largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-288">By default, it consumes the full width of the window.</span></span>  <span data-ttu-id="8bb01-289">Les bords et les bords sont définies sur et, respectivement, reviennent au moment où les valeurs `left` `right` ne sont pas `titlebar-area-inset-left` `titlebar-area-inset-right` `0` définies.</span><span class="sxs-lookup"><span data-stu-id="8bb01-289">The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.</span></span>  <span data-ttu-id="8bb01-290">Il définit également pour empêcher toute tentative de faire glisser la fenêtre consommée à la place, il met en sur `user-select: none` évidence le texte dans l'élément. `div`</span><span class="sxs-lookup"><span data-stu-id="8bb01-290">It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.</span></span>  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

<span data-ttu-id="8bb01-291">Le conteneur de l'ID est également corrigé sur place et attaché `mainContent` au bas de la page `position: absolute` web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-291">The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.</span></span>  <span data-ttu-id="8bb01-292">La `height` propriété est définie sur et revient pour remplir `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` l'espace restant sous la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-292">The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.</span></span>  <span data-ttu-id="8bb01-293">Il définit `overflow-y: scroll` pour permettre au contenu de défiler verticalement dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="8bb01-293">It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.</span></span>  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

<span data-ttu-id="8bb01-294">Dans les cas où le navigateur ne prend pas en charge la superposition des contrôles de fenêtre, une variable CSS est ajoutée pour définir une hauteur par défaut pour la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8bb01-294">For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.</span></span>  <span data-ttu-id="8bb01-295">Les limites des ID et des ID sont initialement définies pour remplir l'intégralité de la zone cliente et vous n'avez pas besoin de la modifier si la superposition `titleBarContainer` `mainContent` n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-295">The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.</span></span>  

<span data-ttu-id="8bb01-296">L'extrait de code suivant inclut toutes les mises à jour CSS recommandées.</span><span class="sxs-lookup"><span data-stu-id="8bb01-296">The following code snippet includes all the recommended CSS updates.</span></span>

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  

## <a name="run-on-os-login"></a><span data-ttu-id="8bb01-297">Exécuter sur la connexion au système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="8bb01-297">Run On OS Login</span></span>  

<span data-ttu-id="8bb01-298">Cette fonctionnalité vous permet de configurer le lancement automatique de votre application lorsque l'utilisateur se connecte à Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8bb01-298">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="8bb01-299">Plusieurs classes d'applications tirez parti de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8bb01-299">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="8bb01-300">Les classes d'applications incluent la messagerie électronique, la conversation, le tableau de bord de surveillance et les applications d'affichage de données en temps réel.</span><span class="sxs-lookup"><span data-stu-id="8bb01-300">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="8bb01-301">Cette fonctionnalité permet à un utilisateur d'interagir avec les applications dès qu'il se connecte au système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="8bb01-301">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="8bb01-302">Cette fonctionnalité démarre automatiquement PWA de la même façon qu'elle est lancée manuellement.</span><span class="sxs-lookup"><span data-stu-id="8bb01-302">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8bb01-303">**L'exécuter sur la connexion au** système d'exploitation est une fonctionnalité [puissante.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="8bb01-303">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="8bb01-304">Les utilisateurs doivent décider d'activer ou non la fonctionnalité pour l'application web installée.</span><span class="sxs-lookup"><span data-stu-id="8bb01-304">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="8bb01-305">Activer l'ouverture de session du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="8bb01-305">Turn on Run On OS Login</span></span>  

<span data-ttu-id="8bb01-306">Pour afficher un aperçu des fonctionnalités de connexion [](#turn-on-experimental-features) au système d'exploitation **RunOn** pour votre PWA, accédez à Activer les fonctionnalités expérimentales et activer les applications de bureau PWA qui s'exécutent sur la connexion **au système d'exploitation.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-306">To preview the **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activer les applications de bureau de bureau s'exécutent sur l'expérience de connexion au système d'exploitation" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="8bb01-308">Activer les applications de bureau de bureau **s'exécutent sur l'expérience de connexion au système d'exploitation**</span><span class="sxs-lookup"><span data-stu-id="8bb01-308">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="8bb01-309">Activer la fonctionnalité pour l'application web installée</span><span class="sxs-lookup"><span data-stu-id="8bb01-309">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="8bb01-310">Pour activer la `Start app when you sign in` fonctionnalité pour un PWA installé,</span><span class="sxs-lookup"><span data-stu-id="8bb01-310">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="8bb01-311">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-311">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="8bb01-312">Accédez `edge://apps` à .</span><span class="sxs-lookup"><span data-stu-id="8bb01-312">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="8bb01-313">Pointez sur votre application.</span><span class="sxs-lookup"><span data-stu-id="8bb01-313">Hover on your app.</span></span>  
1.  <span data-ttu-id="8bb01-314">Ouvrez le menu contextuel \(clic droit\), puis choisissez **Démarrer l'application lorsque vous vous connectez.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-314">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Utiliser le menu contextuel pour activer l'application Démarrer lorsque vous vous connectez à la fonctionnalité dans Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="8bb01-316">Utiliser le menu contextuel pour activer **l'application Démarrer lorsque vous vous connectez** à la fonctionnalité dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8bb01-316">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="8bb01-317">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="8bb01-317">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="8bb01-318">est un nouveau membre du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="8bb01-318">is a new member of the manifest file.</span></span>  <span data-ttu-id="8bb01-319">Il vous permet de définir des liens vers des composants, des pages web clés ou des actions dans votre application web.</span><span class="sxs-lookup"><span data-stu-id="8bb01-319">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="8bb01-320">Microsoft Windows l'intègre en tant **que Jumplists**.</span><span class="sxs-lookup"><span data-stu-id="8bb01-320">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="8bb01-321">**Les listes de** choix définissent des menus contextuels qui s'affichent lorsque vous êtes sur l'un des éléments d'interface utilisateur suivants et ouvrent un menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="8bb01-321">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="8bb01-322">Une vignette dans le menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="8bb01-322">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="8bb01-323">Icône de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="8bb01-323">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="8bb01-324">Lorsqu'un utilisateur appelle un raccourci, il navigue jusqu'à l'adresse spécifiée par le membre `url` du raccourci.</span><span class="sxs-lookup"><span data-stu-id="8bb01-324">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Exemple de jumplists sur Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="8bb01-326">Exemple de **jumplists** sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="8bb01-326">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="8bb01-327">Raccourcis dans le fichier manifeste</span><span class="sxs-lookup"><span data-stu-id="8bb01-327">Shortcuts in the Manifest file</span></span>  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="8bb01-328">Propriétés des raccourcis</span><span class="sxs-lookup"><span data-stu-id="8bb01-328">Properties of shortcuts</span></span>  

<span data-ttu-id="8bb01-329">Les propriétés suivantes définissent chaque raccourci.</span><span class="sxs-lookup"><span data-stu-id="8bb01-329">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="8bb01-330">Propriété</span><span class="sxs-lookup"><span data-stu-id="8bb01-330">Property</span></span> | <span data-ttu-id="8bb01-331">Détails</span><span class="sxs-lookup"><span data-stu-id="8bb01-331">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="8bb01-332">Chaîne qui s'affiche pour l'utilisateur dans **jumplists** ou le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="8bb01-332">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="8bb01-333">Chaîne qui s'affiche lorsque l'espace est insuffisant pour afficher le nom complet du raccourci.</span><span class="sxs-lookup"><span data-stu-id="8bb01-333">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="8bb01-334">Chaîne qui décrit l'objectif du raccourci.</span><span class="sxs-lookup"><span data-stu-id="8bb01-334">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="8bb01-335">Il est possible d'y accéder par la technologie d'assistance.</span><span class="sxs-lookup"><span data-stu-id="8bb01-335">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="8bb01-336">URI dans l'application web qui s'ouvre lorsque le raccourci est activé.</span><span class="sxs-lookup"><span data-stu-id="8bb01-336">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="8bb01-337">Ensemble d'icônes qui représente le raccourci.</span><span class="sxs-lookup"><span data-stu-id="8bb01-337">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="8bb01-338">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="8bb01-338">File Handling</span></span>  

<span data-ttu-id="8bb01-339">La possibilité de s'inscrire en tant que handler de type de fichier est dans la phase d'expérimentation.</span><span class="sxs-lookup"><span data-stu-id="8bb01-339">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="8bb01-340">Vous pouvez spécifier les types de fichiers gérés par votre application dans une entrée de manifeste.</span><span class="sxs-lookup"><span data-stu-id="8bb01-340">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="8bb01-341">Lors de l'installation, le système d'exploitation hôte de l'utilisateur inscrit votre application en tant que handleur de fichiers pour les types de fichiers répertoriés.</span><span class="sxs-lookup"><span data-stu-id="8bb01-341">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="8bb01-342">Assurez-vous que la fonctionnalité existe dans le code de démarrage de vos applications et `launchQueue` qu'elle gère le fichier.</span><span class="sxs-lookup"><span data-stu-id="8bb01-342">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="8bb01-343">Les navigateurs basés sur Chromium testent et façonnent cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8bb01-343">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="8bb01-344">Pour plus d'informations, y compris des exemples de code, accédez à [Let web applications be file handlers][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="8bb01-344">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="8bb01-345">Pour afficher un aperçu de la gestion des [](#turn-on-experimental-features) fichiers dans Microsoft Edge pour Windows 10, accédez à Activer les fonctionnalités expérimentales et activer l'API de **gestion de fichiers.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-345">To preview file handling in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="8bb01-346">Commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="8bb01-346">Providing feedback on experimental features</span></span>  

<span data-ttu-id="8bb01-347">Pour fournir des commentaires sur les expériences d'application web Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8bb01-347">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="8bb01-348">Envoyez vos commentaires à **l'aide de Paramètres et** plus \( `...` \) > **envoyer des commentaires à Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="8bb01-348">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="8bb01-349">Sélectionnez `Alt` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="8bb01-349">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Envoyer des commentaires à partir de votre PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="8bb01-351">Envoyer des commentaires à partir de votre PWA</span><span class="sxs-lookup"><span data-stu-id="8bb01-351">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Essai d'origine | Développeur Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "S'inscrire à l'enregistrement du | Développeur Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Les | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Fonctionnalité puissante : autorisations | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs en tant que | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Que les applications web soient des | web.dev"  
