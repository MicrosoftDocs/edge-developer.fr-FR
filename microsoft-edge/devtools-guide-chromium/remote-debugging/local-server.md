---
description: Hébergez un site sur un serveur web d’ordinateur de développement, puis accédez au contenu à partir d’un appareil Android.
title: Accéder aux serveurs locaux
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 51ef0d951d587d310b6474698924d9f87cf68607
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461261"
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
# <a name="access-local-servers"></a><span data-ttu-id="3f1c1-104">Accéder aux serveurs locaux</span><span class="sxs-lookup"><span data-stu-id="3f1c1-104">Access local servers</span></span>  

<span data-ttu-id="3f1c1-105">Hébergez un site sur un serveur web d’ordinateur de développement, puis accédez au contenu à partir d’un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="3f1c1-106">Avec un câble USB et Microsoft Edge DevTools, exécutez un site à partir d’un ordinateur de développement, puis affichez le site sur un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <a name="summary"></a><span data-ttu-id="3f1c1-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="3f1c1-107">Summary</span></span>  

*   <span data-ttu-id="3f1c1-108">Le portage vous permet d’afficher le contenu hébergé par le serveur web s’exécutant sur votre ordinateur de développement sur votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="3f1c1-109">Si votre serveur web utilise un domaine personnalisé, configurer votre appareil Android pour accéder au contenu de ce domaine avec le mappage de domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <a name="set-up-port-forwarding"></a><span data-ttu-id="3f1c1-110">Configurer le forwarding de port</span><span class="sxs-lookup"><span data-stu-id="3f1c1-110">Set up port forwarding</span></span>  

<span data-ttu-id="3f1c1-111">Le portage permet à votre appareil Android d’accéder au contenu hébergé sur le serveur web en cours d’exécution sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="3f1c1-112">Le portage fonctionne en créant un port TCP d’écoute sur votre appareil Android qui est mappé à un port TCP sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="3f1c1-113">Le trafic entre les ports passe par la connexion USB entre votre appareil Android et votre ordinateur de développement, de sorte que la connexion ne dépend pas de votre configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="3f1c1-114">Pour activer le portage :</span><span class="sxs-lookup"><span data-stu-id="3f1c1-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="3f1c1-115">Configurer le [débogage à distance][RemoteDebuggingGettingStarted] entre votre ordinateur de développement et votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="3f1c1-116">Lorsque vous avez terminé, votre appareil Android doit s’afficher  dans le menu gauche de la boîte de dialogue Inspecter les appareils et un **indicateur d’état** Connecté.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-116">When you are finished, your Android device should be displayed in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="3f1c1-117">Dans la **boîte de dialogue Inspecter les** appareils dans DevTools, activez le **portage.**</span><span class="sxs-lookup"><span data-stu-id="3f1c1-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="3f1c1-118">Choose **Add rule**.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Ajout d’une règle de forwarding de port" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="3f1c1-120">Ajout d’une règle de forwarding de port</span><span class="sxs-lookup"><span data-stu-id="3f1c1-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3f1c1-121">Dans la **zone de texte** Du port de l’appareil sur la gauche, entrez le numéro de port à partir duquel vous souhaitez pouvoir accéder au site sur votre appareil `localhost` Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="3f1c1-122">Par exemple, si vous souhaitez accéder au site à partir `localhost:5000` `5000` d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="3f1c1-123">Dans  la zone de texte Adresse locale à droite, entrez l’adresse IP ou le nom d’hôte sur lequel votre site est hébergé sur le serveur web en cours d’exécution sur votre ordinateur de développement, suivi du numéro de port.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="3f1c1-124">Par exemple, si votre site est en cours d’exécution sur `localhost:7331` entrée `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="3f1c1-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="3f1c1-125">Choose **Add**.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="3f1c1-126">Le forwarding de port est maintenant installé.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="3f1c1-127">Examinez l’indicateur d’état du port avant sous l’onglet de votre appareil dans la boîte de dialogue **Inspecter les appareils.**</span><span class="sxs-lookup"><span data-stu-id="3f1c1-127">Review the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="État du port de forwarding" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="3f1c1-129">État du port de forwarding</span><span class="sxs-lookup"><span data-stu-id="3f1c1-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="3f1c1-130">Pour afficher le contenu, ouvrez Microsoft Edge sur votre appareil Android et allez au port que vous avez spécifié dans le champ `localhost` **Port de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="3f1c1-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="3f1c1-131">Par exemple, si vous avez `5000` entré dans le champ, visitez `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="3f1c1-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <a name="map-to-custom-local-domains"></a><span data-ttu-id="3f1c1-132">Ma map to custom local domains</span><span class="sxs-lookup"><span data-stu-id="3f1c1-132">Map to custom local domains</span></span>  

<span data-ttu-id="3f1c1-133">Le mappage de domaine personnalisé vous permet d’afficher le contenu sur un appareil Android à partir d’un serveur web sur votre ordinateur de développement qui utilise un domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="3f1c1-134">Par exemple, supposons que votre site utilise une bibliothèque JavaScript tierce qui fonctionne uniquement sur le `microsoft-edge.devtools` domaine.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="3f1c1-135">Par exemple, vous créez une entrée dans votre fichier sur votre ordinateur de développement pour ma cartographier ce domaine sur `hosts` `localhost` \(par `127.0.0.1 microsoft-edge.devtools` exemple, \).</span><span class="sxs-lookup"><span data-stu-id="3f1c1-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="3f1c1-136">Après avoir mis en place le mappage de domaine personnalisé et le forwarding de port, affichez le site sur votre appareil Android à `microsoft-edge.devtools` l’URL.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <a name="set-up-port-forwarding-to-proxy-server"></a><span data-ttu-id="3f1c1-137">Configurer le port de forwarding vers le serveur proxy</span><span class="sxs-lookup"><span data-stu-id="3f1c1-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="3f1c1-138">Pour ma cartographier un domaine personnalisé, vous devez exécuter un serveur proxy sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="3f1c1-139">Par exemple, les serveurs proxy [sont Charles][CharlesWebDebuggingProxy], Fiddler et [Fiddler.][FiddlerWebDebuggingProxy] [][SquidOptimisingWebDelivery]</span><span class="sxs-lookup"><span data-stu-id="3f1c1-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="3f1c1-140">Pour configurer le port de forwarding vers un proxy :</span><span class="sxs-lookup"><span data-stu-id="3f1c1-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="3f1c1-141">Exécutez le serveur proxy et enregistrez le port qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3f1c1-142">Le serveur proxy et votre serveur web doivent s’exécuter sur différents ports.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="3f1c1-143">Configurer le [portage vers](#set-up-port-forwarding) votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="3f1c1-144">Pour le **champ d’adresse** local, entrez suivi du port sur `localhost:` qui votre serveur proxy est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="3f1c1-145">Par exemple, s’il est en cours d’exécution sur le `8000` port, accédez à `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="3f1c1-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="3f1c1-146">Dans le **champ port de l’appareil,** entrez le numéro que vous souhaitez que votre appareil Android écoute, par `3333` exemple.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <a name="configure-proxy-settings-on-your-device"></a><span data-ttu-id="3f1c1-147">Configurer les paramètres de proxy sur votre appareil</span><span class="sxs-lookup"><span data-stu-id="3f1c1-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="3f1c1-148">Ensuite, vous devez configurer votre appareil Android pour communiquer avec le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="3f1c1-149">Sur votre appareil Android, accédez à **Paramètres**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-149">On your Android device, navigate to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="3f1c1-150">Appuyez longuement sur le nom du réseau auquel vous êtes actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3f1c1-151">Les paramètres proxy s’appliquent par réseau.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="3f1c1-152">Choose **Modify network**.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="3f1c1-153">Choisissez **Options avancées.**</span><span class="sxs-lookup"><span data-stu-id="3f1c1-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="3f1c1-154">Les paramètres du proxy s’affichent.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="3f1c1-155">Choisissez le menu **proxy** et choisissez **Manuel.**</span><span class="sxs-lookup"><span data-stu-id="3f1c1-155">Choose the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="3f1c1-156">Pour le **champ Nom d’hôte proxy,** entrez `localhost` .</span><span class="sxs-lookup"><span data-stu-id="3f1c1-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="3f1c1-157">Pour le **champ Port proxy,** entrez le numéro de port que vous avez entré pour le **port** d’appareil dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="3f1c1-158">Choose **Save**.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="3f1c1-159">Avec ces paramètres, votre appareil forwarde toutes ses demandes au proxy sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="3f1c1-160">Le proxy effectue des demandes au nom de votre appareil, afin que les demandes à votre domaine local personnalisé soient correctement résolues.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="3f1c1-161">Accédez maintenant à des domaines personnalisés sur votre appareil Android, comme sur l’ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="3f1c1-162">Si votre serveur web s’exécute hors d’un port non standard, n’oubliez pas de spécifier le port lorsque vous demandez le contenu à partir de votre appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="3f1c1-163">Par exemple, si votre serveur web utilise le domaine personnalisé sur le port, lorsque vous affichez le site à partir de votre appareil Android, vous devez utiliser `microsoft-edge.devtools` `7331` l’URL `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="3f1c1-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="3f1c1-164">Pour reprendre la navigation normale, n’oubliez pas de revenir aux paramètres proxy de votre appareil Android après vous être déconnecté de l’ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="3f1c1-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3f1c1-165">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="3f1c1-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de débogage Web Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "programme d’optimisation de la distribution web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler - Proxy de débogage web gratuit"  

> [!NOTE]
> <span data-ttu-id="3f1c1-170">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f1c1-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3f1c1-171">La page d’origine est trouvée ici et est co-auteure par [Les Basques DeCénais (Rédacteur][KayceBasques] technique, Chrome DevTools \& Writer\) et [Meggin Kearney][MegginKearney] \(Tech Writer\). [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server)</span><span class="sxs-lookup"><span data-stu-id="3f1c1-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="3f1c1-173">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f1c1-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
