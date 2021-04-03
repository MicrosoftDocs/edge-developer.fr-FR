---
description: Dernières fonctionnalités expérimentales de Microsoft Edge pour les applications web
title: Fonctionnalités expérimentales | Applications web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, expérimentation, applications web progressives, applications web, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474961"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="db967-104">Fonctionnalités expérimentales dans les applications web progressives (P.A.S.)</span><span class="sxs-lookup"><span data-stu-id="db967-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="db967-105">Microsoft Edge permet d’accéder aux fonctionnalités expérimentales qui sont toujours en développement.</span><span class="sxs-lookup"><span data-stu-id="db967-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="db967-106">Pour déterminer si chaque fonctionnalité est prête et quand publier chacune d’elles, testez [et fournissez des commentaires.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="db967-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="db967-107">Les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, mais les dernières fonctionnalités expérimentales sont disponibles uniquement dans le canal Canary de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db967-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="db967-108">Activer les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="db967-108">Turn on experimental features</span></span>  

<span data-ttu-id="db967-109">Pour activer \(ou désactiver\) les fonctionnalités expérimentales dans Microsoft Edge, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="db967-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="db967-110">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="db967-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="db967-111">Veillez à utiliser une version de Microsoft Edge dont l’expérience est répertoriée dans cet article.</span><span class="sxs-lookup"><span data-stu-id="db967-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="db967-112">Accédez aux [fonctionnalités expérimentales.](#features-that-are-available-to-test)</span><span class="sxs-lookup"><span data-stu-id="db967-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="db967-113">Accédez `edge://flags` à .</span><span class="sxs-lookup"><span data-stu-id="db967-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="db967-114">Accédez à l’expérience pertinente.</span><span class="sxs-lookup"><span data-stu-id="db967-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="db967-115">Choisissez le menu déroulant en face de la description de l’expérience et choisissez `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="db967-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Choose Enabled to turn on an experiment" lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="db967-117">Choose **Enabled** to turn on an experiment</span><span class="sxs-lookup"><span data-stu-id="db967-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="db967-118">Chaque expérience possède généralement un menu déroulant pour choisir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="db967-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="db967-119">Si une fonctionnalité expérimentale ne dispose pas d’une entrée dans **Expériences,** des instructions sont fournies pour démarrer Microsoft Edge avec cette fonctionnalité à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="db967-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="db967-120">Redémarrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="db967-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="db967-121">Versions d’évaluation d’origine</span><span class="sxs-lookup"><span data-stu-id="db967-121">Origin Trials</span></span>  

<span data-ttu-id="db967-122">Microsoft Edge utilise parfois des essais d’origine pour tester des fonctionnalités pour des domaines ou des sites web spécifiques.</span><span class="sxs-lookup"><span data-stu-id="db967-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="db967-123">Vous pouvez utiliser une version d’essai d’origine pour votre site web afin d’appliquer une fonctionnalité spécifique.</span><span class="sxs-lookup"><span data-stu-id="db967-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="db967-124">Si vous êtes propriétaire d’un site web, vous pouvez vous inscrire à une version d’essai d’origine.</span><span class="sxs-lookup"><span data-stu-id="db967-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="db967-125">Une version d’essai d’origine fournit des fonctionnalités à un pourcentage d’utilisateurs de Microsoft Edge qui visitent votre site web.</span><span class="sxs-lookup"><span data-stu-id="db967-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="db967-126">Pour plus d’informations sur les essais d’origine, accédez à la console du développeur des essais [d’origine De Microsoft Edge.][MicrosoftDeveloperMicrosoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="db967-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="db967-127">Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="db967-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="db967-128">Pour désactiver une fonctionnalité expérimentale, accédez à Activer [les](#turn-on-experimental-features)fonctionnalités expérimentales, accédez à l’expérience, puis choisissez `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="db967-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="db967-129">Fonctionnalités disponibles pour le test</span><span class="sxs-lookup"><span data-stu-id="db967-129">Features that are available to test</span></span>  

<span data-ttu-id="db967-130">La liste suivante décrit les nouvelles fonctionnalités expérimentales d’application web disponibles pour le test et la validation sur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db967-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="db967-131">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="db967-131">Feature</span></span> | <span data-ttu-id="db967-132">Version de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db967-132">Microsoft Edge version</span></span> | <span data-ttu-id="db967-133">Plateforme</span><span class="sxs-lookup"><span data-stu-id="db967-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="db967-134">Gestion du protocole URI</span><span class="sxs-lookup"><span data-stu-id="db967-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="db967-135">91 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="db967-135">91 or later</span></span> | <span data-ttu-id="db967-136">Windows</span><span class="sxs-lookup"><span data-stu-id="db967-136">Windows</span></span> |    
| [<span data-ttu-id="db967-137">Gestion des liens d’URL</span><span class="sxs-lookup"><span data-stu-id="db967-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="db967-138">91 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="db967-138">91 or later</span></span> | <span data-ttu-id="db967-139">Windows</span><span class="sxs-lookup"><span data-stu-id="db967-139">Windows</span></span>|  
| [<span data-ttu-id="db967-140">Exécuter sur la connexion au système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="db967-140">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="db967-141">88 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="db967-141">88 or later</span></span> | <span data-ttu-id="db967-142">Tous</span><span class="sxs-lookup"><span data-stu-id="db967-142">All</span></span> |  
| [<span data-ttu-id="db967-143">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="db967-143">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="db967-144">87 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="db967-144">87 or later</span></span> | <span data-ttu-id="db967-145">Tous</span><span class="sxs-lookup"><span data-stu-id="db967-145">All</span></span> |  
| [<span data-ttu-id="db967-146">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="db967-146">File Handling</span></span>](#file-handling) | <span data-ttu-id="db967-147">83 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="db967-147">83 or later</span></span> | <span data-ttu-id="db967-148">Tous les ordinateurs de bureau</span><span class="sxs-lookup"><span data-stu-id="db967-148">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="db967-149">Gestion du protocole URI</span><span class="sxs-lookup"><span data-stu-id="db967-149">URI Protocol Handling</span></span>  

<span data-ttu-id="db967-150">Un identificateur de ressource uniforme \(URI\) peut être utilisé pour définir plus que des liens vers des pages web et du contenu web à l’aide du protocole HTTP ou FTP.</span><span class="sxs-lookup"><span data-stu-id="db967-150">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="db967-151">Les UR peuvent être utilisés pour décrire les liens vers tout ce que vous codifiez dans un schéma.</span><span class="sxs-lookup"><span data-stu-id="db967-151">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="db967-152">Par exemple, le protocole est utilisé pour décrire un lien de messagerie et le système d’exploitation \(OS\) ou le navigateur décide quelle page web ou application doit gérer `mailto://` ce protocole.</span><span class="sxs-lookup"><span data-stu-id="db967-152">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="db967-153">Pour plus d’informations sur la prise en charge existante basée sur le navigateur, accédez aux serveurs de protocole [web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]</span><span class="sxs-lookup"><span data-stu-id="db967-153">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="db967-154">Cette fonctionnalité vous permet d’effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="db967-154">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="db967-155">Inscrire votre PWA auprès du système d’exploitation hôte à l’aide du manifeste de votre application web</span><span class="sxs-lookup"><span data-stu-id="db967-155">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="db967-156">Déclarer qu’un PWA gère un protocole URI spécifique</span><span class="sxs-lookup"><span data-stu-id="db967-156">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="db967-157">Après avoir inscrit un PWA en tant que programme de traitement de protocole, lorsqu’un utilisateur choisit un lien hypertexte avec un schéma spécifique tel qu’un navigateur ou une application native, l’application PWA enregistrée est activée par le système d’exploitation et reçoit `mailto://` `web+music://` l’URI.</span><span class="sxs-lookup"><span data-stu-id="db967-157">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="db967-158">Cette fonctionnalité nécessite que vous mettez à jour le manifeste de l’application web pour inclure un tableau, dans le tableau, vous devez `protocol_handlers` spécifier deux champs :</span><span class="sxs-lookup"><span data-stu-id="db967-158">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="db967-159">: protocole de traitement de la demande, par exemple `mailto` ou `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="db967-159">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="db967-160">: URI HTTPS dans l’étendue de l’application qui gère le protocole.</span><span class="sxs-lookup"><span data-stu-id="db967-160">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="db967-161">À l’avenir, l’URI commençant par le schéma de handlers de protocole est prévu pour remplacer le `%s` jeton.</span><span class="sxs-lookup"><span data-stu-id="db967-161">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="db967-162">Mettez à jour votre manifeste pour prendre en charge le protocole que vous souhaitez inscrire.</span><span class="sxs-lookup"><span data-stu-id="db967-162">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="db967-163">Une fois que vous avez mis en place cette fonctionnalité, Microsoft Edge termine les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="db967-163">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="db967-164">Détecte les modifications dans le manifeste</span><span class="sxs-lookup"><span data-stu-id="db967-164">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="db967-165">Enregistre l’application pour le protocole</span><span class="sxs-lookup"><span data-stu-id="db967-165">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="db967-166">Si plusieurs applications inscrivent un protocole, une invite s’est présentée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db967-166">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="db967-167">L’utilisateur choisit l’application appropriée dans la liste présentée par le système d’exploitation ou le navigateur.</span><span class="sxs-lookup"><span data-stu-id="db967-167">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="db967-168">Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des protocoles dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et à activer desktop **Web Apps support Protocol Handlers**.</span><span class="sxs-lookup"><span data-stu-id="db967-168">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop Web Apps support Protocol Handlers**.</span></span>  

<span data-ttu-id="db967-169">Pour plus d’informations sur l’essai d’origine est en cours d’exécution pour les responsables de protocole, accédez à [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span><span class="sxs-lookup"><span data-stu-id="db967-169">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="db967-170">Exemple de manifeste</span><span class="sxs-lookup"><span data-stu-id="db967-170">Example Manifest</span></span>

<span data-ttu-id="db967-171">Dans cet exemple, un manifeste d’application web déclare que l’application doit être enregistrée pour gérer les protocoles `web+jngl` et `web+jnglstore` .</span><span class="sxs-lookup"><span data-stu-id="db967-171">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

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
 
## <a name="url-link-handling"></a><span data-ttu-id="db967-172">Gestion des liens d’URL</span><span class="sxs-lookup"><span data-stu-id="db967-172">URL Link Handling</span></span>  

<span data-ttu-id="db967-173">Un localisateur de ressources uniforme \(URL\) est un type d’URI.</span><span class="sxs-lookup"><span data-stu-id="db967-173">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="db967-174">Créez une expérience plus attrayante lorsque les applications web progressives \(PWAs\) s’inscrivent en tant que handleurs pour les URIs https.</span><span class="sxs-lookup"><span data-stu-id="db967-174">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="db967-175">Les URS associés peuvent demander à être lancés lorsque les URIs associés sont activés.</span><span class="sxs-lookup"><span data-stu-id="db967-175">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="db967-176">Par exemple, si un utilisateur choisit un lien vers un article d’actualités dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="db967-176">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="db967-177">Un PWA associé pour afficher des articles d’actualités est automatiquement lancé pour gérer l’activation du lien.</span><span class="sxs-lookup"><span data-stu-id="db967-177">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="db967-178">Cette fonctionnalité vous permet d’inscrire un PWA auprès du navigateur à l’aide du manifeste de l’application web et de déclarer que le navigateur gère des liens spécifiques.</span><span class="sxs-lookup"><span data-stu-id="db967-178">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="db967-179">Pour inscrire un PWA avec le navigateur, ajoutez le `url_handlers` membre facultatif au fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="db967-179">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="db967-180">Le membre est un groupe qui groupe les origines des `url_handlers` `object[]` URIs que l’application souhaite gérer.</span><span class="sxs-lookup"><span data-stu-id="db967-180">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="db967-181">La gestion des liens est validée par le navigateur à l’aide d’un `web-app-origin-association` fichier JSON situé sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="db967-181">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="db967-182">Le fichier d’origine affinera davantage les chemins d’accès inclus ou exclus à l’origine.</span><span class="sxs-lookup"><span data-stu-id="db967-182">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="db967-183">Pour obtenir des instructions détaillées sur le test du handler d’URL, accédez à [pwAs en tant que handleurs d’URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]</span><span class="sxs-lookup"><span data-stu-id="db967-183">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="db967-184">Pour afficher un aperçu de la gestion [](#turn-on-experimental-features) des liens d’URL dans Microsoft Edge sur Windows, accédez à Activer les fonctionnalités expérimentales et activer la gestion des **URL PWA de bureau.**</span><span class="sxs-lookup"><span data-stu-id="db967-184">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL  Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="db967-185">Exemple de la url_handlers dans le manifeste</span><span class="sxs-lookup"><span data-stu-id="db967-185">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="db967-186">L’extrait de code suivant est un exemple de manifeste d’application web avec le `url_handlers` membre.</span><span class="sxs-lookup"><span data-stu-id="db967-186">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

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

<span data-ttu-id="db967-187">Un PWA correspond à un URI pour la gestion des URL si l’URI correspond à l’une des chaînes d’origine dans et que le navigateur confirme que l’origine accepte d’autoriser cette application à gérer un tel `url_handlers` URI.</span><span class="sxs-lookup"><span data-stu-id="db967-187">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="db967-188">Le membre contient une origine qui englobe l’étendue, ainsi que d’autres origines non liées `url_handlers` de l’application PWA à l’origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="db967-188">The `url_handlers` member contains an origin that encompasses the scope and also other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="db967-189">Si vous ne limitez pas les URIs à la même étendue ou domaine que pWA à la demande, vous pouvez utiliser des noms de domaine différents pour le même contenu, mais les gérer avec le même PWA.</span><span class="sxs-lookup"><span data-stu-id="db967-189">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="db967-190">Correspondance de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="db967-190">Wildcard matching</span></span>  

<span data-ttu-id="db967-191">Utilisez le caractère générique \( `*` \) pour faire correspondre un ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="db967-191">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="db967-192">Un préfixe générique est utilisé dans les chaînes d’origine du membre à mettre en `url_handlers` correspondance pour différents sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="db967-192">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="db967-193">Le préfixe doit être `*.` pour cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="db967-193">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="db967-194">Le `https` schéma est supposé lorsque vous utilisez un préfixe générique.</span><span class="sxs-lookup"><span data-stu-id="db967-194">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="db967-195">Par exemple, la `url_handlers` valeur de membre est définie sur `*.contoso.com` correspondances et , mais ne `tenant.contoso.com` correspond pas `www.tenant.contoso.com` `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="db967-195">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

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

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

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
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

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

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

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

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

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

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

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
-->  

## <a name="run-on-os-login"></a><span data-ttu-id="db967-196">Exécuter sur la connexion au système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="db967-196">Run On OS Login</span></span>  

<span data-ttu-id="db967-197">Cette fonctionnalité vous permet de configurer le lancement automatique de votre application lorsque l’utilisateur se connecte à Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="db967-197">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="db967-198">Plusieurs classes d’applications tirez parti de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="db967-198">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="db967-199">Les classes d’applications incluent la messagerie électronique, la conversation, le tableau de bord de surveillance et les applications d’affichage de données en temps réel.</span><span class="sxs-lookup"><span data-stu-id="db967-199">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="db967-200">Cette fonctionnalité permet à un utilisateur d’interagir avec les applications dès qu’il se connecte au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="db967-200">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="db967-201">Cette fonctionnalité démarre automatiquement PWA de la même façon qu’elle est lancée manuellement.</span><span class="sxs-lookup"><span data-stu-id="db967-201">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="db967-202">**L’exécuter sur la connexion au** système d’exploitation est une fonctionnalité [puissante.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="db967-202">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="db967-203">Les utilisateurs doivent décider d’activer ou non la fonctionnalité pour l’application web installée.</span><span class="sxs-lookup"><span data-stu-id="db967-203">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="db967-204">Activer l’ouverture de session du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="db967-204">Turn on Run On OS Login</span></span>  

<span data-ttu-id="db967-205">Pour activer les fonctionnalités **d’ouverture** de session [](#turn-on-experimental-features) du système d’exploitation d’exécuter pour votre application PWA, accédez à Activer les fonctionnalités expérimentales et activer les applications de bureau PWA qui s’exécutent sur la connexion **au système d’exploitation.**</span><span class="sxs-lookup"><span data-stu-id="db967-205">To turn on **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activer les applications de bureau de bureau s’exécutent sur l’expérience de connexion au système d’exploitation" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="db967-207">Activer les applications de bureau de bureau **s’exécutent sur l’expérience de connexion au système d’exploitation**</span><span class="sxs-lookup"><span data-stu-id="db967-207">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="db967-208">Activer la fonctionnalité pour l’application web installée</span><span class="sxs-lookup"><span data-stu-id="db967-208">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="db967-209">Pour activer la `Start app when you sign in` fonctionnalité pour un PWA installé,</span><span class="sxs-lookup"><span data-stu-id="db967-209">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="db967-210">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="db967-210">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="db967-211">Accédez `edge://apps` à .</span><span class="sxs-lookup"><span data-stu-id="db967-211">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="db967-212">Pointez sur votre application.</span><span class="sxs-lookup"><span data-stu-id="db967-212">Hover on your app.</span></span>  
1.  <span data-ttu-id="db967-213">Ouvrez le menu contextuel \(clic droit\), puis choisissez **Démarrer l’application lorsque vous vous connectez.**</span><span class="sxs-lookup"><span data-stu-id="db967-213">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Utiliser le menu contextuel pour activer l’application Démarrer lorsque vous vous connectez à la fonctionnalité dans Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="db967-215">Utiliser le menu contextuel pour activer **l’application Démarrer lorsque vous vous connectez** à la fonctionnalité dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db967-215">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="db967-216">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="db967-216">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="db967-217">est un nouveau membre du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="db967-217">is a new member of the manifest file.</span></span>  <span data-ttu-id="db967-218">Il vous permet de définir des liens vers des composants, des pages web clés ou des actions dans votre application web.</span><span class="sxs-lookup"><span data-stu-id="db967-218">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="db967-219">Microsoft Windows l’intègre en tant **que Jumplists**.</span><span class="sxs-lookup"><span data-stu-id="db967-219">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="db967-220">**Les listes de** choix définissent des menus contextuels qui s’affichent lorsque vous êtes sur l’un des éléments d’interface utilisateur suivants et ouvrent un menu contextuel \(clic droit\).</span><span class="sxs-lookup"><span data-stu-id="db967-220">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="db967-221">Une vignette dans le menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="db967-221">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="db967-222">Icône de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="db967-222">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="db967-223">Lorsqu’un utilisateur appelle un raccourci, il navigue jusqu’à l’adresse spécifiée par le membre `url` du raccourci.</span><span class="sxs-lookup"><span data-stu-id="db967-223">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Exemple de jumplists sur Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="db967-225">Exemple de **jumplists** sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="db967-225">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="db967-226">Raccourcis dans le fichier manifeste</span><span class="sxs-lookup"><span data-stu-id="db967-226">Shortcuts in the Manifest file</span></span>  

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

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="db967-227">Propriétés des raccourcis</span><span class="sxs-lookup"><span data-stu-id="db967-227">Properties of shortcuts</span></span>  

<span data-ttu-id="db967-228">Les propriétés suivantes définissent chaque raccourci.</span><span class="sxs-lookup"><span data-stu-id="db967-228">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="db967-229">Propriété</span><span class="sxs-lookup"><span data-stu-id="db967-229">Property</span></span> | <span data-ttu-id="db967-230">Détails</span><span class="sxs-lookup"><span data-stu-id="db967-230">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="db967-231">Chaîne qui s’affiche pour l’utilisateur dans **jumplists** ou le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="db967-231">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="db967-232">Chaîne qui s’affiche lorsque l’espace est insuffisant pour afficher le nom complet du raccourci.</span><span class="sxs-lookup"><span data-stu-id="db967-232">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="db967-233">Chaîne qui décrit l’objectif du raccourci.</span><span class="sxs-lookup"><span data-stu-id="db967-233">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="db967-234">Il est possible d’y accéder par la technologie d’assistance.</span><span class="sxs-lookup"><span data-stu-id="db967-234">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="db967-235">URI dans l’application web qui s’ouvre lorsque le raccourci est activé.</span><span class="sxs-lookup"><span data-stu-id="db967-235">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="db967-236">Ensemble d’icônes qui représente le raccourci.</span><span class="sxs-lookup"><span data-stu-id="db967-236">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="db967-237">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="db967-237">File Handling</span></span>  

<span data-ttu-id="db967-238">La possibilité de s’inscrire en tant que handler de type de fichier est dans la phase d’expérimentation.</span><span class="sxs-lookup"><span data-stu-id="db967-238">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="db967-239">Vous pouvez spécifier les types de fichiers gérés par votre application dans une entrée de manifeste.</span><span class="sxs-lookup"><span data-stu-id="db967-239">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="db967-240">Lors de l’installation, le système d’exploitation hôte de l’utilisateur inscrit votre application en tant que handleur de fichiers pour les types de fichiers répertoriés.</span><span class="sxs-lookup"><span data-stu-id="db967-240">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="db967-241">Assurez-vous que la fonctionnalité existe dans le code de démarrage de vos applications et `launchQueue` qu’elle gère le fichier.</span><span class="sxs-lookup"><span data-stu-id="db967-241">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="db967-242">Les navigateurs basés sur Chromium testent et façonnent cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="db967-242">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="db967-243">Pour plus d’informations, y compris des exemples de code, accédez à [Let web applications be file handlers][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="db967-243">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="db967-244">Pour afficher un aperçu de la gestion des [](#turn-on-experimental-features) fichiers dans Microsoft Edge pour les OS de bureau, accédez à Activer les fonctionnalités expérimentales et activer l’API de **gestion de fichiers.**</span><span class="sxs-lookup"><span data-stu-id="db967-244">To preview file handling in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="db967-245">Commentaires sur les fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="db967-245">Providing feedback on experimental features</span></span>  

<span data-ttu-id="db967-246">Pour fournir des commentaires sur les expériences d’application web Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db967-246">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="db967-247">Envoyez vos commentaires à **l’aide de Paramètres et** plus \( `...` \) > **envoyer des commentaires à Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="db967-247">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="db967-248">Sélectionnez `Alt` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="db967-248">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Envoyer des commentaires à partir de votre PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="db967-250">Envoyer des commentaires à partir de votre PWA</span><span class="sxs-lookup"><span data-stu-id="db967-250">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Essai d’origine | Développeur Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "S’inscrire à l’enregistrement du | Développeur Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Les | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Fonctionnalité puissante : autorisations | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs en tant que | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Que les applications web soient des | web.dev"  
