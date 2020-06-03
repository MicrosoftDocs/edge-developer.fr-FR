---
description: Cette page fournit une vue d’ensemble des nouveautés de EdgeHTML 12.
title: Nouveautés de EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: f16db0551d4bea3d29b974c2a35fff2adf476c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564688"
---
# <span data-ttu-id="abc7c-104">Nouveautés de EdgeHTML 12</span><span class="sxs-lookup"><span data-stu-id="abc7c-104">What's New in EdgeHTML 12</span></span>

<span data-ttu-id="abc7c-105">Microsoft Edge présente EdgeHTML, un nouveau moteur «vivant» conçu pour une interopérabilité à son cœur, afin de vous assurer que vous avez toujours accès à la version la plus récente de la plateforme Windows Web.</span><span class="sxs-lookup"><span data-stu-id="abc7c-105">Microsoft Edge introduces EdgeHTML, a new "living" engine designed with interoperability at its core, to ensure that you are always getting the latest and greatest Windows web platform.</span></span> <span data-ttu-id="abc7c-106">Microsoft Edge est un saut de nouvelle version, disponible à partir du code hérité requis pour prendre en charge les contrôles ActiveX, les objets d’assistance du navigateur (BHO) et d’autres pratiques de développement Web Bygone.</span><span class="sxs-lookup"><span data-stu-id="abc7c-106">Microsoft Edge presents a clean break from the past, free from the legacy code needed to support ActiveX controls, Browser Helper Objects (BHOs), and other bygone web development practices.</span></span> <span data-ttu-id="abc7c-107">Par ailleurs, Microsoft Edge fournit une prise en charge native PDF.</span><span class="sxs-lookup"><span data-stu-id="abc7c-107">Additionally, Microsoft Edge provides native PDF support.</span></span> <span data-ttu-id="abc7c-108">À partir de IE11, les modes de document hérités ont été déconseillés, et avec Microsoft Edge, l’infrastructure de navigateur pour les prendre en charge n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="abc7c-108">As of IE11, legacy document modes have been deprecated, and with Microsoft Edge, the browser infrastructure to support them does not exist.</span></span> <span data-ttu-id="abc7c-109">Pour plus d’informations, consultez [IEBlog](https://go.microsoft.com/fwlink/p/?LinkID=519011) .</span><span class="sxs-lookup"><span data-stu-id="abc7c-109">Check out the [IEBlog](https://go.microsoft.com/fwlink/p/?LinkID=519011) for more info.</span></span>

<span data-ttu-id="abc7c-110">Voici les modifications envoyées avec EdgeHTML 12 dans la version initiale de [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) (07/2015, Build 10240).</span><span class="sxs-lookup"><span data-stu-id="abc7c-110">Here are the changes shipped with EdgeHTML 12 in the initial release of [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) (07/2015, Build 10240).</span></span> <span data-ttu-id="abc7c-111">Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir [une pause dans le passé: la naissance du nouveau moteur de rendu Web de Microsoft](https://blogs.windows.com/msedgedev/2015/02/26/a-break-from-the-past-the-birth-of-microsofts-new-web-rendering-engine/) et [un saut passé par le passé, 2e partie: dire adieu aux contrôles ActiveX, VBScript et AttachEvent...](https://blogs.windows.com/msedgedev/2015/05/06/a-break-from-the-past-part-2-saying-goodbye-to-activex-vbscript-attachevent/).</span><span class="sxs-lookup"><span data-stu-id="abc7c-111">For an overview of changes to the overall Microsoft Edge browser, see [A break from the past: the birth of Microsoft's new web rendering engine](https://blogs.windows.com/msedgedev/2015/02/26/a-break-from-the-past-the-birth-of-microsofts-new-web-rendering-engine/) and [A break from the past, part 2: Saying goodbye to ActiveX, VBScript, attachEvent...](https://blogs.windows.com/msedgedev/2015/05/06/a-break-from-the-past-part-2-saying-goodbye-to-activex-vbscript-attachevent/).</span></span>

<span data-ttu-id="abc7c-112">Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante: [https://aka.ms/devguide_edgehtml_12](https://aka.ms/devguide_edgehtml_12) .</span><span class="sxs-lookup"><span data-stu-id="abc7c-112">Here's the permalink for the following list of changes: [https://aka.ms/devguide_edgehtml_12](https://aka.ms/devguide_edgehtml_12).</span></span>


## <span data-ttu-id="abc7c-113">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="abc7c-113">New Features</span></span>

### <span data-ttu-id="abc7c-114">Politique de sécurité du contenu 1,0</span><span class="sxs-lookup"><span data-stu-id="abc7c-114">Content Security Policy 1.0</span></span>
<span data-ttu-id="abc7c-115">Microsoft Edge implémente désormais le 1,0 de stratégie de sécurité du contenu (CSP).</span><span class="sxs-lookup"><span data-stu-id="abc7c-115">Microsoft Edge now implements Content Security Policy (CSP) 1.0.</span></span> <span data-ttu-id="abc7c-116">La norme de sécurité du fournisseur de services cryptographiques permet aux développeurs Web de contrôler les ressources (script, CSS, plug-ins, images, etc.) qu’une page particulière peut récupérer ou exécuter dans le cadre de la prévention de l’exécution de scripts entre sites (XSS), Clickjacking et d’autres attaques par injection de code dans le contexte d’une page Web fiable.</span><span class="sxs-lookup"><span data-stu-id="abc7c-116">The CSP security standard enables web developers to control the resources (script, CSS, plugins, images, etc.) which a particular page can fetch or execute with the aim of preventing cross-site scripting (XSS), clickjacking, and other code injection attacks seeking to execute malicious content in the context of a trusted web page.</span></span> <span data-ttu-id="abc7c-117">Pour plus d’informations sur les fournisseurs de services cryptographiques dans Microsoft Edge, voir [stratégie de sécurité du contenu](https://docs.microsoft.com/microsoft-edge/dev-guide/security/content-security-policy) .</span><span class="sxs-lookup"><span data-stu-id="abc7c-117">Check out [Content Security Policy](https://docs.microsoft.com/microsoft-edge/dev-guide/security/content-security-policy) for more information about CSP in Microsoft Edge.</span></span> 

### <span data-ttu-id="abc7c-118">Effets de filtre</span><span class="sxs-lookup"><span data-stu-id="abc7c-118">Filter Effects</span></span>
<span data-ttu-id="abc7c-119">Microsoft Edge fournit un moyen facile d’ajouter des effets visuels aux éléments.</span><span class="sxs-lookup"><span data-stu-id="abc7c-119">Microsoft Edge provides an easy way to add visual effects to elements.</span></span> <span data-ttu-id="abc7c-120">À l’aide de la `filter` propriété, vous pouvez ajouter des flous, ajuster la luminosité, ajouter une ombre portée, modifier l’opacité, etc.</span><span class="sxs-lookup"><span data-stu-id="abc7c-120">Using the `filter` property you can add blurs, adjust the brightness, add a drop shadow, change the opacity, and more to an element.</span></span> <span data-ttu-id="abc7c-121">À l’aide d’une feuille de style CSS uniquement, vous pouvez appliquer plusieurs effets de filtre à un élément et animer les filtres.</span><span class="sxs-lookup"><span data-stu-id="abc7c-121">Using purely CSS, you can apply multiple filter effects to one element and animate the filters.</span></span> <span data-ttu-id="abc7c-122">Pour plus d’informations, voir [effets de filtre](https://docs.microsoft.com/microsoft-edge/dev-guide/css/filter-effects).</span><span class="sxs-lookup"><span data-stu-id="abc7c-122">For more information, see [Filter effects](https://docs.microsoft.com/microsoft-edge/dev-guide/css/filter-effects).</span></span>

### <span data-ttu-id="abc7c-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="abc7c-123">JavaScript</span></span>
<span data-ttu-id="abc7c-124">La prise en charge de JavaScript varie légèrement entre la version finale d’Internet Explorer (IE11) et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abc7c-124">JavaScript support varies slightly between the final version of Internet Explorer (IE11) and Microsoft Edge.</span></span> <span data-ttu-id="abc7c-125">Les nouvelles fonctionnalités de Microsoft Edge sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="abc7c-125">New features in Edge include:</span></span>

| | |
|--|--|
|**<span data-ttu-id="abc7c-126">Relevés</span><span class="sxs-lookup"><span data-stu-id="abc7c-126">Statements</span></span>**| <span data-ttu-id="abc7c-127">[Class](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) (expérimental), [pour... de](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of)</span><span class="sxs-lookup"><span data-stu-id="abc7c-127">[class](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) (experimental), [for...of](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of)</span></span> |
|**<span data-ttu-id="abc7c-128">Objets</span><span class="sxs-lookup"><span data-stu-id="abc7c-128">Objects</span></span>**| <span data-ttu-id="abc7c-129">[Promesse](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [symbole](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [WeakSet](/scripting/javascript/reference/weakset-object-javascript)</span><span class="sxs-lookup"><span data-stu-id="abc7c-129">[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [Proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [Symbol](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [WeakSet](/scripting/javascript/reference/weakset-object-javascript)</span></span> |
|**<span data-ttu-id="abc7c-130">Fonctions</span><span class="sxs-lookup"><span data-stu-id="abc7c-130">Functions</span></span>** | <span data-ttu-id="abc7c-131">[acosh](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [IsNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [RAW](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)</span><span class="sxs-lookup"><span data-stu-id="abc7c-131">[acosh](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [isNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [raw](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)</span></span> |
|**<span data-ttu-id="abc7c-132">Méthodes</span><span class="sxs-lookup"><span data-stu-id="abc7c-132">Methods</span></span>**| <span data-ttu-id="abc7c-133">[inclut](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [Keys](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) (matrice), [REPEAT](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) (chaîne), [valeurs](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) (matrice)</span><span class="sxs-lookup"><span data-stu-id="abc7c-133">[includes](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [keys](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) (Array), [repeat](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) (String), [values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) (Array)</span></span> |
|**<span data-ttu-id="abc7c-134">Autres fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="abc7c-134">Other features</span></span>**| <span data-ttu-id="abc7c-135">[Fonctions](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) (expérimentaux), [générateurs](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [itérateurs](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [ `y` indicateur d’expression régulière](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) (expérimental), [chaînes de modèle](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), caractères d’échappement de point de [code Unicode](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals)</span><span class="sxs-lookup"><span data-stu-id="abc7c-135">[Functions](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) (experimental), [Generators](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators),  [Iterators](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [Regular Expression `y` flag](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) (experimental), [Template strings](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), [Unicode code point escape characters](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals)</span></span> |

<span data-ttu-id="abc7c-136">Pour en savoir plus sur la prise en charge JavaScript entre les applications Internet Explorer, Microsoft Edge et Microsoft Store, voir [*informations sur la version JavaScript*](./javascript-version-information.md).</span><span class="sxs-lookup"><span data-stu-id="abc7c-136">For a comparison of JavaScript support across Internet Explorer, Microsoft Edge, and Microsoft Store apps, see [*JavaScript Version Information*](./javascript-version-information.md).</span></span>

### <span data-ttu-id="abc7c-137">Capture multimédia et flux</span><span class="sxs-lookup"><span data-stu-id="abc7c-137">Media Capture and Streams</span></span>
<span data-ttu-id="abc7c-138">Microsoft Edge présente la prise en charge des API de capture multimédia et de flux, en fonction de la spécification de [capture et de flux de média W3C](https://go.microsoft.com/fwlink/p/?LinkID=534096) .</span><span class="sxs-lookup"><span data-stu-id="abc7c-138">Microsoft Edge introduces support for the Media Capture and Streams APIs based on the [W3C Media Capture and Streams](https://go.microsoft.com/fwlink/p/?LinkID=534096) specification.</span></span> <span data-ttu-id="abc7c-139">Ces API JavaScript permettent aux pages Web d’accéder aux périphériques de capture multimédias, tels que des webcams ou des microphones, avec l’autorisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abc7c-139">These JavaScript APIs allow webpages to access media capture devices, like webcams or microphones, with permission from the user.</span></span> <span data-ttu-id="abc7c-140">À l’aide des API de capture multimédia et de flux, vous pouvez créer des scénarios comme la capture d’une photo à l’aide d’une webcam ou la capture d’un message vocal à partir d’un micro.</span><span class="sxs-lookup"><span data-stu-id="abc7c-140">By using the Media Capture and Streams APIs, you can create scenarios like capturing a photo using a webcam or capturing a voice message from a microphone.</span></span> <span data-ttu-id="abc7c-141">Pour en savoir plus sur la capture multimédia dans Microsoft Edge, consultez le [blog du développeur Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/13/announcing-media-capture-functionality-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="abc7c-141">Read more about Media Capture in Microsoft Edge on the [Microsoft Edge Developer blog](https://blogs.windows.com/msedgedev/2015/05/13/announcing-media-capture-functionality-in-microsoft-edge/).</span></span> 

### <span data-ttu-id="abc7c-142">Nouvel élément HTML et attributs</span><span class="sxs-lookup"><span data-stu-id="abc7c-142">New HTML element and attributes</span></span>
* `meter` <span data-ttu-id="abc7c-143">élément</span><span class="sxs-lookup"><span data-stu-id="abc7c-143">element</span></span>
* `picture` <span data-ttu-id="abc7c-144">élément</span><span class="sxs-lookup"><span data-stu-id="abc7c-144">element</span></span>
* `template` <span data-ttu-id="abc7c-145">élément</span><span class="sxs-lookup"><span data-stu-id="abc7c-145">element</span></span>
* `image` <span data-ttu-id="abc7c-146">élément: `srcset` et `sizes` attributs ( [billet de blog](https://blogs.windows.com/msedgedev/2015/06/08/introducing-srcset-responsive-images-in-microsoft-edge/)du développeur Microsoft Edge)</span><span class="sxs-lookup"><span data-stu-id="abc7c-146">element: `srcset` and `sizes` attributes (Microsoft Edge Developer [blog post](https://blogs.windows.com/msedgedev/2015/06/08/introducing-srcset-responsive-images-in-microsoft-edge/))</span></span>
* `selectionDirection` <span data-ttu-id="abc7c-147">attribut</span><span class="sxs-lookup"><span data-stu-id="abc7c-147">attribute</span></span>
* `input type=time` <span data-ttu-id="abc7c-148">et</span><span class="sxs-lookup"><span data-stu-id="abc7c-148">and</span></span> `input type=datetime-local`

### <span data-ttu-id="abc7c-149">API RTC Object</span><span class="sxs-lookup"><span data-stu-id="abc7c-149">Object RTC API</span></span> 
<span data-ttu-id="abc7c-150">Les communications en temps réel entre objets (ORTC) permettent le lecture de contenu multimédia (audio et/ou vidéo) en temps réel entre les navigateurs Web, les appareils mobiles et les serveurs par le biais des API JavaScript natives.</span><span class="sxs-lookup"><span data-stu-id="abc7c-150">Object Real-Time Communications (ORTC) enables media (audio and/or video) to be streamed (sent and received) in real-time directly between web browsers, mobile devices, and servers via native JavaScript APIs.</span></span> <span data-ttu-id="abc7c-151">Pour plus d’informations sur la validation de l’utilisation de la mise en route dans Microsoft Edge, voir [objet](https://docs.microsoft.com/microsoft-edge/dev-guide/realtime-communication/object-rtc-api) sujet du Guide de développement.</span><span class="sxs-lookup"><span data-stu-id="abc7c-151">Check out the Dev guide topic [Object RTC API](https://docs.microsoft.com/microsoft-edge/dev-guide/realtime-communication/object-rtc-api) for more information about ORTC in Microsoft Edge.</span></span> 

### <span data-ttu-id="abc7c-152">Mode lecture</span><span class="sxs-lookup"><span data-stu-id="abc7c-152">Reading View</span></span>
<span data-ttu-id="abc7c-153">Microsoft Edge fournit un mode lecture pour une connaissance plus rationalisée et plus agréable de la lecture de pages Web, sans la distraction de contenus non liés ou secondaires sur la page.</span><span class="sxs-lookup"><span data-stu-id="abc7c-153">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span> <span data-ttu-id="abc7c-154">Le mode lecture peut être activé ou désactivé à l’aide du bouton mode lecture (icône du livre) de la barre d’adresse (ou de Ctrl + Maj + R).</span><span class="sxs-lookup"><span data-stu-id="abc7c-154">Reading view can be toggled on or off from the Reading view (book icon) button on the address bar (or with Ctrl + Shift + R).</span></span> <span data-ttu-id="abc7c-155">Pour plus d’informations, consultez le [mode lecture](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/reading-view) .</span><span class="sxs-lookup"><span data-stu-id="abc7c-155">Visit [Reading view](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/reading-view) for more information.</span></span> 

### <span data-ttu-id="abc7c-156">Découverte du fournisseur de recherche</span><span class="sxs-lookup"><span data-stu-id="abc7c-156">Search provider discovery</span></span>
<span data-ttu-id="abc7c-157">L’intégration de recherche complète est intégrée à la barre d’adresses Microsoft Edge, y compris aux suggestions de recherche, aux résultats provenant du Web, à votre historique de navigation et aux favoris.</span><span class="sxs-lookup"><span data-stu-id="abc7c-157">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span> <span data-ttu-id="abc7c-158">Microsoft Edge suit la spécification [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) pour découvrir et utiliser les fournisseurs de recherche Web.</span><span class="sxs-lookup"><span data-stu-id="abc7c-158">Microsoft Edge follows the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification to discover and use web search providers.</span></span> <span data-ttu-id="abc7c-159">Si vous êtes un fournisseur de recherche, [en savoir plus](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/search-provider-discovery) sur la façon de s’assurer que Microsoft Edge prend en charge votre service.</span><span class="sxs-lookup"><span data-stu-id="abc7c-159">If you are a search provider, [read more](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/search-provider-discovery) about how to ensure that Microsoft Edge supports your service.</span></span> 

### <span data-ttu-id="abc7c-160">Prise en charge des API WebKit</span><span class="sxs-lookup"><span data-stu-id="abc7c-160">Support for WebKit APIs</span></span>
<span data-ttu-id="abc7c-161">Pour une meilleure compatibilité, Microsoft Edge prend en charge une variété d’API préréglées «-WebKit-».</span><span class="sxs-lookup"><span data-stu-id="abc7c-161">For improved compatibility, Microsoft Edge supports a variety of "-webkit-" prefixed APIs.</span></span> <span data-ttu-id="abc7c-162">Pour obtenir la liste complète des API «-WebKit-» prises en charge, utilisez le [catalogue API](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).</span><span class="sxs-lookup"><span data-stu-id="abc7c-162">For a full list of supported "-webkit-" APIs, use the [API Catalog](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).</span></span>

### <span data-ttu-id="abc7c-163">Audio Web</span><span class="sxs-lookup"><span data-stu-id="abc7c-163">Web Audio</span></span>
<span data-ttu-id="abc7c-164">Microsoft Edge présente la prise en charge de la spécification de l' [API audio Web W3C](https://go.microsoft.com/fwlink/p/?LinkID=512167) .</span><span class="sxs-lookup"><span data-stu-id="abc7c-164">Microsoft Edge introduces support for the [W3C Web Audio API](https://go.microsoft.com/fwlink/p/?LinkID=512167) specification.</span></span> <span data-ttu-id="abc7c-165">Le son Web est une API JavaScript de haut niveau permettant de traiter et de synthétiser du son dans les applications Web pour fournir des expériences audio et musicales plus riches.</span><span class="sxs-lookup"><span data-stu-id="abc7c-165">Web Audio is a high-level JavaScript API for processing and synthesizing audio in web applications to provide rich audio and music experiences.</span></span> <span data-ttu-id="abc7c-166">Bien que l' `audio` élément HTML5 autorise la lecture de contenu audio en continu de base, l’API audio Web fournit une gamme d’API qui vous permettent de lire des sons multiples avec une synchronisation rapprochée et d’appliquer des gains, des fondus, des transitions et des effets de base sur le son mélangé.</span><span class="sxs-lookup"><span data-stu-id="abc7c-166">While the HTML5 `audio` element allows for basic streaming audio playback, Web Audio API provides a range of APIs that allow you to play multiple sounds with tight synchronization, and apply gain, fades, transitions, and basic effects on mixed audio.</span></span> <span data-ttu-id="abc7c-167">En savoir plus sur le [son Web](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-audio) dans le Guide de développement et sur le [blog du développeur Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/19/bringing-web-audio-to-microsoft-edge-for-interoperable-gaming-and-enthusiast-media/).</span><span class="sxs-lookup"><span data-stu-id="abc7c-167">Read more about [Web Audio](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-audio) in the Dev guide and on the [Microsoft Edge Developer blog](https://blogs.windows.com/msedgedev/2015/05/19/bringing-web-audio-to-microsoft-edge-for-interoperable-gaming-and-enthusiast-media/).</span></span> 

### <span data-ttu-id="abc7c-168">Pilote Web</span><span class="sxs-lookup"><span data-stu-id="abc7c-168">Web Driver</span></span> 
<span data-ttu-id="abc7c-169">L' [API WebDriver W3C](https://w3.org/TR/webdriver/) est une plate-forme et un protocole filaire qui autorisent des programmes ou des scripts à contrôler le comportement d’un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="abc7c-169">The [W3C WebDriver API](https://w3.org/TR/webdriver/) is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser.</span></span> <span data-ttu-id="abc7c-170">Le WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abc7c-170">WebDriver enables developers to create automated tests that simulate user interaction.</span></span> <span data-ttu-id="abc7c-171">Cette fonction est différente de celle des tests unitaires JavaScript, car le WebDriver a accès aux fonctionnalités et aux informations que JavaScript en cours d’exécution dans le navigateur ne permet pas de simuler plus précisément les événements utilisateur ou au niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="abc7c-171">This is different from JavaScript unit tests because WebDriver has access to functionality and information that JavaScript running in the browser doesn't, and it can more accurately simulate user events or OS-level events.</span></span> <span data-ttu-id="abc7c-172">Le Web Driver peut également gérer des tests sur plusieurs fenêtres, des onglets et des pages Web au sein d’une seule et même session de test.</span><span class="sxs-lookup"><span data-stu-id="abc7c-172">WebDriver can also manage testing across multiple windows, tabs and webpages in a single test session.</span></span>  <span data-ttu-id="abc7c-173">Pour plus d’informations sur la manière de prendre en main le WebDriver pour Microsoft Edge, consultez le [WebDriver](https://docs.microsoft.com/microsoft-edge/dev-guide/tools/webdriver).</span><span class="sxs-lookup"><span data-stu-id="abc7c-173">For more information on how to get started with WebDriver for Microsoft Edge, check out [WebDriver](https://docs.microsoft.com/microsoft-edge/dev-guide/tools/webdriver).</span></span> 


## <span data-ttu-id="abc7c-174">Nouvelles API dans EdgeHTML 12</span><span class="sxs-lookup"><span data-stu-id="abc7c-174">New APIs in EdgeHTML 12</span></span>

<span data-ttu-id="abc7c-175">Voici la liste complète des nouvelles API dans EdgeHTML 12.</span><span class="sxs-lookup"><span data-stu-id="abc7c-175">Here's the full list of new APIs in EdgeHTML 12.</span></span>  <span data-ttu-id="abc7c-176">Ils sont répertoriés au format **[nom de l’interface]. [ nom de l’API]**.</span><span class="sxs-lookup"><span data-stu-id="abc7c-176">They are listed in the format of **[interface name].[api name]**.</span></span>

 > [!NOTE] 
 > <span data-ttu-id="abc7c-177">Bon nombre de ces API étaient disponibles dans IE11.</span><span class="sxs-lookup"><span data-stu-id="abc7c-177">Many of these APIs were available in IE11.</span></span> <span data-ttu-id="abc7c-178">Les données suivantes pour EdgeHTML 12 sont proposées comme référence pour comparer la version initiale de EdgeHTML aux versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="abc7c-178">The data below for EdgeHTML 12 is offered as a baseline for comparing the initial version of EdgeHTML to later versions.</span></span>

<iframe height='580' scrolling='no' title='<span data-ttu-id="abc7c-179">Nouvelles API dans EdgeHTML 12</span><span class="sxs-lookup"><span data-stu-id="abc7c-179">New APIs in EdgeHTML 12</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="abc7c-180">Reportez-vous au stylo <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> nouvelles API dans EdgeHTML 12 </a> par docs Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="abc7c-180">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'>New APIs in EdgeHTML 12</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>