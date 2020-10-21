---
description: Hébergez un site sur un serveur Web d’ordinateur de développement, puis accédez au contenu d’un appareil Android.
title: Accéder aux serveurs locaux
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f994092460f090743119d7304bfe12aa28556b19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125411"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="f6015-104">Accéder aux serveurs locaux</span><span class="sxs-lookup"><span data-stu-id="f6015-104">Access local servers</span></span>  

<span data-ttu-id="f6015-105">Hébergez un site sur un serveur Web d’ordinateur de développement, puis accédez au contenu d’un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="f6015-106">Avec un câble USB et Microsoft Edge DevTools, exécutez un site à partir d’un ordinateur de développement, puis affichez le site sur un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="f6015-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="f6015-107">Summary</span></span>  

*   <span data-ttu-id="f6015-108">Le transfert de port vous permet d’afficher le contenu hébergé par le serveur Web exécuté sur votre ordinateur de développement sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="f6015-109">Si votre serveur Web utilise un domaine personnalisé, configurez votre appareil Android pour accéder au contenu de ce domaine avec le mappage de domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f6015-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="f6015-110">Configurer le transfert de port</span><span class="sxs-lookup"><span data-stu-id="f6015-110">Set up port forwarding</span></span>  

<span data-ttu-id="f6015-111">Le transfert de port permet à votre appareil Android d’accéder au contenu hébergé sur le serveur Web exécuté sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="f6015-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="f6015-112">Le transfert de port fonctionne en créant un port TCP d’écoute sur votre appareil Android qui mappe vers un port TCP sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="f6015-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="f6015-113">Le trafic entre les ports voyage via la connexion USB entre votre appareil et votre machine de développement Android, de sorte que la connexion ne dépend pas de votre configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="f6015-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="f6015-114">Pour activer le transfert de port:</span><span class="sxs-lookup"><span data-stu-id="f6015-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="f6015-115">Configurez le [débogage à distance][RemoteDebuggingGettingStarted] entre votre ordinateur de développement et votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="f6015-116">Lorsque vous avez terminé, vous devriez voir votre appareil Android dans le menu de gauche de la boîte de dialogue **inspecter les appareils** et un témoin de statut **connecté** .</span><span class="sxs-lookup"><span data-stu-id="f6015-116">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="f6015-117">Dans la boîte de dialogue **inspection des appareils** de devtools, activez le **transfert de port**.</span><span class="sxs-lookup"><span data-stu-id="f6015-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="f6015-118">Cliquez sur **Ajouter une règle**.</span><span class="sxs-lookup"><span data-stu-id="f6015-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Ajout d’une règle de transfert de port" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="f6015-120">Ajout d’une règle de transfert de port</span><span class="sxs-lookup"><span data-stu-id="f6015-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f6015-121">Dans la zone de texte **port du périphérique** à gauche, entrez le `localhost` numéro de port à partir duquel vous voulez accéder au site sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="f6015-122">Par exemple, si vous voulez accéder au site à partir de `localhost:5000` Enter `5000` .</span><span class="sxs-lookup"><span data-stu-id="f6015-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="f6015-123">Dans la zone d' **adresse locale** située à droite, entrez l’adresse IP ou le nom d’hôte sur lequel votre site est hébergé sur le serveur Web exécuté sur votre ordinateur de développement, puis le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="f6015-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="f6015-124">Par exemple, si votre site est en cours d’exécution sur `localhost:7331` Enter (entrée) `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="f6015-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="f6015-125">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f6015-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="f6015-126">Le transfert de port est désormais configuré.</span><span class="sxs-lookup"><span data-stu-id="f6015-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="f6015-127">Pour afficher l’indicateur d’État du port vers l’avant, accédez à l’onglet de votre appareil dans la boîte de dialogue **inspecter les appareils** .</span><span class="sxs-lookup"><span data-stu-id="f6015-127">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Ajout d’une règle de transfert de port" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="f6015-129">État de transfert de port</span><span class="sxs-lookup"><span data-stu-id="f6015-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="f6015-130">Pour afficher le contenu, ouvrez Microsoft Edge sur votre appareil Android et accédez au `localhost` port que vous avez spécifié dans le champ **port** de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f6015-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="f6015-131">Par exemple, si vous avez entré `5000` dans le champ, rendez-vous `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="f6015-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="f6015-132">Mapper aux domaines locaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="f6015-132">Map to custom local domains</span></span>  

<span data-ttu-id="f6015-133">Le mappage de domaine personnalisé vous permet d’afficher le contenu sur un appareil Android à partir d’un serveur Web sur votre ordinateur de développement qui utilise un domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f6015-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="f6015-134">Par exemple, supposons que votre site utilise une bibliothèque JavaScript tierce qui fonctionne uniquement sur le domaine `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="f6015-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="f6015-135">Par conséquent, vous créez une entrée dans votre `hosts` fichier sur votre ordinateur de développement pour mapper ce domaine à `localhost` \ (par exemple, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="f6015-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="f6015-136">Après avoir configuré le mappage de domaine personnalisé et le transfert de port, affichez le site sur votre appareil Android à l’URL `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="f6015-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="f6015-137">Configurer le transfert de port vers le serveur proxy</span><span class="sxs-lookup"><span data-stu-id="f6015-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="f6015-138">Pour mapper un domaine personnalisé, vous devez exécuter un serveur proxy sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="f6015-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="f6015-139">Voici quelques exemples de serveurs proxy: [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]et [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="f6015-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="f6015-140">Pour configurer le renvoi de port vers un proxy:</span><span class="sxs-lookup"><span data-stu-id="f6015-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="f6015-141">Exécutez le serveur proxy et enregistrez le port qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="f6015-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f6015-142">Le serveur proxy et votre serveur Web doivent s’exécuter sur différents ports.</span><span class="sxs-lookup"><span data-stu-id="f6015-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="f6015-143">Configurez le [renvoi de port](#set-up-port-forwarding) vers votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="f6015-144">Pour le champ **adresse locale** , entrez `localhost:` suivi du port sur lequel votre serveur proxy s’exécute.</span><span class="sxs-lookup"><span data-stu-id="f6015-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="f6015-145">Par exemple, s’il est en cours d’exécution sur le port `8000` , accédez à `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="f6015-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="f6015-146">Dans le champ Port de l' **appareil** , entrez le numéro que vous souhaitez que votre appareil Android écoute, par exemple `3333` .</span><span class="sxs-lookup"><span data-stu-id="f6015-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <span data-ttu-id="f6015-147">Configurer les paramètres de proxy sur votre appareil</span><span class="sxs-lookup"><span data-stu-id="f6015-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="f6015-148">Ensuite, vous devez configurer votre appareil Android pour communiquer avec le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="f6015-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="f6015-149">Sur votre appareil Android, accédez à **réglages**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="f6015-149">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="f6015-150">Appuyez longuement sur le nom du réseau auquel vous êtes actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="f6015-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f6015-151">Les paramètres de proxy s’appliquent par réseau.</span><span class="sxs-lookup"><span data-stu-id="f6015-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="f6015-152">Sélectionnez **modifier le réseau**.</span><span class="sxs-lookup"><span data-stu-id="f6015-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="f6015-153">Sélectionnez **Options avancées**.</span><span class="sxs-lookup"><span data-stu-id="f6015-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="f6015-154">Les paramètres du proxy apparaissent.</span><span class="sxs-lookup"><span data-stu-id="f6015-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="f6015-155">Sélectionnez le menu **proxy** , puis choisissez **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="f6015-155">Select the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="f6015-156">Pour le champ **nom_hôte du proxy** , entrez `localhost` .</span><span class="sxs-lookup"><span data-stu-id="f6015-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="f6015-157">Pour le champ **port proxy** , entrez le numéro de port que vous avez entré pour **port d’appareil** dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="f6015-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="f6015-158">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f6015-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="f6015-159">À l’aide de ces paramètres, votre appareil transfère toutes les demandes à ce proxy sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="f6015-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="f6015-160">Le serveur proxy effectue des demandes de la part de votre appareil, de sorte que les demandes adressées à votre domaine local personnalisé sont correctement résolues.</span><span class="sxs-lookup"><span data-stu-id="f6015-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="f6015-161">Accédez désormais aux domaines personnalisés sur votre appareil Android tout comme sur l’ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="f6015-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="f6015-162">Si votre serveur Web est en cours d’exécution sur un port autre qu’un port standard, n’oubliez pas de spécifier le port lors de la demande du contenu à partir de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="f6015-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="f6015-163">Par exemple, si votre serveur Web utilise le domaine personnalisé `microsoft-edge.devtools` sur le port `7331` , lorsque vous affichez le site à partir de votre appareil Android, vous devez utiliser l’URL `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="f6015-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="f6015-164">Pour reprendre la navigation normale, n’oubliez pas de rétablir les paramètres de proxy sur votre appareil Android après vous être déconnecté de l’ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="f6015-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <span data-ttu-id="f6015-165">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f6015-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de débogage Web Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: optimisation de la remise sur le Web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler-proxy de débogage Web gratuit"  

> [!NOTE]
> <span data-ttu-id="f6015-170">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f6015-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f6015-171">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="f6015-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f6015-173">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f6015-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
