---
description: Cet article fournit de la documentation sur les conseils Microsoft Edge client de l’agent utilisateur et la chaîne de l’agent utilisateur
title: Comment détecter Microsoft Edge dans votre site web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilité, plateforme web, chaîne d’agent utilisateur, chaîne ua, substitutions ua, conseils client de l’agent utilisateur, conseils client de l’agent utilisateur, conseils de client ua, ua ch
ms.openlocfilehash: 1957bb5bd33d9d921d8a12e16a4a52a23836027b
ms.sourcegitcommit: e90bbc210b5d510004bbc2145d49e14fe72ed54b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2021
ms.locfileid: "11578777"
---
# <a name="how-to-detect-microsoft-edge-in-your-website"></a><span data-ttu-id="e2a38-104">Comment détecter Microsoft Edge dans votre site web</span><span class="sxs-lookup"><span data-stu-id="e2a38-104">How to detect Microsoft Edge in your website</span></span>  

<span data-ttu-id="e2a38-105">Les navigateurs fournissent des mécanismes permettant aux sites web de détecter les informations de navigateur telles que la marque et le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="e2a38-105">Browsers provide mechanisms for websites to detect browser information such as brand and version number.</span></span>  <span data-ttu-id="e2a38-106">Les mécanismes détectent également d’autres caractéristiques d’appareil telles que le système d’exploitation hôte.</span><span class="sxs-lookup"><span data-stu-id="e2a38-106">The mechanisms also detect other device characteristics like the host operating system.</span></span>  <span data-ttu-id="e2a38-107">Deux de ces mécanismes pris en charge sur Microsoft Edge sont les [conseils](#user-agent-client-hints) client de l’agent utilisateur et les chaînes [d’agent utilisateur](#user-agent-string).</span><span class="sxs-lookup"><span data-stu-id="e2a38-107">Two such mechanisms supported on Microsoft Edge are [User-Agent Client Hints](#user-agent-client-hints) and [User-Agent strings](#user-agent-string).</span></span>  <span data-ttu-id="e2a38-108">Après des années d’utilisation, User-Agent chaînes sont obsolètes et ont un long historique en tant que cause des problèmes de compatibilité des sites web.</span><span class="sxs-lookup"><span data-stu-id="e2a38-108">After decades of use, User-Agent strings are outdated and have a long history as the cause of website compatibility issues.</span></span>  <span data-ttu-id="e2a38-109">Au lieu de cela, l’équipe Microsoft Edge vous recommande d’utiliser un mécanisme amélioré pour récupérer les informations de navigateur [nommées User-Agent Client Hints](#user-agent-client-hints).</span><span class="sxs-lookup"><span data-stu-id="e2a38-109">Instead, the Microsoft Edge team recommends you use an improved mechanism to retrieve browser information named [User-Agent Client Hints](#user-agent-client-hints).</span></span>  <span data-ttu-id="e2a38-110">Cet article décrit les deux mécanismes Microsoft Edge pour la récupération des informations de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2a38-110">This article outlines the two mechanisms Microsoft Edge supports for retrieving user agent information.</span></span>  

|  | <span data-ttu-id="e2a38-111">Côté serveur</span><span class="sxs-lookup"><span data-stu-id="e2a38-111">Server-side</span></span> | <span data-ttu-id="e2a38-112">Côté client</span><span class="sxs-lookup"><span data-stu-id="e2a38-112">Client-side</span></span> |  
|:--- |:--- |:--- | 
| <span data-ttu-id="e2a38-113">**Conseils client de l’agent** utilisateur \(recommandé\)</span><span class="sxs-lookup"><span data-stu-id="e2a38-113">**User-Agent Client Hints** \(recommended\)</span></span> | `Sec-CH-UA` <span data-ttu-id="e2a38-114">En-tête HTTPS</span><span class="sxs-lookup"><span data-stu-id="e2a38-114">HTTPS header</span></span> | `navigator.userAgentData` <span data-ttu-id="e2a38-115">Méthode JavaScript</span><span class="sxs-lookup"><span data-stu-id="e2a38-115">JavaScript method</span></span> |  
| <span data-ttu-id="e2a38-116">**Chaîne user-Agent** \(legacy\)</span><span class="sxs-lookup"><span data-stu-id="e2a38-116">**User-Agent string** \(legacy\)</span></span> | `User-Agent` <span data-ttu-id="e2a38-117">En-tête HTTPS</span><span class="sxs-lookup"><span data-stu-id="e2a38-117">HTTPS header</span></span> | `navigator.userAgent` <span data-ttu-id="e2a38-118">Méthode JavaScript</span><span class="sxs-lookup"><span data-stu-id="e2a38-118">JavaScript method</span></span> |  

<span data-ttu-id="e2a38-119">Microsoft recommande d’utiliser la détection [des][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] fonctionnalités dans la mesure du possible pour les raisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2a38-119">Microsoft recommends that you use [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] whenever possible for the following reasons.</span></span>  

*   <span data-ttu-id="e2a38-120">Améliorer la maintenabilité du code.</span><span class="sxs-lookup"><span data-stu-id="e2a38-120">Improve code maintainability.</span></span>  
*   <span data-ttu-id="e2a38-121">Réduisez la flexibilité du code.</span><span class="sxs-lookup"><span data-stu-id="e2a38-121">Reduce code fragility.</span></span>  
*   <span data-ttu-id="e2a38-122">Réduisez l’arrêt du code suite aux modifications apportées à User-Agent chaîne.</span><span class="sxs-lookup"><span data-stu-id="e2a38-122">Reduce code breakage from changes to the User-Agent string.</span></span>  
    
<span data-ttu-id="e2a38-123">Lorsque [la détection des][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] fonctionnalités n’est pas applicable et que vous devez utiliser la détection de l’agent utilisateur, utilisez le format suivant pour détecter Microsoft Edge’agent utilisateur sur Windows et Android.</span><span class="sxs-lookup"><span data-stu-id="e2a38-123">When [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable and you must use user agent detection, use the following format to detect Microsoft Edge user agent on Windows and Android.</span></span>  

## <a name="user-agent-client-hints"></a><span data-ttu-id="e2a38-124">User-Agent client</span><span class="sxs-lookup"><span data-stu-id="e2a38-124">User-Agent Client Hints</span></span>  

<span data-ttu-id="e2a38-125">À partir Microsoft Edge version 90, accédez aux informations du navigateur de manière plus propre et plus confidentielle.</span><span class="sxs-lookup"><span data-stu-id="e2a38-125">Starting in Microsoft Edge version 90, access browser information in a cleaner, more privacy-preserving way.</span></span>  

### <a name="user-agent-client-hints-https-header"></a><span data-ttu-id="e2a38-126">User-Agent d’en-tête HTTPS des conseils du client</span><span class="sxs-lookup"><span data-stu-id="e2a38-126">User-Agent Client Hints HTTPS Header</span></span>  

<span data-ttu-id="e2a38-127">Par défaut, Chromium navigateurs, y compris Microsoft Edge envoyer l’en-tête de `Accept-CH-UA` réponse au format suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a38-127">By default, Chromium browsers including Microsoft Edge send the `Accept-CH-UA` response header in the following format.</span></span>  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> <span data-ttu-id="e2a38-128">Les conseils client sont uniquement envoyés via des connexions sécurisées à l’aide `HTTPS` de .</span><span class="sxs-lookup"><span data-stu-id="e2a38-128">Client Hints are only sent over secure connections using `HTTPS`.</span></span>  

<span data-ttu-id="e2a38-129">Les conseils d’entropie faible suivants sont envoyés par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2a38-129">The following low entropy hints are sent by default.</span></span>  <span data-ttu-id="e2a38-130">Si vous avez besoin d’accéder à plus d’informations, envoyez l’un des en-têtes de requête suivants.</span><span class="sxs-lookup"><span data-stu-id="e2a38-130">If you need to access more information, send one of the following request headers.</span></span>  

#### <a name="user-agent-request-and-response-headers"></a><span data-ttu-id="e2a38-131">User-Agent en-têtes de requête et de réponse</span><span class="sxs-lookup"><span data-stu-id="e2a38-131">User-Agent request and response headers</span></span>  

| <span data-ttu-id="e2a38-132">En-tête de requête</span><span class="sxs-lookup"><span data-stu-id="e2a38-132">Request header</span></span> | <span data-ttu-id="e2a38-133">Exemple de valeur de réponse</span><span class="sxs-lookup"><span data-stu-id="e2a38-133">Example response value</span></span> |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a><span data-ttu-id="e2a38-134">User-Agent API JavaScript d’indications client</span><span class="sxs-lookup"><span data-stu-id="e2a38-134">User-Agent Client Hints JavaScript API</span></span>  

<span data-ttu-id="e2a38-135">La valeur de réponse par défaut `navigator.userAgentData` utilise le format suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a38-135">The default response value from `navigator.userAgentData` uses the following format.</span></span>  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

<span data-ttu-id="e2a38-136">Si vous avez besoin d’accéder à des informations plus détaillées, utilisez la [méthode getHighEntropyValues().][GithubWicgUaClientHintsGethighentropyvalues]</span><span class="sxs-lookup"><span data-stu-id="e2a38-136">If you need to access more detailed information, use the [getHighEntropyValues()][GithubWicgUaClientHintsGethighentropyvalues] method.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2a38-137">L’extrait de code suivant envoie une demande.</span><span class="sxs-lookup"><span data-stu-id="e2a38-137">The following code snippet sends a request.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e2a38-138">Pour recevoir la réponse suivante.</span><span class="sxs-lookup"><span data-stu-id="e2a38-138">To receive the following response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```javascript
         navigator.userAgentData.getHighEntropyValues(
             ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
             .then(ua => { console.log(ua) });
      ```  
   :::column-end:::
   :::column span="":::
      ```javascript
      {architecture: "x86", 
      model: "", 
      platform: "Windows", 
      platformVersion: "10.0", 
      uaFullVersion: "92.0.866.0"}
      ```  
   :::column-end:::
:::row-end:::  

## <a name="recommended-uses-of-user-agent-client-hints"></a><span data-ttu-id="e2a38-139">Utilisations recommandées des conseils User-Agent client</span><span class="sxs-lookup"><span data-stu-id="e2a38-139">Recommended uses of User-Agent Client Hints</span></span>  

<span data-ttu-id="e2a38-140">L’ensemble des marques et l’ordre d’affichage associé changent au fil du temps. Vous ne devez donc jamais coder en dur les index dans le tableau des marques renvoyées.</span><span class="sxs-lookup"><span data-stu-id="e2a38-140">The set of brands and the associated display order change over time, so you should never hard-code indices into the array of returned brands.</span></span>  <span data-ttu-id="e2a38-141">Pour vous assurer de détecter des problèmes similaires dans votre site web tôt, le navigateur inclut une valeur de marque qui change au fil du temps et est mise en forme pour se rompre en raison de problèmes courants d’utilisation des `GREASE` chaînes.</span><span class="sxs-lookup"><span data-stu-id="e2a38-141">To help ensure you spot similar issues in your website early, the browser includes a `GREASE` brand value that changes over time and is formatted to break because of common string parsing issues.</span></span>  

<span data-ttu-id="e2a38-142">Si vous ne pouvez pas utiliser la détection de [fonctionnalités,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]n’utilisez pas de liste codée en dur des navigateurs basés sur Chromium connus pour la vérification.</span><span class="sxs-lookup"><span data-stu-id="e2a38-142">If you're prevented from using [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection], don't use a hardcoded list of known Chromium-based browsers for verification.</span></span>  <span data-ttu-id="e2a38-143">Exemples de noms de navigateur codés en dur `Microsoft Edge` : `Google Chrome`</span><span class="sxs-lookup"><span data-stu-id="e2a38-143">Examples of hardcoded browser names include `Microsoft Edge` and `Google Chrome`.</span></span>  <span data-ttu-id="e2a38-144">Les raisons [pour lesquelles la détection des][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] fonctionnalités n’est pas applicable peuvent inclure la situation suivante.</span><span class="sxs-lookup"><span data-stu-id="e2a38-144">Reasons why [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable may include the following situation.</span></span>  

*   <span data-ttu-id="e2a38-145">Un correctif pour un bogue Chromium dans une version ultérieure doit être évité et les navigateurs concernés sont difficiles à détecter en dehors d’une vérification de la marque et de la version.</span><span class="sxs-lookup"><span data-stu-id="e2a38-145">A fix for a Chromium bug in a later version must be avoided and the affected browsers are difficult to detect outside of a verification of the brand and version.</span></span>  
    
<span data-ttu-id="e2a38-146">Au lieu de cela, vous devez vérifier la marque, ce qui garantit que votre détection s’applique à tous Chromium `Chromium` navigateurs basés sur les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="e2a38-146">Instead, you should verify the `Chromium` brand, which ensures your detection applies to all affected Chromium-based browsers.</span></span>  


```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium") {
            return true;
        }
    }
    return false;
}
```  

## <a name="user-agent-string"></a><span data-ttu-id="e2a38-147">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="e2a38-147">User agent string</span></span>  

<span data-ttu-id="e2a38-148">Dans la mesure du possible, Microsoft vous recommande de réduire votre utilisation de la logique de détection Microsoft Edge navigateur en fonction de la chaîne de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2a38-148">Wherever possible, Microsoft recommends you minimize your use of Microsoft Edge browser detection logic based on the user agent string.</span></span>  <span data-ttu-id="e2a38-149">Si vous avez une bonne raison de détecter l’agent utilisateur, l’équipe Microsoft Edge vous recommande d’utiliser les [conseils](#user-agent-client-hints) client de l’agent utilisateur comme logique de détection principale.</span><span class="sxs-lookup"><span data-stu-id="e2a38-149">If you have a good reason to detect the user agent, the Microsoft Edge team recommends you use [User-Agent Client Hints](#user-agent-client-hints) as the primary detection logic.</span></span>  <span data-ttu-id="e2a38-150">[Les conseils client de l’agent](#user-agent-client-hints) utilisateur réduisent également le nombre requis de chaînes filées.</span><span class="sxs-lookup"><span data-stu-id="e2a38-150">[User-Agent Client Hints](#user-agent-client-hints) also reduces the required number of parsed strings.</span></span>  <span data-ttu-id="e2a38-151">Toutefois, pour la référence héritée, le format suivant est utilisé pour User-Agent chaîne.</span><span class="sxs-lookup"><span data-stu-id="e2a38-151">However, for legacy reference, the following format is used for the User-Agent string.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2a38-152">Sur Windows, l’en-tête de requête `User-Agent` HTTP utilise le format suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a38-152">On Windows, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e2a38-153">Sur Android, `User-Agent` l’en-tête de requête HTTP utilise le format suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a38-153">On Android, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e2a38-154">La valeur de réponse de `navigator.userAgent` la méthode utilise le format suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a38-154">The response value from `navigator.userAgent` method uses the following format.</span></span>  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

<span data-ttu-id="e2a38-155">Les identificateurs de plateforme changent en fonction du système d’exploitation utilisé, et les numéros de version sont également incrémentés au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="e2a38-155">Platform identifiers change based on the operating system used, and the version numbers also increment as time passes.</span></span>  <span data-ttu-id="e2a38-156">Le format est identique à celui de Chromium’agent utilisateur avec l’ajout d’un nouveau jeton `Edg` à la fin.</span><span class="sxs-lookup"><span data-stu-id="e2a38-156">The format is the same as the Chromium user agent with the addition of a new `Edg` token at the end.</span></span>  <span data-ttu-id="e2a38-157">Microsoft a choisi le jeton pour éviter les problèmes de compatibilité causés par la chaîne, qui était utilisée Microsoft Edge navigateur basé sur `Edg` `Edge` EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e2a38-157">Microsoft chose the `Edg` token to avoid compatibility issues caused by `Edge` string, which was used legacy Microsoft Edge browser based on EdgeHTML.</span></span>  <span data-ttu-id="e2a38-158">Le `Edg` jeton est également cohérent avec [les jetons existants utilisés][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] sur iOS et Android.</span><span class="sxs-lookup"><span data-stu-id="e2a38-158">The `Edg` token is also consistent with [existing tokens][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] used on iOS and Android.</span></span>

## <a name="map-the-user-agent-string-to-browser-name"></a><span data-ttu-id="e2a38-159">Ma cartographier la chaîne de l’agent utilisateur sur le nom du navigateur</span><span class="sxs-lookup"><span data-stu-id="e2a38-159">Map the user agent string to browser name</span></span>  

<span data-ttu-id="e2a38-160">Maplisez les jetons de chaîne de l’agent utilisateur sur un nom de navigateur plus lisible à utiliser dans le code.</span><span class="sxs-lookup"><span data-stu-id="e2a38-160">Map the user agent string tokens to a more human-readable browser name to use in code.</span></span>  <span data-ttu-id="e2a38-161">Il s’agit d’un modèle courant sur le web aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="e2a38-161">It's a common pattern on the web today.</span></span>  <span data-ttu-id="e2a38-162">Lorsque vous mapz le nouveau jeton sur un nom de navigateur, Microsoft vous recommande d’utiliser un nom différent de celui utilisé pour le navigateur Microsoft Edge hérité pour éviter d’appliquer accidentellement des solutions de contournement héritées qui ne sont pas applicables aux navigateurs basés sur `Edg` Chromium.</span><span class="sxs-lookup"><span data-stu-id="e2a38-162">When you map the new `Edg` token to a browser name, Microsoft recommends that you use a different name than the one used for the legacy Microsoft Edge browser to avoid accidentally applying any legacy workarounds that aren't applicable to Chromium-based browsers.</span></span>

## <a name="user-agent-overrides"></a><span data-ttu-id="e2a38-163">Remplacements de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="e2a38-163">User Agent overrides</span></span>  

<span data-ttu-id="e2a38-164">Parfois, un site web ne reconnaît pas le nouvel agent Microsoft Edge utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2a38-164">Sometimes, a website doesn't recognize the new Microsoft Edge user agent.</span></span>  <span data-ttu-id="e2a38-165">Par conséquent, un ensemble de fonctionnalités du site web peut ne pas fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="e2a38-165">As a result, a set of the features of the website may not work correctly.</span></span>  <span data-ttu-id="e2a38-166">Lorsque Microsoft est informé des types de problèmes, Microsoft vous contacte \(un propriétaire de site web\) et vous informe de l’agent utilisateur mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e2a38-166">When Microsoft is notified about the types of issues, Microsoft contacts you \(a website owner\) and informs you about the updated user agent.</span></span>  

<span data-ttu-id="e2a38-167">Vous aurez peut-être besoin de plus de temps pour mettre à jour et tester la logique de détection de l’agent utilisateur pour votre site web afin de résoudre les problèmes signalés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2a38-167">You may need more time to update and test the user agent detection logic for your website to address the issues reported by Microsoft.</span></span>  <span data-ttu-id="e2a38-168">Pour optimiser la compatibilité pour vos utilisateurs, les canaux Microsoft Edge Beta et stables utilisent une liste de substitutions d’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2a38-168">To maximize compatibility for your users, the Microsoft Edge Beta and Stable channels use a list of user agent overrides.</span></span>  <span data-ttu-id="e2a38-169">Utilisez les remplacements de l’agent utilisateur lors de la mise à jour de votre site web.</span><span class="sxs-lookup"><span data-stu-id="e2a38-169">Use the user agent overrides while you update your website.</span></span>  <span data-ttu-id="e2a38-170">Liste des substitutions d’agent utilisateur fournies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2a38-170">The list of user agent overrides provided by Microsoft.</span></span>  

<span data-ttu-id="e2a38-171">Les substitutions spécifient de nouvelles valeurs d’agent utilisateur Microsoft Edge à la place de l’agent utilisateur par défaut pour des sites web spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e2a38-171">The overrides specify new user agent values that Microsoft Edge sends instead of the default user agent for specific websites.</span></span>  <span data-ttu-id="e2a38-172">Pour afficher la liste des substitutions d’agent utilisateur actuellement appliquées, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2a38-172">To display the list of user agent overrides that are currently applied, complete the following actions.</span></span>  

1.  <span data-ttu-id="e2a38-173">Ouvrez le Microsoft Edge Beta canal stable ou stable.</span><span class="sxs-lookup"><span data-stu-id="e2a38-173">Open the Microsoft Edge Beta or Stable channel.</span></span>  
1.  <span data-ttu-id="e2a38-174">Naviguez vers`edge://compat/useragent` .</span><span class="sxs-lookup"><span data-stu-id="e2a38-174">Navigate to `edge://compat/useragent`.</span></span>  
    
<span data-ttu-id="e2a38-175">Les Microsoft Edge Canary et dev ne reçoivent actuellement pas de substitutions d’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2a38-175">The Microsoft Edge Canary and Dev channels don't currently receive user agent overrides.</span></span>  <span data-ttu-id="e2a38-176">Les canaux Microsoft Edge Canary et Dev fournissent des environnements qui utilisent l’agent utilisateur Microsoft Edge par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2a38-176">The Microsoft Edge Canary and Dev channels provide environments that use the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="e2a38-177">Utilisez les canaux Microsoft Edge Canary et Dev pour reproduire facilement les problèmes sur votre site web causés par l’agent Microsoft Edge par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2a38-177">Use the Microsoft Edge Canary and Dev channels to easily reproduce issues on your website caused by the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="e2a38-178">Pour désactiver les substitutions d’agent utilisateur dans Microsoft Edge Beta ou canaux stables, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2a38-178">To turn off user agent overrides in the Microsoft Edge Beta or Stable channels, complete the following actions.</span></span>  

1.  <span data-ttu-id="e2a38-179">Ouvrez votre application en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e2a38-179">Open your command-line app.</span></span>  
1.  <span data-ttu-id="e2a38-180">Copiez et collez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a38-180">Copy and paste the following code snippet.</span></span>  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  <span data-ttu-id="e2a38-181">Exécutez l Microsoft Edge appapplment de code à l’aide de l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="e2a38-181">Run the Microsoft Edge app using the code snippet.</span></span>  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge pour iOS et Android : ce que les développeurs doivent savoir | Blogs microsoft Windows"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. méthode getHighEntropyValues - User-Agent client hints | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Mise en œuvre des fonctionnalités de détection | MDN"  
