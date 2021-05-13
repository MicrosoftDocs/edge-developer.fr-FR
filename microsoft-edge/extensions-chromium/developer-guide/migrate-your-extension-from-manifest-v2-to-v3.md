---
description: En savoir plus sur la mise à jour de votre extension du manifeste V2 vers V3
title: Préparer la mise à jour de vos extensions du manifeste V2 vers V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions edge, extensions de navigateur, addons, développeur, manifeste v3, migrer vers le manifeste v3
ms.openlocfilehash: 5aa1aa7446a312d581bacc4fa19ba7362c6c2a3e
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564615"
---
# <a name="prepare-to-update-your-extensions-from-manifest-v2-to-v3"></a>Préparer la mise à jour de vos extensions du manifeste v2 vers v3  

Ce document répertorie les modifications importantes implémentées dans le cadre du manifeste v3, qui est la prochaine version de la plateforme Chromium Extensions.  L’équipe Microsoft Edge extensions de service met à jour ce document à mesure que l’implémentation progresse.  Pour obtenir des instructions détaillées sur la migration de votre extension vers manifeste v3, accédez à [La migration vers manifeste V3][ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist].  

## <a name="remotely-hosted-code"></a>Code hébergé à distance  

Aujourd’hui, certaines parties du code des extensions sont hébergées à distance et ne l’incluent pas dans le package d’extension pendant le processus de validation.  Bien que cela offre de la flexibilité pour modifier le code sans resoumettre l’extension dans le magasin, le code peut être exploité après l’installation.  Pour [s’assurer Microsoft Edge listes][MicrosoftMicrosoftedgeAddons] d’extensions validées, l’équipe Microsoft Edge extensions de l’équipe des extensions ne peut pas utiliser de code hébergé à distance.  Cette modification rend les extensions plus sécurisées.  Les développeurs doivent créer un package et soumettre tout le code utilisé par l’extension pour validation.  Vous pouvez également utiliser la fonction dans un environnement `eval()` en bac à [sable][ChromeDeveloperDocsExtensionsMv2Sandboxingeval].  

## <a name="run-time-host-permissions"></a>Autorisations d’hôte au moment de l’run-time  

Au moment de l’installation, les extensions peuvent demander des autorisations d’accès autorisé pour accéder à tous les sites et contenus.  Ces autorisations permettent aux extensions de fonctionner avec une intervention minimale et de créer un risque pour la confidentialité et la sécurité des utilisateurs.  Pour améliorer la transparence, l’équipe Microsoft Edge extensions fournit des contrôles permettant aux utilisateurs d’autoriser ou de restreindre l’accès aux sites web au moment de l’utilisation.  

## <a name="cross-origin-requests-in-content-scripts"></a>Demandes d’origine croisée dans les scripts de contenu  

Aujourd’hui, les scripts de contenu demandent l’accès à n’importe quelle origine, y compris aux origines qui ne sont pas autorisées par le site web.  Le comportement rompt les principes d’origine croisée.  À l’avenir, l’équipe des extensions Microsoft Edge exige que les scripts de contenu soient autorisés à avoir les mêmes autorisations que la page web dans laquelle les scripts sont injectés, ce qui permet de fermer une faille de sécurité potentielle.  Pour effectuer des demandes d’origine croisée, vous devez utiliser des scripts d’arrière-plan pour relayer les réponses aux scripts de contenu.  Ces modifications sont disponibles et derrière un indicateur.  Pour plus d’informations, accédez à ce [document.][ChromiumHomeChromiumSecurityExtensionContentScriptFetches]  

## <a name="web-request-api"></a>API de demande web  

L Microsoft Edge d’extensions de connexion remplace [l’API][ChromeDeveloperDocsExtensionsReferenceWebrequest] de demande Web par l’API de demande [Net][ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]déclarative, mais continue de conserver les fonctionnalités d’observation de l’API de demande Web.  Sauf dans certains scénarios spécifiques où les fonctionnalités d’observation de l’API de demande Web sont requises par l’extension, l’équipe des extensions Microsoft Edge recommande d’utiliser uniquement les API DNR.  L Microsoft Edge d’extensions de service estime que cette modification aura un impact positif sur les extensions qui utilisent des fonctionnalités déclaratives enrichies.  À mesure que d’autres extensions passeront aux API DNR, cette modification améliorera la confidentialité des utilisateurs, ce qui contribue à renforcer la confiance dans l’utilisation des extensions.  
Les entreprises peuvent continuer à utiliser le comportement de blocage de l’API de demande web pour les extensions gérées par le biais de stratégies d’entreprise.  Pour plus d’informations sur les stratégies d’extension, [accédez à Microsoft Edge – Stratégies.][DeployedgeMicrosoftEdgePoliciesExtensions]  

## <a name="background-service-workers"></a>Travailleurs du service d’arrière-plan  
 
Les employés de service peuvent être testés dans Canary.  Pour migrer vos extensions des pages d’arrière-plan vers les travailleurs du service, reportez-vous à La migration des pages d’arrière-plan vers les travailleurs [de service.][ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers]  L Microsoft Edge d’extensions de l’utilisateur évalue et examine l’impact de cette modification à la fois pour les développeurs et les utilisateurs.  L Microsoft Edge des extensions de l’équipe ajoute des détails supplémentaires sur la modification à ce document à l’avenir.  

## <a name="when-are-these-changes-available-in-microsoft-edge"></a>Quand ces modifications sont-elles disponibles dans Microsoft Edge  

L’implémentation actuelle de l’API de demande net déclarative est disponible dans nos canaux stables et bêta.  Testez les modifications et fournissez des commentaires.  L’équipe Microsoft Edge extensions de projet contribue aux efforts de développement et examine d’autres modifications.  

| Nom du canal | Détails |  
|:--- |:--- |  
| Microsoft Edge 84 stable | L’API DNR est disponible pour les tests |  
| Microsoft Edge 85 bêta | La prise en charge de la modification d’en-tête est disponible|  

Lorsque les modifications sont apportées à Chromium, l’équipe des extensions Microsoft Edge partage les chronologies afin que vous pouvez mettre à jour votre code et republier les extensions dans le magasin.  

L’équipe Microsoft Edge extensions de publication continue de publier des mises à jour sur le blog.  Vous pouvez fournir vos commentaires sur les modifications par le biais [de Tech Community][MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254].

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesExtensions]: /deployedge/microsoft-edge-policies#extensions "Extensions - Microsoft Edge - Stratégies | Documents Microsoft"  

[MicrosoftMicrosoftedgeAddons]: https://microsoftedge.microsoft.com/addons "Microsoft Edge Modules de modules"  

[MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Les modifications du manifeste V3 sont désormais disponibles dans Microsoft Edge | Microsoft Tech Community"  

[ChromeDeveloperDocsExtensionsMv2Sandboxingeval]: https://developer.chrome.com/docs/extensions/mv2/sandboxingEval "Utilisation d’eval dans les extensions Chrome | Développeurs Chrome"  
[ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers]:  https://developer.chrome.com/docs/extensions/mv3/migrating_to_service_workers "Migration de pages d’arrière-plan vers des | Développeurs Chrome"  
[ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist]: https://developer.chrome.com/docs/extensions/mv3/mv3-migration-checklist "Liste de contrôle de la migration de manifeste V3 | Développeurs Chrome"    

[ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]: https://developer.chrome.com/docs/extensions/reference/declarativeNetRequest "Chrome.declarativeNetRequest | Développeurs Chrome"  
[ChromeDeveloperDocsExtensionsReferenceWebrequest]: https://developer.chrome.com/docs/extensions/reference/webRequest "Chrome.webRequest, | Développeurs Chrome"  

[ChromiumHomeChromiumSecurityExtensionContentScriptFetches]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Modifications apportées aux demandes d’origine croisée dans les scripts de contenu d’extension Chrome | Projets Chromium projet"  
