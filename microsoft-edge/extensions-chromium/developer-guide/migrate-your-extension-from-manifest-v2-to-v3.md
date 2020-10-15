---
description: En savoir plus sur la mise à jour de votre extension du manifeste v2 vers la version v3
title: Préparer la mise à jour de vos extensions du manifeste v2 au version v3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions latérales, extensions de navigateur, compléments, développeur, manifeste v3, migration vers le manifeste v3
ms.openlocfilehash: 262a5cab54dd23f596791c93ec1238619e247333
ms.sourcegitcommit: 1ad087b00df16fd7718a5d95226de57e29b335e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117827"
---
# Préparer la mise à jour de vos extensions du manifeste v2 au version v3 

Ce document dresse la liste des modifications importantes qui sont implémentées dans le cadre du manifeste v3, qui est la version suivante de la plateforme d’extensions de chrome. Nous allons mettre à jour ce document au fur et à mesure de l’avancement de l’implémentation. Pour obtenir des instructions détaillées sur la migration de votre extension vers manifest v3, accédez à la [migration vers le manifeste v3][Google_Migrate_to_MV3]. 

## Code hébergé à distance  

Aujourd’hui, les extensions peuvent héberger des parties de leur code à distance, mais ne les incluent pas dans le cadre du processus de validation. Même si cela permet de modifier le code sans remettre l’extension dans le Windows Store, le code peut être exploité après l’installation. Pour vous assurer que [les modules complémentaires Microsoft Edge][EdgeAddons] répertorient les extensions validées, nous n’autorisons pas les extensions à utiliser du Code hébergé à distance. Cette modification rend les extensions plus sûres. Les développeurs doivent empaqueter et transmettre tout le code utilisé par l’extension de validation. Par ailleurs, les développeurs peuvent utiliser la fonction eval () dans un [environnement en bac à sable (sandbox][sandboxingEval]). 

## Autorisations d’hébergement au moment de l’exécution  

Au moment de l’installation, les extensions pourront demander des autorisations d’accès permanent pour accéder à l’ensemble des sites et du contenu. Ces autorisations permettent les extensions de fonctionner avec le minimum d’intervention et créent un risque pour la confidentialité et la sécurité de l’utilisateur. Pour améliorer la transparence, nous proposons des contrôles permettant aux utilisateurs d’autoriser ou de restreindre l’accès aux sites Web lors de l’exécution. 

## Demandes d’origine dans les scripts de contenu  

Les scripts de contenu du jour peuvent demander l’accès à toute origine, y compris les origines qui ne sont pas autorisées par le site Web. Ce comportement décompose les principes d’origine croisée. À l’avenir, nous aurons besoin de scripts de contenu pour utiliser les mêmes autorisations que celles de la page dans laquelle elles sont injectées, ce qui a provoqué une faille de sécurité potentielle. Pour effectuer des demandes d’exécution croisée, vous devez utiliser des scripts en arrière-plan pour relayer les réponses aux scripts de contenu. Ces modifications sont disponibles et derrière un indicateur. Pour plus d’informations, accédez à ce [document][CORS]. 

## API de requête Web  

Nous remplaçons l' [API de requête Web][WebRequestAPI] par une [API de requête net déclarative][DeclarativeNetRequestAPI], mais les fonctionnalités de observational de l’API de requête Web seront maintenues. À l’exception des scénarios spécifiques dans lesquels les fonctionnalités observational de l’API de requête Web sont requises par l’extension, nous vous recommandons d’utiliser les API DNR uniquement. Nous pensons que cette modification aura un impact positif sur les extensions qui utilisent des fonctionnalités déclaratives riches en fonctionnalités. Dans la mesure où de plus en plus d’extensions seront transférées vers les API DNR, cette modification améliorera la confidentialité des utilisateurs, ce qui contribue à améliorer la fiabilité de l’utilisation des extensions.
Les entreprises peuvent continuer à utiliser le comportement de blocage de l’API de requête Web pour les extensions gérées par le biais des stratégies d’entreprise. Pour plus d’informations sur les stratégies d’extension, accédez à [Microsoft Edge-politiques][MicrosoftEdgePolicies]. 

## Travailleurs de services en arrière-plan  
 
Les travailleurs de services peuvent être testés au Canaries. Pour migrer vos extensions des pages d’arrière-plan vers des travailleurs de service, voir [migrer des pages d’arrière-plan vers des travailleurs de service][ServiceWorkers]. Nous estimons & d’avoir examiné l’impact que ce changement apporte aux développeurs et aux utilisateurs. Nous ajouterons des informations supplémentaires sur cette modification à ce document à l’avenir. 

## Quelles sont les modifications disponibles dans Microsoft Edge?

L’implémentation actuelle de l’API de requête NET déclaratif est disponible dans nos canaux stables et beta. Les développeurs peuvent tester ces modifications et transmettre des commentaires. Nous allons contribuer aux efforts de développement et étudier les changements ultérieurs. 

| Nom du canal | Description |
|:--- |:--- |  
| Microsoft Edge 84 stable | L’API DNR est disponible pour le test |  
| Microsoft Edge 85 Beta | La prise en charge du changement d’en-tête est disponible| 

Lorsque les modifications sont apportées au chrome, nous partageons les chronologies pour permettre aux développeurs de mettre à jour leur code et de republier les extensions dans le Windows Store. 

Nous allons continuer à publier des mises à jour sur notre blog. Vous pouvez fournir vos commentaires sur ces modifications par le biais de [TechCommunity][TechCommunity].

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/ "Modules complémentaires Microsoft Edge"  
[MicrosoftBlog]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/  
[MicrosoftEdgePolicies]: https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions 

[TechCommunity]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Communauté technologique"  


[Google_Migrate_to_MV3]: https://developer.chrome.com/extensions/migrating_to_manifest_v3   
[SandboxingEval]: https://developer.chrome.com/apps/sandboxingEval "Utilisation de eval dans les extensions chrome. En toute sécurité."
[CORS]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Modifications apportées aux demandes d’interrogation dans les scripts de contenu d’extension"
[WebRequestAPI]: https://developer.chrome.com/extensions/webRequest "API de requête Web"  
[DeclarativeNetRequestAPI]: https://developer.chrome.com/extensions/declarativeNetRequest/ "API de requête NET déclaratif"
[ServiceWorkers]:  https://developers.chrome.com/extensions/migrating_to_service_workers


