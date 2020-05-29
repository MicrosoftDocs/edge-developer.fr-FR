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
# API RTC Object

Les communications en temps réel entre objets (ORTC) permettent le lecture de contenu multimédia (audio et/ou vidéo) en temps réel entre les navigateurs Web, les appareils mobiles et les serveurs par le biais des API JavaScript natives.

> [!NOTE]
> Microsoft Edge implémente désormais le ORTC pour les appareils Windows 10. Toutefois, cette implémentation diffère de la version la plus récente de l' [API ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096). La norme ORTC a continué d’évoluer depuis le développement et la publication de Microsoft Edge: le navigateur n’implémente pas chaque objet ou méthode au sein de l’API ORTC et inclut des extensions qui ne sont pas actuellement incorporées dans la spécification. D’autres développements seront poursuivis pour permettre aux développeurs de tout le monde de créer des expériences qui incluent la possibilité de parler aux utilisateurs de Skype et aux services de communication compatibles WebRTC.



Pour bénéficier d’une expérience pratique avec la fonction ORTC, testez ces démonstrations sur le lecteur:
-  [SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [Appel téléphonique ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [Démonstration ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


Pour plus d’informations sur la fonction ORTC, voir l' [API ORTC est désormais disponible dans Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) sur le blog du développement Microsoft Edge.


## Diagramme de vue d’ensemble


Le diagramme ci-dessous fournit un récapitulatif des relations entre les objets ORTC. Les flèches horizontales ou inclinées indiquent le flux de média ou de données, alors que les flèches verticales indiquent les interactions par le biais de méthodes et d’événements.

La fonction ORTC utilise les objets «*sender*», «*Receiver*» et «*transport*», qui ont des «*fonctionnalités*» qui décrivent ce qu’ils sont en mesure d’effectuer, ainsi que des «*paramètres*» définissant ce qu’ils sont configurés. «*Pistes*» capturez et encodez les flux multimédias par les expéditeurs, en circulant sur les transports, puis décodés par des récepteurs qui effectuent le rendu des pistes du flux multimédia pour les balises vidéo/audio.

![Diagramme de flux Microsoft Edge ORTC ](./../media/ortc_diagram.png) dans l’illustration ci-dessus, le [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) code effectue le suivi fourni en entrée, qui est transporté sur une [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) ou une [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) . L’envoi de tonalités DTMF (Dual-tonalité multifréquence) est pris en charge par le biais de [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .

La [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) et [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilise une [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) pour sélectionner une voie de communication pour joindre l’homologue de réception `RTCIceTransport` , qui est à son tour associé à un `RTCDtlsTransport` ou `RTCSrtpSdesTransport` de ces éléments [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) . Le `RTCRtpReceiver` code multimédia, puis décode, génère une piste rendue par une balise audio ou vidéo.

Plusieurs autres objets jouent également un rôle. Le [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) rassemblement de candidatures de glace locales pour une utilisation par un seul [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) objet. Les sections restantes de l’API remplissent des détails relatifs aux *fonctionnalités* et *paramètres*RTP, aux *statistiques opérationnelles* et à la compatibilité avec l' [API 1,0 WebRTC](https://go.microsoft.com/fwlink/p/?LinkID=627573).

> [!NOTE]
> Dans la mesure où Microsoft Edge n’implémente pas le canal de données, les `RTCDataChannel` objets et ne `RTCSctpTransport` sont pas pris en charge.




## Composants pris en charge dans l’implémentation initiale de Microsoft Edge


* **Prise en charge de l’API ORTC.** Les communications audio/vidéo sont le principal foyer, y compris les objets suivants:,,,, ainsi que [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) les [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces qui ne s’affichent pas directement dans le diagramme.
* **Prise en charge du multiplexage RTP/RTCP.** [`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)est requis pour l’utilisation de [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) . Le multiplexage a/V est également pris en charge.
* **Support STUN/TURN/ICE.** STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) et Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621)sont pris en charge. Dans le cadre de la glace, la dénomination normale est prise en charge, avec une désignation agressive entièrement prise en charge (en tant que destinataire). DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) est pris en charge en fonction de DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).
* **Prise en charge du codec.** Pour les [codecs audio](https://msdn.microsoft.com/library/Mt599587), nous prenons en charge g. 711, g. 722, opus et soie. Nous prenons également en charge les bruits de confort (CN) et DTMF en fonction de la configuration audio RTCWEB. Pour la vidéo, le codec utilisé par les services Skype est actuellement pris en charge [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) , à l’aide des fonctionnalités avancées telles que la simultanéité, le codage vidéo évolutif et la correction des erreurs de transfert. Nous travaillons à l’activation de la vidéo interopérable avec H. 264.

> [!NOTE]
> Si vous connaissez les implémentations de WebRTC 1,0 et que vous êtes intéressé par l’évolution de la prise en charge des objets dans WebRTC 1,0 et ORTC, nous recommandons la présentation suivante par Google, Microsoft et Hookflash à partir de la Conférence 2014 IIT RTC: «[mise à jour d’API ORTC](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)».




## Flux de code de niveau application pour les communications 1:1


Pour ce scénario, deux ordinateurs Windows 10 font office de deux homologues avec un serveur WebServer comme canal de signalisation pour échanger des informations entre les homologues afin qu’une connexion puisse être établie entre eux.

Les étapes ci-dessous sont limitées aux opérations effectuées par un homologue. Les deux homologues doivent suivre les étapes ci-dessous afin de configurer les communications 1:1. Pour plus d’informations sur les extraits de code ci-dessous, reportez-vous à la [démonstration Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635).

Cet exemple utilise le multiplexage audio-vidéo et RTP/RTCP, de sorte que vous ne voyez qu’un seul transport de glace et de DTLS, utilisé pour transporter les paquets RTP et RTCP pour les appels audio et vidéo.

`Step #1.` Créer [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) un objet (par exemple [, API de capture multimédia et de flux](./../multimedia/media-Capture-and-Streams.md)) avec une piste audio et une piste vidéo.

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

`Step #2.` Créez le [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) et activez local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) pour être signalé au pair distant.

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

Pour vous aider à protéger la vie privée de l’utilisateur, Microsoft Edge introduit une option qui permet à un utilisateur de contrôler si les adresses IP d’hôte local peuvent être exposées par les [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objets. Une option d’interface sera fournie pour activer ou désactiver ce paramètre.

Dans la [démonstration Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635), un serveur Turn a été configuré. Le débit du serveur est très limité et ne peut être utilisé que sur la page de démonstration.

`Step #3.` Créez le [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) périphérique audio et vidéo et préparez-vous à gérer [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) la télécommande sur le transport de glace.

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

Une autre option consiste à accumuler tous les candidats à distance de glace dans un tableau `remoteCandidates` et `iceTr.setRemoteCandidates(remoteCandidates)` à appeler pour ajouter tous les candidats distants.

`Step #4.` Créez le transport DTLS.

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` Créez les objets expéditeur et destinataire.

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

Étape #6. Récupérer les fonctionnalités du destinataire et de l’expéditeur.

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` Les paramètres de glace/DTLS et les fonctionnalités d’envoi et de réception peuvent être échangés.

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

`Step #8.` Obtenez les paramètres distants, démarrez le [`ICE`](https://msdn.microsoft.com/library/Mt433112) et [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, puis définissez les paramètres d’envoi et de réception audio et vidéo.

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

Vous trouverez ci-dessous une structure des fonctions d’assistance. Pour plus d’informations, consultez la [démonstration Microsoft Edge test](https://go.microsoft.com/fwlink/p/?LinkID=627635).

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

`Step #9.` Afficher et lire le flux multimédia distant effectue le suivi d’une balise vidéo.

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

Dès lors que vous avez configuré les appels 1:1, appliquez les mêmes principes pour configurer les appels de groupe de petite taille à l’aide d’une topologie de maille, où chaque homologue aura une connexion 1:1 avec le reste du groupe. Dans la mesure où la fonction de bifurcation parallèle n’est pas prise en charge sur la plateforme Microsoft Edge, cela doit être géré par le biais de la signalisation 1:1 de sorte que les [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objets indépendants et puissent [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) être utilisés pour chaque connexion.

## Détails de l’implémentation dans Microsoft Edge


La spécification ORTC est relativement stable dans la mesure où le groupe de la communauté de ORTC a émis les «appels pour les implémentations» et les défis importants liés au niveau de l’API JavaScript ne sont pas attendus. En fonction de ce qui suit, l’implémentation de Microsoft Edge a été publiée pour les tests d’interopérabilité entre les navigateurs au niveau du protocole.

Voici quelques limitations de l’implémentation de Microsoft Edge:

* `RTCIceTransportController` n’est pas pris en charge. L’implémentation de Microsoft Edge gère la congélation et l’incongélation de glace pour chaque transport, de telle sorte que la commande All `IceTransports` n’est pas nécessaire. Cette approche doit interopérer avec des implémentations existantes.
* `RtpListener` n’est pas encore pris en charge. Cela signifie que les SSRCs (sources de flux et de synchronisation) doivent être spécifiées à l’avance dans le [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .
* La bifurcation n’est pas encore prise en charge dans l’un ou l’autre `IceTransport` `IceGatherer` `DtlsTransport` . La solution à la `DtlsTransport` bifurcation est toujours située en discussion dans le groupe de la communauté ORTC.
* Le protocole RTP/RTCP n' `DtlsTransport` est pas encore pris en charge. Lorsque vous utilisez `DtlsTransport` votre application, vous devez prendre en charge RTP/RTCP Mux.
* Dans le cadre de l’utilisation de [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) Microsoft Edge, vous ignorez actuellement la plupart des contrôles de qualité d’encodage, mais vous avez besoin de définir les attributs «actif» et «ssrc».
* L' `icecandidatepairchanged` événement n’est pas encore pris en charge. Vous pouvez extraire les informations sur les paires de candidat par le biais de la [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) méthode.
* Pour le moment, Microsoft Edge ne prend en charge aucune des `DataChannel` fonctionnalités actuellement définies dans la spécification ORTC.

#### Avance

Le déploiement de Microsoft Edge est toujours anticipé, car la fonctionnalité définie pour continuera de s’agrandir dans les prochains mois. L’objectif de la mise en œuvre de Microsoft Edge est d’interopérabilité sur le Web dès aujourd’hui et de communiquer en temps réel sur le long terme.



## Référence API

[ORTC (Object Real-Time communications)](https://msdn.microsoft.com/library/Mt433097)

## Démos

[SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[Appel téléphonique ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[Démonstration ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## Rubriques connexes

[L’API ORTC est désormais disponible dans Microsoft Edge.](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[SimpleWebRTC: utilisez l’API ORTC de Microsoft Edge et les API WebRTC dans chrome et Firefox pour effectuer des conférences téléphoniques par navigateur.](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[Des expériences de communication transparentes pour le Web avec Skype, Skype entreprise et Microsoft Edge.](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[GROUPE DE LA COMMUNAUTÉ ORTC (OBJECT REAL-TIME COMMUNICATIONS)](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## Spécifier

[API W3C Object RTC (ORTC) pour WebRTC](http://draft.ortc.org/)  
