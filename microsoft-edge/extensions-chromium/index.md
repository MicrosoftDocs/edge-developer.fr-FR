---
description: La vue d’ensemble des extensions Microsoft Edge (chrome), ainsi que la création et la publication d’extensions de navigateur en général.
title: Extensions Microsoft Edge (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, développement d’extensions, extensions de navigateur, compléments, centre de partenaires, développeurs et extensions chrome
ms.openlocfilehash: 2c4c34805e93bf6fbae57f1d0230cc821d1f3f65
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684698"
---
# Extensions Microsoft Edge (chrome)  

Une extension est un petit programme que vous \ (le développeur \) peut utiliser pour ajouter de nouvelles fonctionnalités à Microsoft Edge \ (chrome \) ou pour modifier la fonctionnalité existante.  Une extension est conçue pour améliorer l’utilisation de la navigation quotidienne d’un utilisateur en fournissant une fonctionnalité de niche essentielle pour les audiences ciblées.  

Vous pouvez créer des extensions si votre idée ou votre produit dépend de la disponibilité d’un navigateur Web spécifique ou d’une augmentation de l’environnement de navigation où la fonctionnalité que vous souhaitez fournir étend les sites Web existants.  Les exemples d’expériences complémentaires incluent les gestionnaires de AdBlockers et de mots de passe.  

Une extension est structurée de façon similaire à une application Web standard.  Le cas échéant, il inclut un fichier JSON de manifeste de l’application qui contient des informations sur la plateforme de base, un fichier JavaScript pour définir les fonctionnalités, ainsi qu’un fichier HTML et CSS pour déterminer l’apparence de l’interface utilisateur \ (si nécessaire).  Pour travailler directement avec une partie du navigateur, telle qu’une fenêtre ou un onglet, vous devez envoyer des demandes d’API et souvent référencer le navigateur par son nom.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Extension Microsoft Edge (chrome)":::
  Extension Microsoft Edge \ (chrome \)  
:::image-end:::  

## Recommandations de base  

Voici quelques-uns des navigateurs les plus populaires à générer pour inclure Safari, Firefox, chrome, Opera, courage et Microsoft Edge.  Les lieux formidables de début de développement d’extensions et de documentation sont des sites hébergés par les organisations du navigateur.  Le tableau suivant n’est pas définitif, vous pouvez l’utiliser comme point de départ utile.  

| Navigateur web | En chrome? | Page d’accueil du développement d’extensions |  
|:--- |:--- |:--- |  
| Safari | Non | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Non | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Oui | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Oui | [dev.opera.com/extensions][OperaDevExtensions] |  
| Ère | Oui | Utilise le [Web Store chrome][GoogleChromeWebstoreCategoryExtensions] |  
| nouvelle Microsoft Edge | Oui | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Un grand nombre des didacticiels des sites utilisent des API propres au navigateur qui peuvent ne pas correspondre au navigateur pour lequel vous développez.  Dans la plupart des cas, une extension de chrome fonctionne tel quel dans les différents navigateurs de chrome et les API fonctionnent comme prévu.  Seules certaines API moins communes pourront être strictement spécifiques au navigateur.  Pour des liens vers les didacticiels, voir [Voir aussi](#see-also).  

## Pourquoi chrome  

Si vous avez l’intention de publier votre extension sur autant qu’il est possible d’extensions de navigateur, il doit être modifié pour plusieurs versions afin de pouvoir cibler et s’exécuter dans chaque environnement de navigateur distinct.  Les [extensions Safari][AppleDeveloperSafariservicesAppExtensions], contrairement aux autres types d’extension, risquent d’utiliser le code Web et le code natif pour communiquer avec les applications natives de contrepartie.  Les [Extensions Firefox][MDNWebextensions] peuvent être partagées en commun avec les autres types d’extensions, mais il existe également quelques [différences][ExtensionworkshopPorting] à prendre en considération.  Néanmoins, il existe d’excellentes informations; les quatre derniers navigateurs du graphique ci-dessus sont en mesure d’utiliser le même package de code et de réduire les besoins en matière de modification et de conservation des versions parallèles.  En effet, les navigateurs sont basés sur le [projet open-source de chrome][|::ref1::|Home].  

La création d’une extension de chrome vous permet d’écrire le plus petit nombre de codes pour maximiser le nombre de magasins d’extension que vous ciblez, ainsi que le nombre d’utilisateurs capables de rechercher et d’acquérir votre extension.  

Le contenu suivant est essentiellement axé sur les extensions de chrome.  

## Compatibilité des navigateurs et tests d’extension  

Il arrive parfois que la parité API n’existe pas entre les navigateurs de chrome.  Par exemple, il existe des différences dans les API d’identité et de paiement.  Pour vous assurer que votre extension satisfait aux attentes des clients, examinez l’état de l’API par le biais de la documentation du navigateur ( [API chrome][ChromeDeveloperExtensionsApiIndex]), [API d’extension prises en charge dans Opera][OperaDevExtensionsApis]et [de l’extension du chrome de port sur le bord Microsoft (chrome)][ExtensionsChromiumDeveloperGuidePortChrome].  

En fonction des API dont vous avez besoin, ces différences peut signifier que vous devez créer des packages de code légèrement différents en incluant de petites différences dans le code de chaque Store.  

Lorsque vous développez votre extension, vous pouvez l’charger dans votre navigateur pour la tester dans d’autres environnements avant de soumettre votre extension aux magasins de navigateurs.  

## Publier votre extension dans les magasins de navigateur  

Vous pouvez également demander les extensions de navigateur dans les magasins de navigateur suivants.  

*   [Modules complémentaires de navigateur Firefox][MozillaAddonsFirefoxExtensions]  
*   [Magasin Web chrome][GoogleChromeWebstoreCategoryExtensions]  
*   [Compléments Opera][OperaAddonsExtensions]  
*   [Modules complémentaires Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Certains magasins vous permettent de télécharger les extensions répertoriées à partir d’autres navigateurs.  Le téléchargement à partir d’un autre navigateur peut vous éviter d’avoir besoin d’enregistrer votre travail dans les autres magasins si les utilisateurs sont en mesure d’accéder aux descriptions existantes dans les différents navigateurs.  Toutefois, l’accès multiplateforme n’est pas garanti par les magasins de navigateurs.  Pour vous assurer que vos utilisateurs peuvent trouver votre extension dans différents navigateurs, vous devez conserver une liste sur chaque magasin d’extensions de navigateur.  

Une extension peut avoir des audiences chevauchantes qui utilisent souvent plusieurs navigateurs, ou vous pouvez découvrir qu’elle doit cibler un public qui ne l’a pas encore fait.  Pour que cela se produise, les extensions de chrome peuvent être déplacées d’un navigateur à un autre.  

### Migrer une extension existante vers Microsoft Edge  

Si vous avez déjà créé une extension pour un autre navigateur de chrome et que vous souhaitez l’offrir et garantir son fonctionnement par le biais de Microsoft Edge, il n’est pas nécessaire de réécrire votre extension.  La migration d’extensions de chrome existantes vers d’autres navigateurs de chrome est simple tant que les API que vous utilisez sont disponibles dans différents navigateurs ou dans d’autres API qui fournissent les fonctionnalités nécessaires.  

Pour plus d’informations sur le portage de votre extension chrome, voir [extensions de chrome de port vers Microsoft Edge][ExtensionsChromiumDeveloperGuidePortChrome].  Une fois que vous avez porté votre extension vers le navigateur cible, l’étape suivante consiste à la publier.  

### Publication sur le site Web des modules complémentaires Microsoft Edge  

Pour commencer à publier votre extension sur Microsoft Edge, vous devez vous [inscrire à un compte de développeur][MicrosoftDeveloperRegistration] doté d’un compte de messagerie MSA \ (@outlook. com, @live. com, etc.) pour envoyer votre description de l’extension dans le Windows Store.  Lors du choix d’une adresse de messagerie à inscrire, envisagez de transférer ou de partager le propriétaire de l’extension avec d’autres membres de votre organisation.  Une fois l’enregistrement terminé, vous pouvez créer une soumission d’extension dans le Windows Store.  

Pour transmettre votre extension au Windows Store, vous devez disposer de la configuration requise suivante.  

*   Un fichier archive (. zip) qui contient vos fichiers de code.  
*   Toutes les ressources visuelles requises, qui comprennent un logo et une petite vignette promotionnelle.  
*   Éléments multimédias promotionnels facultatifs, tels que des captures d’écran, des vignettes promotionnelles plus grandes, une URL ou n’importe quelle combinaison de vidéos de votre extension.  
*   Des informations qui décrivent votre extension, telles que le nom, la description courte, la description longue et un lien vers votre politique de confidentialité.  

> [!NOTE]
> Il est possible que les différentes banques aient différentes exigences de soumission.  La liste ci-dessus résume la [Configuration requise][ExtensionsChromiumPublish] pour la publication d’une extension dans Microsoft Edge.  

Lorsque vous avez terminé le processus de soumission, votre extension est examinée et le processus de certification est transmis ou échoue.  Les propriétaires sont avertis du résultat et en suivant les étapes suivantes, le cas échéant.  Si vous soumettez une extension mise à jour au Windows Store, y compris des mises à jour apportées aux détails de la liste d’extensions, un nouveau processus de révision est lancé.  

## Voir également  

*   [Portage d’une extension Google Chrome][ExtensionworkshopPorting]  
*   [Création d’une extension d’application Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Votre première extension (Firefox)][MDNWebextensionsYourFirst]  
*   [Didacticiel de mise en route (chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Mise en route (Opera)][OperaDevExtensionsGettingStarted]  
*   [Premiers pas avec les extensions Microsoft Edge (chrome)][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Extension du chrome port sur le bord Microsoft (chrome) | Documents Microsoft"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Premiers pas avec les extensions Microsoft Edge (chrome) | Documents Microsoft"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publier une extension | Documents Microsoft"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Développement d’extensions pour Microsoft Edge | Développeur Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Centre de partenariat | Développeur Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensions pour Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensions de l’application Safari | Développeur Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Création d’une extension d’application Safari | Développeur Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Présentation des extensions Développeur de chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "API chrome | Développeur de chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Didacticiel de mise en route | Développeur de chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Hexavalent"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portage d’une extension Google Chrome | Ateliers d’extension"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensions | Magasin Web chrome"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensions de navigateur | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Votre première extension | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensions | Modules complémentaires pour Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensions | Compléments Opera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentation sur les extensions | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API d’extension prises en charge dans Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Mise en route | Dev. Opera"  
