---
ms.assetid: ef705c70-73f8-445b-84ed-4f83679f1980
description: Découvrez comment les communications en temps réel entre objets permettent aux médias d’être diffusés en continu en temps réel entre les navigateurs Web, les appareils mobiles et les serveurs.
title: Guide de développement-objet RTC API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: ac033ea26fa7c1eb435b0164e5dbd2a3a5428474
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564692"
---
# <span data-ttu-id="189bd-104">API RTC Object</span><span class="sxs-lookup"><span data-stu-id="189bd-104">Object RTC API</span></span>

<span data-ttu-id="189bd-105">Les communications en temps réel entre objets (ORTC) permettent le lecture de contenu multimédia (audio et/ou vidéo) en temps réel entre les navigateurs Web, les appareils mobiles et les serveurs par le biais des API JavaScript natives.</span><span class="sxs-lookup"><span data-stu-id="189bd-105">Object Real-Time Communications (ORTC) enables media (audio and/or video) to be streamed (sent and received) in real-time directly between web browsers, mobile devices, and servers via native Javascript APIs.</span></span>

> [!NOTE]
> <span data-ttu-id="189bd-106">Microsoft Edge implémente désormais le ORTC pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="189bd-106">Microsoft Edge now implements ORTC for Windows 10 devices.</span></span> <span data-ttu-id="189bd-107">Toutefois, cette implémentation diffère de la version la plus récente de l' [API ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span><span class="sxs-lookup"><span data-stu-id="189bd-107">However, this implementation differs from the most recent version of the [ORTC API](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span></span> <span data-ttu-id="189bd-108">La norme ORTC a continué d’évoluer depuis le développement et la publication de Microsoft Edge: le navigateur n’implémente pas chaque objet ou méthode au sein de l’API ORTC et inclut des extensions qui ne sont pas actuellement incorporées dans la spécification.</span><span class="sxs-lookup"><span data-stu-id="189bd-108">ORTC has continued to evolve since the development and release of Microsoft Edge -- the browser does not implement every object or method within the ORTC API, and includes extensions not currently incorporated within the specification.</span></span> <span data-ttu-id="189bd-109">D’autres développements seront poursuivis pour permettre aux développeurs de tout le monde de créer des expériences qui incluent la possibilité de parler aux utilisateurs de Skype et aux services de communication compatibles WebRTC.</span><span class="sxs-lookup"><span data-stu-id="189bd-109">Further development will continue with the goal to enable developers around the world to build experiences that include the ability to talk to Skype users and other WebRTC compatible communication services.</span></span>



<span data-ttu-id="189bd-110">Pour bénéficier d’une expérience pratique avec la fonction ORTC, testez ces démonstrations sur le lecteur:</span><span class="sxs-lookup"><span data-stu-id="189bd-110">To get a hands-on experience with ORTC, try out these demos on Test Drive:</span></span>
-  [<span data-ttu-id="189bd-111">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="189bd-111">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [<span data-ttu-id="189bd-112">Appel téléphonique ORTC</span><span class="sxs-lookup"><span data-stu-id="189bd-112">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [<span data-ttu-id="189bd-113">Démonstration ORTC</span><span class="sxs-lookup"><span data-stu-id="189bd-113">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


<span data-ttu-id="189bd-114">Pour plus d’informations sur la fonction ORTC, voir l' [API ORTC est désormais disponible dans Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) sur le blog du développement Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="189bd-114">For more information about ORTC, check out [ORTC API is now available in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) on the Microsoft Edge dev blog.</span></span>


## <span data-ttu-id="189bd-115">Diagramme de vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="189bd-115">Overview Diagram</span></span>


<span data-ttu-id="189bd-116">Le diagramme ci-dessous fournit un récapitulatif des relations entre les objets ORTC.</span><span class="sxs-lookup"><span data-stu-id="189bd-116">The diagram below provides a summary describing relationships between ORTC objects.</span></span> <span data-ttu-id="189bd-117">Les flèches horizontales ou inclinées indiquent le flux de média ou de données, alors que les flèches verticales indiquent les interactions par le biais de méthodes et d’événements.</span><span class="sxs-lookup"><span data-stu-id="189bd-117">Horizontal or slanted arrows denote the flow of media or data, whereas vertical arrows denote interactions via methods and events.</span></span>

<span data-ttu-id="189bd-118">La fonction ORTC utilise les objets «*sender*», «*Receiver*» et «*transport*», qui ont des «*fonctionnalités*» qui décrivent ce qu’ils sont en mesure d’effectuer, ainsi que des «*paramètres*» définissant ce qu’ils sont configurés.</span><span class="sxs-lookup"><span data-stu-id="189bd-118">ORTC uses "*sender*", "*receiver*" and "*transport*" objects, which have "*capabilities*" describing what they are capable of doing, as well as "*parameters*" which define what they are configured to do.</span></span> <span data-ttu-id="189bd-119">«*Pistes*» capturez et encodez les flux multimédias par les expéditeurs, en circulant sur les transports, puis décodés par des récepteurs qui effectuent le rendu des pistes du flux multimédia pour les balises vidéo/audio.</span><span class="sxs-lookup"><span data-stu-id="189bd-119">"*Tracks*" capture and encode media streams by senders, traveling over transports, then decoded by receivers that render the media stream tracks to video/audio tags.</span></span>

![<span data-ttu-id="189bd-120">Diagramme de flux Microsoft Edge ORTC ](./../media/ortc_diagram.png) dans l’illustration ci-dessus, le [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) code effectue le suivi fourni en entrée, qui est transporté sur une [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) ou une [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) .</span><span class="sxs-lookup"><span data-stu-id="189bd-120">Microsoft Edge ORTC Flow Diagram](./../media/ortc_diagram.png) In the figure above, the [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) encodes the track provided as input, which is transported over a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) or an [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527).</span></span> <span data-ttu-id="189bd-121">L’envoi de tonalités DTMF (Dual-tonalité multifréquence) est pris en charge par le biais de [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .</span><span class="sxs-lookup"><span data-stu-id="189bd-121">Sending of Dual Tone Multi Frequency (DTMF) tones is supported via the [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496).</span></span>

<span data-ttu-id="189bd-122">La [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) et [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilise une [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) pour sélectionner une voie de communication pour joindre l’homologue de réception `RTCIceTransport` , qui est à son tour associé à un `RTCDtlsTransport` ou `RTCSrtpSdesTransport` de ces éléments [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="189bd-122">The [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) and [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilize an [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) to select a communication path to reach the receiving peer's `RTCIceTransport`, which is in turn associated with an `RTCDtlsTransport` or `RTCSrtpSdesTransport` which de-multiplexes media to the [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span> <span data-ttu-id="189bd-123">Le `RTCRtpReceiver` code multimédia, puis décode, génère une piste rendue par une balise audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="189bd-123">The `RTCRtpReceiver` then decodes media, producing a track which is rendered by an audio or video tag.</span></span>

<span data-ttu-id="189bd-124">Plusieurs autres objets jouent également un rôle.</span><span class="sxs-lookup"><span data-stu-id="189bd-124">Several other objects also play a role.</span></span> <span data-ttu-id="189bd-125">Le [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) rassemblement de candidatures de glace locales pour une utilisation par un seul [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) objet.</span><span class="sxs-lookup"><span data-stu-id="189bd-125">The [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) gathers local ICE candidates for use by a single [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) object.</span></span> <span data-ttu-id="189bd-126">Les sections restantes de l’API remplissent des détails relatifs aux *fonctionnalités* et *paramètres*RTP, aux *statistiques opérationnelles* et à la compatibilité avec l' [API 1,0 WebRTC](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span><span class="sxs-lookup"><span data-stu-id="189bd-126">Remaining sections of the API fill in details relating to RTP *capabilities* and *parameters*, *operational statistics* and compatibility with the [WebRTC 1.0 API](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span></span>

> [!NOTE]
> <span data-ttu-id="189bd-127">Dans la mesure où Microsoft Edge n’implémente pas le canal de données, les `RTCDataChannel` objets et ne `RTCSctpTransport` sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-127">Since Microsoft Edge does not implement the data channel, the `RTCDataChannel` and `RTCSctpTransport` objects are not supported.</span></span>




## <span data-ttu-id="189bd-128">Composants pris en charge dans l’implémentation initiale de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="189bd-128">Components supported in the initial Microsoft Edge implementation</span></span>


* **<span data-ttu-id="189bd-129">Prise en charge de l’API ORTC.</span><span class="sxs-lookup"><span data-stu-id="189bd-129">ORTC API support.</span></span>** <span data-ttu-id="189bd-130">Les communications audio/vidéo sont le principal foyer, y compris les objets suivants:,,,, ainsi que [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) les [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces qui ne s’affichent pas directement dans le diagramme.</span><span class="sxs-lookup"><span data-stu-id="189bd-130">Audio/video communications is the primary focus, including the following objects: [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107), [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112), [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495), [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516), [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508), as well as the [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces that are not shown directly in the diagram.</span></span>
* **<span data-ttu-id="189bd-131">Prise en charge du multiplexage RTP/RTCP.</span><span class="sxs-lookup"><span data-stu-id="189bd-131">RTP/RTCP multiplexing support.</span></span>** <span data-ttu-id="189bd-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)est requis pour l’utilisation de [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) .</span><span class="sxs-lookup"><span data-stu-id="189bd-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503) is required for use with the [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495).</span></span> <span data-ttu-id="189bd-133">Le multiplexage a/V est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-133">A/V multiplexing is also supported.</span></span>
* **<span data-ttu-id="189bd-134">Support STUN/TURN/ICE.</span><span class="sxs-lookup"><span data-stu-id="189bd-134">STUN/TURN/ICE support.</span></span>** <span data-ttu-id="189bd-135">STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) et Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621)sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-135">STUN [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), TURN [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) as well as ICE [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621), are supported.</span></span> <span data-ttu-id="189bd-136">Dans le cadre de la glace, la dénomination normale est prise en charge, avec une désignation agressive entièrement prise en charge (en tant que destinataire).</span><span class="sxs-lookup"><span data-stu-id="189bd-136">Within ICE, regular nomination is supported, with aggressive nomination partially supported (as a receiver).</span></span> <span data-ttu-id="189bd-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) est pris en charge en fonction de DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span><span class="sxs-lookup"><span data-stu-id="189bd-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) is supported, based on DTLS 1.0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span></span>
* **<span data-ttu-id="189bd-138">Prise en charge du codec.</span><span class="sxs-lookup"><span data-stu-id="189bd-138">Codec support.</span></span>** <span data-ttu-id="189bd-139">Pour les [codecs audio](https://msdn.microsoft.com/library/Mt599587), nous prenons en charge g. 711, g. 722, opus et soie.</span><span class="sxs-lookup"><span data-stu-id="189bd-139">For [audio codecs](https://msdn.microsoft.com/library/Mt599587), we support G.711, G.722, Opus and SILK.</span></span> <span data-ttu-id="189bd-140">Nous prenons également en charge les bruits de confort (CN) et DTMF en fonction de la configuration audio RTCWEB.</span><span class="sxs-lookup"><span data-stu-id="189bd-140">We also support Comfort Noise (CN) and DTMF according to the RTCWEB audio requirements.</span></span> <span data-ttu-id="189bd-141">Pour la vidéo, le codec utilisé par les services Skype est actuellement pris en charge [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) , à l’aide des fonctionnalités avancées telles que la simultanéité, le codage vidéo évolutif et la correction des erreurs de transfert.</span><span class="sxs-lookup"><span data-stu-id="189bd-141">For video we currently support the [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec used by Skype services, supporting advanced features such as simulcast, scalable video coding and forward error correction.</span></span> <span data-ttu-id="189bd-142">Nous travaillons à l’activation de la vidéo interopérable avec H. 264.</span><span class="sxs-lookup"><span data-stu-id="189bd-142">We're working toward to enabling interoperable video with H.264.</span></span>

> [!NOTE]
> <span data-ttu-id="189bd-143">Si vous connaissez les implémentations de WebRTC 1,0 et que vous êtes intéressé par l’évolution de la prise en charge des objets dans WebRTC 1,0 et ORTC, nous recommandons la présentation suivante par Google, Microsoft et Hookflash à partir de la Conférence 2014 IIT RTC: «[mise à jour d’API ORTC](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)».</span><span class="sxs-lookup"><span data-stu-id="189bd-143">If you are familiar with WebRTC 1.0 implementations, and are interested in the evolution of object support within WebRTC 1.0 and ORTC, we recommend the following presentation by Google, Microsoft, and Hookflash from the 2014 IIT RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)."</span></span>




## <span data-ttu-id="189bd-144">Flux de code de niveau application pour les communications 1:1</span><span class="sxs-lookup"><span data-stu-id="189bd-144">App level code flow for 1:1 communications</span></span>


<span data-ttu-id="189bd-145">Pour ce scénario, deux ordinateurs Windows 10 font office de deux homologues avec un serveur WebServer comme canal de signalisation pour échanger des informations entre les homologues afin qu’une connexion puisse être établie entre eux.</span><span class="sxs-lookup"><span data-stu-id="189bd-145">For this scenario, two Windows 10 machines will act as two peers with a webserver as the signaling channel to exchange information between the peers so that a connection may be established between them.</span></span>

<span data-ttu-id="189bd-146">Les étapes ci-dessous sont limitées aux opérations effectuées par un homologue.</span><span class="sxs-lookup"><span data-stu-id="189bd-146">The steps below are scoped to operations taken by one peer.</span></span> <span data-ttu-id="189bd-147">Les deux homologues doivent suivre les étapes ci-dessous afin de configurer les communications 1:1.</span><span class="sxs-lookup"><span data-stu-id="189bd-147">Both peers must go through similar steps in order to set up the 1:1 communications.</span></span> <span data-ttu-id="189bd-148">Pour plus d’informations sur les extraits de code ci-dessous, reportez-vous à la [démonstration Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="189bd-148">To make better sense out of the code snippets below, refer to the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

<span data-ttu-id="189bd-149">Cet exemple utilise le multiplexage audio-vidéo et RTP/RTCP, de sorte que vous ne voyez qu’un seul transport de glace et de DTLS, utilisé pour transporter les paquets RTP et RTCP pour les appels audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="189bd-149">This example uses audio-video and RTP/RTCP multiplexing, so you will see only a single ICE and DTLS transport, used to transport RTP and RTCP packets for both audio and video.</span></span>

`Step #1.` <span data-ttu-id="189bd-150">Créer [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) un objet (par exemple [, API de capture multimédia et de flux](./../multimedia/media-Capture-and-Streams.md)) avec une piste audio et une piste vidéo.</span><span class="sxs-lookup"><span data-stu-id="189bd-150">Create [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) object (i.e. [Media Capture and Streams API](./../multimedia/media-Capture-and-Streams.md)) with one audio track and one video track.</span></span>

```js
navigator.MediaDevices.getUserMedia ({
    "audio": true,
    "video": {
        width: 640,
        height: 360,
        facingMode: "user"
    }
}).then(
    gotStream
).catch(
    gotMediaError
);

function gotStream(stream) {
    var mediaStreamLocal = stream;
    …
}
```

`Step #2.` <span data-ttu-id="189bd-151">Créez le [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) et activez local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) pour être signalé au pair distant.</span><span class="sxs-lookup"><span data-stu-id="189bd-151">Create the [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx), and enable local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) to be signaled to remote peer.</span></span>

```js
var iceOptions = new RTCIceGatherOptions;
iceOptions.gatherPolicy = "all";
iceOptions.iceservers = ... ;
var iceGathr = new RTCIceGatherer(iceOptions);
iceGathr.onlocalcandidate = function(evt) {
    mySignaller.signalMessage({
        "candidate": evt.candidate
    });
};
```

<span data-ttu-id="189bd-152">Pour vous aider à protéger la vie privée de l’utilisateur, Microsoft Edge introduit une option qui permet à un utilisateur de contrôler si les adresses IP d’hôte local peuvent être exposées par les [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objets.</span><span class="sxs-lookup"><span data-stu-id="189bd-152">To help protect user privacy, Microsoft Edge introduces an option that allows a user to control whether local host IP addresses can be exposed by the [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objects.</span></span> <span data-ttu-id="189bd-153">Une option d’interface sera fournie pour activer ou désactiver ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="189bd-153">An interface option will be provided to toggle this setting.</span></span>

<span data-ttu-id="189bd-154">Dans la [démonstration Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635), un serveur Turn a été configuré.</span><span class="sxs-lookup"><span data-stu-id="189bd-154">In the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635), a TURN server has been set up.</span></span> <span data-ttu-id="189bd-155">Le débit du serveur est très limité et ne peut être utilisé que sur la page de démonstration.</span><span class="sxs-lookup"><span data-stu-id="189bd-155">This TURN server has a very limited throughput, so is limited to only demo page use.</span></span>

`Step #3.` <span data-ttu-id="189bd-156">Créez le [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) périphérique audio et vidéo et préparez-vous à gérer [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) la télécommande sur le transport de glace.</span><span class="sxs-lookup"><span data-stu-id="189bd-156">Create the [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) for audio and video, and prepare to handle remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) on the ICE transport.</span></span>

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

<span data-ttu-id="189bd-157">Une autre option consiste à accumuler tous les candidats à distance de glace dans un tableau `remoteCandidates` et `iceTr.setRemoteCandidates(remoteCandidates)` à appeler pour ajouter tous les candidats distants.</span><span class="sxs-lookup"><span data-stu-id="189bd-157">Another option here is to accumulate all the remote ICE candidates into an array `remoteCandidates` and call `iceTr.setRemoteCandidates(remoteCandidates)` to add all the remote candidates together.</span></span>

`Step #4.` <span data-ttu-id="189bd-158">Créez le transport DTLS.</span><span class="sxs-lookup"><span data-stu-id="189bd-158">Create the DTLS transport.</span></span>

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` <span data-ttu-id="189bd-159">Créez les objets expéditeur et destinataire.</span><span class="sxs-lookup"><span data-stu-id="189bd-159">Create the sender and receiver objects.</span></span>

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

<span data-ttu-id="189bd-160">Étape #6.</span><span class="sxs-lookup"><span data-stu-id="189bd-160">Step #6.</span></span> <span data-ttu-id="189bd-161">Récupérer les fonctionnalités du destinataire et de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="189bd-161">Retrieve the receiver and sender capabilities.</span></span>

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` <span data-ttu-id="189bd-162">Les paramètres de glace/DTLS et les fonctionnalités d’envoi et de réception peuvent être échangés.</span><span class="sxs-lookup"><span data-stu-id="189bd-162">ICE/DTLS parameters and Send/Receive capabilities can be exchanged.</span></span>

```js
mySignaller.signalMessage({
    "ice": iceGathr.getLocalParameters(),
    "dtls": dtlsTr.getLocalParameters(),
    "recvAudioCaps": recvAudioCaps,
    "recvVideoCaps": recvVideoCaps,
    "sendAudioCaps": sendAudioCaps,
    "sendVideoCaps": sendVideoCaps
};
```

`Step #8.` <span data-ttu-id="189bd-163">Obtenez les paramètres distants, démarrez le [`ICE`](https://msdn.microsoft.com/library/Mt433112) et [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, puis définissez les paramètres d’envoi et de réception audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="189bd-163">Get remote params, start the [`ICE`](https://msdn.microsoft.com/library/Mt433112) and [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, and set the audio and video send and receive parameters.</span></span>

```js
mySignaller.onRemoteParams = function(params) {
    // The responder answers with its preferences, parameters and capabilities
    // Derive the send and receive parameters.
    var audioSendParams = myCapsToSendParams(sendAudioCaps, params.recvAudioCaps);
    var videoSendParams = myCapsToSendParams(sendVideoCaps, params.recvVideoCaps);
    var audioRecvParams = myCapsToRecvParams(recvAudioCaps, params.sendAudioCaps);
    var videoRecvParams = myCapsToRecvParams(recvVideoCaps, params.sendVideoCaps);
    iceTr.start(iceGathr, params.ice, RTCIceRole.controlling);
    dtlsTr.start(params.dtls);
    audioSender.send(audioSendParams);
    videoSender.send(videoSendParams);
    audioReceiver.receive(audioRecvParams);
    videoReceiver.receive(videoRecvParams);
};
```

<span data-ttu-id="189bd-164">Vous trouverez ci-dessous une structure des fonctions d’assistance.</span><span class="sxs-lookup"><span data-stu-id="189bd-164">Below is a skeleton of the helper functions.</span></span> <span data-ttu-id="189bd-165">Pour plus d’informations, consultez la [démonstration Microsoft Edge test](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="189bd-165">Find more details in the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

```js
RTCRtpParameters function myCapsToSendParams (RTCRtpCapabilities sendCaps, RTCRtpCapabilities remoteRecvCaps) {
    // Function returning the sender RTCRtpParameters, based on intersection of the local sender and remote receiver capabilities.
    // Steps to be followed:
    // 1. Determine the RTP features that the receiver and sender have in common.
    // 2. Determine the codecs that the sender and receiver have in common.
    // 3. Within each common codec, determine the common formats and rtcpFeedback mechanisms.
    // 4. Determine the payloadType to be used, based on the receiver preferredPayloadType.
    // 5. Set RTCRtcpParameters such as mux to their default values.  
}

RTCRtpParameters function myCapsToRecvParams(RTCRtpCapabilities recvCaps, RTCRtpCapabilities remoteSendCaps) {
    return myCapsToSendParams(remoteSendCaps, recvCaps);
}
```

`Step #9.` <span data-ttu-id="189bd-166">Afficher et lire le flux multimédia distant effectue le suivi d’une balise vidéo.</span><span class="sxs-lookup"><span data-stu-id="189bd-166">Render and play the remote media stream tracks through a video tag.</span></span>

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

<span data-ttu-id="189bd-167">Dès lors que vous avez configuré les appels 1:1, appliquez les mêmes principes pour configurer les appels de groupe de petite taille à l’aide d’une topologie de maille, où chaque homologue aura une connexion 1:1 avec le reste du groupe.</span><span class="sxs-lookup"><span data-stu-id="189bd-167">Once familiar with setting up 1:1 calls, apply the same principles to set up small group calls using a mesh topology, where each peer will have a 1:1 connection with the rest of the group.</span></span> <span data-ttu-id="189bd-168">Dans la mesure où la fonction de bifurcation parallèle n’est pas prise en charge sur la plateforme Microsoft Edge, cela doit être géré par le biais de la signalisation 1:1 de sorte que les [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objets indépendants et puissent [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) être utilisés pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="189bd-168">Since parallel forking is not supported on the Microsoft Edge platform, this should be handled via 1:1 signaling, so that independent [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) and [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objects will be used for each connection.</span></span>

## <span data-ttu-id="189bd-169">Détails de l’implémentation dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="189bd-169">Implementation details in Microsoft Edge</span></span>


<span data-ttu-id="189bd-170">La spécification ORTC est relativement stable dans la mesure où le groupe de la communauté de ORTC a émis les «appels pour les implémentations» et les défis importants liés au niveau de l’API JavaScript ne sont pas attendus.</span><span class="sxs-lookup"><span data-stu-id="189bd-170">The ORTC spec has been relatively stable since the ORTC Community Group issued the "Call for Implementations," and significant challenges at the JavaScript API level are not expected.</span></span> <span data-ttu-id="189bd-171">En fonction de ce qui suit, l’implémentation de Microsoft Edge a été publiée pour les tests d’interopérabilité entre les navigateurs au niveau du protocole.</span><span class="sxs-lookup"><span data-stu-id="189bd-171">Based on this, Microsoft Edge implementation has been released for cross-browser interoperability testing at the protocol level.</span></span>

<span data-ttu-id="189bd-172">Voici quelques limitations de l’implémentation de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="189bd-172">A few limitations in the Microsoft Edge implementation should be noted:</span></span>

* `RTCIceTransportController` <span data-ttu-id="189bd-173">n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-173">is not supported.</span></span> <span data-ttu-id="189bd-174">L’implémentation de Microsoft Edge gère la congélation et l’incongélation de glace pour chaque transport, de telle sorte que la commande All `IceTransports` n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="189bd-174">Microsoft Edge implementation handles ICE freezing/unfreezing on a per-transport basis, so that ordering all the `IceTransports` is not necessary.</span></span> <span data-ttu-id="189bd-175">Cette approche doit interopérer avec des implémentations existantes.</span><span class="sxs-lookup"><span data-stu-id="189bd-175">This approach should interoperate with existing implementations.</span></span>
* `RtpListener` <span data-ttu-id="189bd-176">n’est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-176">is not yet supported.</span></span> <span data-ttu-id="189bd-177">Cela signifie que les SSRCs (sources de flux et de synchronisation) doivent être spécifiées à l’avance dans le [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="189bd-177">This means that SSRCs (stream and synchronization sources) need to be specified in advance within the [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span>
* <span data-ttu-id="189bd-178">La bifurcation n’est pas encore prise en charge dans l’un ou l’autre `IceTransport` `IceGatherer` `DtlsTransport` .</span><span class="sxs-lookup"><span data-stu-id="189bd-178">Forking is not yet supported in either `IceTransport`, `IceGatherer`, or `DtlsTransport`.</span></span> <span data-ttu-id="189bd-179">La solution à la `DtlsTransport` bifurcation est toujours située en discussion dans le groupe de la communauté ORTC.</span><span class="sxs-lookup"><span data-stu-id="189bd-179">The solution to `DtlsTransport` forking is still under discussion in the ORTC Community Group.</span></span>
* <span data-ttu-id="189bd-180">Le protocole RTP/RTCP n' `DtlsTransport` est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-180">RTP/RTCP non-mux with `DtlsTransport` is not yet supported.</span></span> <span data-ttu-id="189bd-181">Lorsque vous utilisez `DtlsTransport` votre application, vous devez prendre en charge RTP/RTCP Mux.</span><span class="sxs-lookup"><span data-stu-id="189bd-181">When using `DtlsTransport` your application will need to support RTP/RTCP mux.</span></span>
* <span data-ttu-id="189bd-182">Dans le cadre de l’utilisation de [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) Microsoft Edge, vous ignorez actuellement la plupart des contrôles de qualité d’encodage, mais vous avez besoin de définir les attributs «actif» et «ssrc».</span><span class="sxs-lookup"><span data-stu-id="189bd-182">In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx), Microsoft Edge currently ignores most of the encoding quality controls, but does require setting the 'active' and 'ssrc' attributes.</span></span>
* <span data-ttu-id="189bd-183">L' `icecandidatepairchanged` événement n’est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="189bd-183">The `icecandidatepairchanged` event is not yet supported.</span></span> <span data-ttu-id="189bd-184">Vous pouvez extraire les informations sur les paires de candidat par le biais de la [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) méthode.</span><span class="sxs-lookup"><span data-stu-id="189bd-184">You can extract the candidate pair information through the [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) method.</span></span>
* <span data-ttu-id="189bd-185">Pour le moment, Microsoft Edge ne prend en charge aucune des `DataChannel` fonctionnalités actuellement définies dans la spécification ORTC.</span><span class="sxs-lookup"><span data-stu-id="189bd-185">Microsoft Edge currently does not support any of the `DataChannel` functionality currently defined in the ORTC spec.</span></span>

#### <span data-ttu-id="189bd-186">Avance</span><span class="sxs-lookup"><span data-stu-id="189bd-186">Looking forward</span></span>

<span data-ttu-id="189bd-187">Le déploiement de Microsoft Edge est toujours anticipé, car la fonctionnalité définie pour continuera de s’agrandir dans les prochains mois.</span><span class="sxs-lookup"><span data-stu-id="189bd-187">Microsoft Edge implementation is still early, expect the feature set to continue to grow in the coming months.</span></span> <span data-ttu-id="189bd-188">L’objectif de la mise en œuvre de Microsoft Edge est d’interopérabilité sur le Web dès aujourd’hui et de communiquer en temps réel sur le long terme.</span><span class="sxs-lookup"><span data-stu-id="189bd-188">The goal for Microsoft Edge implementation is interoperability across the web today as well as with the real-time communications industry in the long term.</span></span>



## <span data-ttu-id="189bd-189">Référence API</span><span class="sxs-lookup"><span data-stu-id="189bd-189">API reference</span></span>

[<span data-ttu-id="189bd-190">ORTC (Object Real-Time communications)</span><span class="sxs-lookup"><span data-stu-id="189bd-190">ORTC (Object Real-Time Communications)</span></span>](https://msdn.microsoft.com/library/Mt433097)

## <span data-ttu-id="189bd-191">Démos</span><span class="sxs-lookup"><span data-stu-id="189bd-191">Demos</span></span>

[<span data-ttu-id="189bd-192">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="189bd-192">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[<span data-ttu-id="189bd-193">Appel téléphonique ORTC</span><span class="sxs-lookup"><span data-stu-id="189bd-193">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[<span data-ttu-id="189bd-194">Démonstration ORTC</span><span class="sxs-lookup"><span data-stu-id="189bd-194">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## <span data-ttu-id="189bd-195">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="189bd-195">Related topics</span></span>

[<span data-ttu-id="189bd-196">L’API ORTC est désormais disponible dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="189bd-196">ORTC API is now available in Microsoft Edge</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[<span data-ttu-id="189bd-197">SimpleWebRTC: utilisez l’API ORTC de Microsoft Edge et les API WebRTC dans chrome et Firefox pour effectuer des conférences téléphoniques par navigateur.</span><span class="sxs-lookup"><span data-stu-id="189bd-197">SimpleWebRTC: Use Microsoft Edge's ORTC API and the WebRTC APIs in Chrome and Firefox to make cross-browser conference calls.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[<span data-ttu-id="189bd-198">Des expériences de communication transparentes pour le Web avec Skype, Skype entreprise et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="189bd-198">Enabling Seamless Communication Experiences for the Web with Skype, Skype for Business, and Microsoft Edge.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[<span data-ttu-id="189bd-199">GROUPE DE LA COMMUNAUTÉ ORTC (OBJECT REAL-TIME COMMUNICATIONS)</span><span class="sxs-lookup"><span data-stu-id="189bd-199">ORTC (OBJECT REAL-TIME COMMUNICATIONS) COMMUNITY GROUP</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## <span data-ttu-id="189bd-200">Spécifier</span><span class="sxs-lookup"><span data-stu-id="189bd-200">Specification</span></span>

[<span data-ttu-id="189bd-201">API W3C Object RTC (ORTC) pour WebRTC</span><span class="sxs-lookup"><span data-stu-id="189bd-201">W3C Object RTC (ORTC) API for WebRTC</span></span>](http://draft.ortc.org/)  
