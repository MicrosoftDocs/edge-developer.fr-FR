---
description: Cet article fournit de la documentation sur les conseils Microsoft Edge client de l’agent utilisateur et la chaîne de l’agent utilisateur
title: Comment détecter les Microsoft Edge dans votre site web
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
# <a name="how-to-detect-microsoft-edge-in-your-website"></a>Comment détecter les Microsoft Edge dans votre site web  

Les navigateurs fournissent des mécanismes permettant aux sites web de détecter les informations de navigateur telles que la marque et le numéro de version.  Les mécanismes détectent également d’autres caractéristiques d’appareil telles que le système d’exploitation hôte.  Deux de ces mécanismes pris en charge sur Microsoft Edge sont les [conseils](#user-agent-client-hints) client de l’agent utilisateur et les chaînes [d’agent utilisateur](#user-agent-string).  Après des années d’utilisation, User-Agent chaînes sont obsolètes et ont un long historique en tant que cause des problèmes de compatibilité des sites web.  Au lieu de cela, l’équipe Microsoft Edge vous recommande d’utiliser un mécanisme amélioré pour récupérer les informations de navigateur [nommées User-Agent Client Hints](#user-agent-client-hints).  Cet article décrit les deux mécanismes Microsoft Edge pour la récupération des informations de l’agent utilisateur.  

|  | Côté serveur | Côté client |  
|:--- |:--- |:--- | 
| **Conseils client de l’agent** utilisateur \(recommandé\) | `Sec-CH-UA` En-tête HTTPS | `navigator.userAgentData` Méthode JavaScript |  
| **Chaîne user-Agent** \(legacy\) | `User-Agent` En-tête HTTPS | `navigator.userAgent` Méthode JavaScript |  

Microsoft recommande d’utiliser la détection [des][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] fonctionnalités dans la mesure du possible pour les raisons suivantes.  

*   Améliorer la maintenabilité du code.  
*   Réduisez la flexibilité du code.  
*   Réduisez l’arrêt du code suite aux modifications apportées à User-Agent chaîne.  
    
Lorsque [la détection des][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] fonctionnalités n’est pas applicable et que vous devez utiliser la détection de l’agent utilisateur, utilisez le format suivant pour détecter Microsoft Edge’agent utilisateur sur Windows et Android.  

## <a name="user-agent-client-hints"></a>User-Agent client  

À partir Microsoft Edge version 90, accédez aux informations du navigateur de manière plus propre et plus confidentielle.  

### <a name="user-agent-client-hints-https-header"></a>User-Agent d’en-tête HTTPS des conseils du client  

Par défaut, Chromium navigateurs, y compris Microsoft Edge envoyer l’en-tête de `Accept-CH-UA` réponse au format suivant.  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> Les conseils client sont uniquement envoyés via des connexions sécurisées à l’aide `HTTPS` de .  

Les conseils d’entropie faible suivants sont envoyés par défaut.  Si vous avez besoin d’accéder à plus d’informations, envoyez l’un des en-têtes de requête suivants.  

#### <a name="user-agent-request-and-response-headers"></a>User-Agent en-têtes de requête et de réponse  

| En-tête de requête | Exemple de valeur de réponse |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a>User-Agent API JavaScript d’indications client  

La valeur de réponse par défaut `navigator.userAgentData` utilise le format suivant.  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

Si vous avez besoin d’accéder à des informations plus détaillées, utilisez la [méthode getHighEntropyValues().][GithubWicgUaClientHintsGethighentropyvalues]  

:::row:::
   :::column span="":::
      L’extrait de code suivant envoie une demande.  
   :::column-end:::
   :::column span="":::
      Pour recevoir la réponse suivante.  
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

## <a name="recommended-uses-of-user-agent-client-hints"></a>Utilisations recommandées des conseils User-Agent client  

L’ensemble des marques et l’ordre d’affichage associé changent au fil du temps. Vous ne devez donc jamais coder en dur les index dans le tableau des marques renvoyées.  Pour vous assurer de détecter des problèmes similaires dans votre site web tôt, le navigateur inclut une valeur de marque qui change au fil du temps et est mise en forme pour se rompre en raison de problèmes courants d’utilisation des `GREASE` chaînes.  

Si vous ne pouvez pas utiliser la détection de [fonctionnalités,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]n’utilisez pas de liste codée en dur des navigateurs basés sur Chromium connus pour la vérification.  Exemples de noms de navigateur codés en dur `Microsoft Edge` : `Google Chrome`  Les raisons [pour lesquelles la détection des][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] fonctionnalités n’est pas applicable peuvent inclure la situation suivante.  

*   Un correctif pour un bogue Chromium dans une version ultérieure doit être évité et les navigateurs concernés sont difficiles à détecter en dehors d’une vérification de la marque et de la version.  
    
Au lieu de cela, vous devez vérifier la marque, ce qui garantit que votre détection s’applique à tous Chromium `Chromium` navigateurs basés sur les navigateurs.  


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

## <a name="user-agent-string"></a>Chaîne de l’agent utilisateur  

Dans la mesure du possible, Microsoft vous recommande de réduire votre utilisation de la logique de détection Microsoft Edge navigateur en fonction de la chaîne de l’agent utilisateur.  Si vous avez une bonne raison de détecter l’agent utilisateur, l’équipe Microsoft Edge vous recommande d’utiliser les [conseils](#user-agent-client-hints) client de l’agent utilisateur comme logique de détection principale.  [Les conseils client de l’agent](#user-agent-client-hints) utilisateur réduisent également le nombre requis de chaînes filées.  Toutefois, pour la référence héritée, le format suivant est utilisé pour User-Agent chaîne.  

:::row:::
   :::column span="":::
      Sur Windows, l’en-tête de requête `User-Agent` HTTP utilise le format suivant.  
   :::column-end:::
   :::column span="":::
      Sur Android, `User-Agent` l’en-tête de requête HTTP utilise le format suivant.  
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

La valeur de réponse de `navigator.userAgent` la méthode utilise le format suivant.  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

Les identificateurs de plateforme changent en fonction du système d’exploitation utilisé, et les numéros de version sont également incrémentés au fil du temps.  Le format est identique à celui de Chromium’agent utilisateur avec l’ajout d’un nouveau jeton `Edg` à la fin.  Microsoft a choisi le jeton pour éviter les problèmes de compatibilité causés par la chaîne, qui était utilisée Microsoft Edge navigateur basé sur `Edg` `Edge` EdgeHTML.  Le `Edg` jeton est également cohérent avec [les jetons existants utilisés][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] sur iOS et Android.

## <a name="map-the-user-agent-string-to-browser-name"></a>Ma cartographier la chaîne de l’agent utilisateur sur le nom du navigateur  

Maplisez les jetons de chaîne de l’agent utilisateur sur un nom de navigateur plus lisible à utiliser dans le code.  Il s’agit d’un modèle courant sur le web aujourd’hui.  Lorsque vous mapz le nouveau jeton sur un nom de navigateur, Microsoft vous recommande d’utiliser un nom différent de celui utilisé pour le navigateur Microsoft Edge hérité pour éviter d’appliquer accidentellement des solutions de contournement héritées qui ne sont pas applicables aux navigateurs basés sur `Edg` Chromium.

## <a name="user-agent-overrides"></a>Remplacements de l’agent utilisateur  

Parfois, un site web ne reconnaît pas le nouvel agent Microsoft Edge utilisateur.  Par conséquent, un ensemble de fonctionnalités du site web peut ne pas fonctionner correctement.  Lorsque Microsoft est informé des types de problèmes, Microsoft vous contacte \(un propriétaire de site web\) et vous informe de l’agent utilisateur mis à jour.  

Vous aurez peut-être besoin de plus de temps pour mettre à jour et tester la logique de détection de l’agent utilisateur pour votre site web afin de résoudre les problèmes signalés par Microsoft.  Pour optimiser la compatibilité pour vos utilisateurs, les canaux Microsoft Edge Beta et stables utilisent une liste de substitutions d’agent utilisateur.  Utilisez les remplacements de l’agent utilisateur lors de la mise à jour de votre site web.  Liste des substitutions d’agent utilisateur fournies par Microsoft.  

Les substitutions spécifient de nouvelles valeurs d’agent utilisateur Microsoft Edge à la place de l’agent utilisateur par défaut pour des sites web spécifiques.  Pour afficher la liste des substitutions d’agent utilisateur actuellement appliquées, effectuer les actions suivantes.  

1.  Ouvrez le Microsoft Edge Beta canal stable ou stable.  
1.  Naviguez vers`edge://compat/useragent` .  
    
Les Microsoft Edge Canary et dev ne reçoivent actuellement pas de substitutions d’agent utilisateur.  Les canaux Microsoft Edge Canary et Dev fournissent des environnements qui utilisent l’agent utilisateur Microsoft Edge par défaut.  Utilisez les canaux Microsoft Edge Canary et Dev pour reproduire facilement les problèmes sur votre site web causés par l’agent Microsoft Edge par défaut.  Pour désactiver les substitutions d’agent utilisateur dans Microsoft Edge Beta ou canaux stables, effectuer les actions suivantes.  

1.  Ouvrez votre application en ligne de commande.  
1.  Copiez et collez l’extrait de code suivant.  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  Exécutez l Microsoft Edge appapplment de code à l’aide de l’extrait de code.  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge pour iOS et Android : ce que les développeurs doivent savoir | Blogs microsoft Windows"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. méthode getHighEntropyValues - User-Agent client hints | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Mise en œuvre des fonctionnalités de détection | MDN"  
