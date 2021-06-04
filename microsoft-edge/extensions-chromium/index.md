---
description: Vue d’ensemble de la création et de la publication Microsoft Edge (Chromium) Extensions.
title: Vue d’ensemble Microsoft Edge (Chromium) extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur, extensions chromium
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327525"
---
# Vue d’ensemble Microsoft Edge (Chromium) extensions  

Une extension est un petit programme que vous \(un développeur\) utilisez pour ajouter ou modifier des fonctionnalités pour Microsoft Edge \(Chromium\).  Une extension est destinée à améliorer l’expérience de navigation quotidienne d’un utilisateur.  Il fournit des fonctionnalités ciblées qui sont importantes pour un public cible.  

Vous pouvez créer une extension si vous avez une idée ou un produit basé sur l’une des conditions suivantes.  

*   Navigateur web spécifique.  
*   Améliorations apportées aux fonctionnalités de pages web spécifiques.  
    
Les bloqueurs de mots de passe et les gestionnaires de mots de passe sont des exemples d’expériences complémentaires.  

Une extension est structurée comme une application web normale.  Au minimum, il doit inclure les fonctionnalités suivantes.

*   Fichier JSON de manifeste d’application qui contient des informations de plateforme de base.  
*   Fichier JavaScript qui définit les fonctionnalités.  
*   Fichiers HTML et CSS qui définissent l’interface utilisateur.  

Pour travailler directement avec une partie du navigateur, telle qu’une fenêtre ou un onglet, vous devez envoyer des demandes d’API et référencer souvent le navigateur par son nom.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Une extension Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  Une extension Microsoft Edge \(Chromium\)  
:::image-end:::  

##  <a name="basic-guidance"></a>Conseils de base  

Certains des navigateurs les plus populaires pour créer des extensions incluent Safari, Firefox, Chrome, Opera, Firefox et Microsoft Edge.  L’emplacement idéal pour commencer vos didacticiels de développement d’extension et la recherche de documentation sont les sites hébergés par les organisations de navigateur.  Le tableau suivant n’est pas définitif et peut servir de point de départ.  

| Navigateur web | Chromium base de données ? | Page web de développement d’extensions |  
|:--- |:--- |:--- |  
| Safari | Non | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Non | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Oui | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Oui | [dev.opera.com/extensions][OperaDevExtensions] |  
| Vér. | Oui | Utilise [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| nouvelle Microsoft Edge | Oui | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> La plupart des didacticiels des sites utilisent des API spécifiques au navigateur qui peuvent ne pas correspondre au navigateur pour lequel vous développez.  Dans la plupart des cas, une extension Chromium fonctionne tel quel dans différents navigateurs Chromium et les API fonctionnent comme prévu.  Seules certaines API moins courantes peuvent être strictement spécifiques au navigateur.  Pour obtenir des liens vers les didacticiels, [accédez à Voir aussi](#see-also).  

##  <a name="why-chromium"></a>Pourquoi Chromium ?  

Si votre objectif est de publier votre extension dans le magasin d’extensions pour chaque navigateur, elle doit être modifiée pour que chaque version cible et s’exécute dans chaque environnement de navigateur distinct.  Par exemple, les [extensions Safari peuvent][AppleDeveloperSafariservicesAppExtensions] utiliser du code web et natif pour communiquer avec des applications natives homologues.  Les quatre derniers navigateurs du tableau précédent utilisent le même package de code et réduisent la nécessité de conserver des versions parallèles.  Ces navigateurs sont basés sur le [Chromium open source.][|::ref1::|Home]  

Créez une extension Chromium pour écrire le moins de code.  Il cible également le nombre maximal de magasins d’extensions et, en fin de compte, le nombre maximal d’utilisateurs qui trouvent et achètent votre extension.  

Le contenu suivant se concentre principalement sur Chromium extensions.  

##  <a name="browser-compatibility-and-extension-testing"></a>Test de compatibilité et d’extension du navigateur  

Parfois, la parité d’API n’existe pas entre Chromium navigateurs.  Par exemple, il existe des différences dans les API d’identité et de paiement.  Pour vous assurer que votre extension répond aux attentes des clients, examinez l’état de l’API via les documents officiels suivants du navigateur.  

*   [API Chrome][ChromeDeveloperExtensionsApiIndex]  
*   [API d’extension prise en charge dans Opera][OperaDevExtensionsApis]  
*   [Portage de l’extension Chrome Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]  
    
Les API dont vous avez besoin définissent les modifications que vous devez apporter pour résoudre les différences entre chaque navigateur.  Cela peut signifier que vous devez créer des packages de code légèrement différents avec de petites différences pour chaque magasin.  

Pour tester votre extension dans différents environnements avant de l’envoyer à un magasin de navigateurs, chargez-la dans votre navigateur pendant que vous la développez.  

##  <a name="publish-your-extension-to-browser-stores"></a>Publier votre extension dans les magasins de navigateurs  

Vous pouvez soumettre et rechercher des extensions de navigateur dans les magasins de navigateurs suivants.  

*   [Modules de modules de navigateur Firefox][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Addons d’opéra][OperaAddonsExtensions]  
*   [Microsoft Edge Modules de modules][MicrosoftEdgeAddonsCategoryExtensions]  

Certaines magasins vous permettent de télécharger des extensions répertoriées à partir d’autres navigateurs.  Toutefois, l’accès entre navigateurs n’est pas garanti par les magasins de navigateurs.  Pour vous assurer que vos utilisateurs trouvent votre extension dans différents navigateurs, vous devez conserver une liste sur chaque magasin d’extensions de navigateur.  

Les utilisateurs devront peut-être installer votre extension dans différents navigateurs. Dans ce scénario, vous pouvez migrer des extensions Chromium existantes d’un navigateur à un autre.  

###  <a name="migrate-an-existing-extension-to-microsoft-edge"></a>Migrer une extension existante vers Microsoft Edge  

Si vous avez déjà développé une extension pour un autre navigateur Chromium, vous pouvez la soumettre au magasin Microsoft Edge de modules. Vous n’avez pas besoin de réécrire votre extension et devez vérifier qu’elle fonctionne dans Microsoft Edge.  Lorsque vous migrez une extension Chromium existante vers d’autres navigateurs Chromium, assurez-vous que les mêmes API ou alternatives sont disponibles pour votre navigateur cible.  

Pour plus d’informations sur le portage de votre extension Chrome vers Microsoft Edge, accédez aux [extensions Port Chrome vers Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome] Une fois que vous avez porté votre extension vers le navigateur cible, l’étape suivante consiste à la publier.  

###  <a name="publish-to-the-microsoft-edge-add-ons-website"></a>Publier sur le site modules complémentaires Microsoft Edge web  

Pour commencer à publier votre extension sur [][MicrosoftDeveloperRegistration] Microsoft Edge, vous devez vous inscrire à un compte de développeur auprès d’un compte de messagerie MSA pour soumettre votre liste d’extensions au Store.  Un compte de messagerie MSA `@outlook.com` `@live.com` inclut, etc.  Lorsque vous choisissez une adresse de messagerie à inscrire, pensez à transférer ou partager la propriété de l’extension avec d’autres personnes de votre organisation.  Une fois l’inscription terminée, vous pouvez créer une soumission d’extension au Store.  

Pour envoyer votre extension au Store, veillez à fournir les éléments suivants.  

*   Fichier d’archivage `.zip` \( \) qui contient vos fichiers de code.  
*   Toutes les ressources visuelles requises, qui incluent un logo et une petite vignette promotionnelle.  
*   Médias promotionnels facultatifs, tels que des captures d’écran, des vignettes promotionnelles et une URL vidéo.  
*   Informations qui décrivent votre extension, telles que le nom, la description courte et un lien de stratégie de confidentialité.  

> [!NOTE]
> Différents magasins peuvent avoir des exigences d’envoi différentes.  La liste ci-dessus récapitule les [conditions requises][ExtensionsChromiumPublish] pour publier une extension pour Microsoft Edge.  

Une fois que vous avez envoyé votre extension, elle est soumise à un processus de révision et réussit ou échoue au processus de certification.  Les propriétaires sont avertis du résultat et doivent suivre les étapes suivantes, le cas échéant.  Si vous soumettez une mise à jour d’extension au Store, un nouveau processus de révision est démarré.  

##  <a name="see-also"></a>Articles associés  

*   [Portage d’une extension Google Chrome][ExtensionworkshopPorting]  
*   [Créer une extension d’application Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Votre première extension (Firefox)][MDNWebextensionsYourFirst]  
*   [Didacticiel de mise en place (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Get started (Opera)][OperaDevExtensionsGettingStarted]  
*   [Commencer avec les extensions Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Portage de l’extension Chrome Microsoft Edge (Chromium) | Documents Microsoft"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Getting Started With Microsoft Edge (Chromium) Extensions | Documents Microsoft"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publier une extension | Documents Microsoft"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Développer des extensions pour Microsoft Edge | Développeur Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Développeur Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensions pour Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensions d’application Safari | Développeur Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Création d’une extension d’application Safari | Développeur Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Que sont les extensions ? | Développeur Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Api Chrome | Développeur Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Didacticiel de mise en | Développeur Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portage d’une extension Google Chrome | Atelier d’extension"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensions | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensions de navigateur | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Votre première extension | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensions | Modules de modules pour Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensions | Opéra Addons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentation sur les extensions | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API d’extension prise en charge dans Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Mise en | Dev. Opera"  
