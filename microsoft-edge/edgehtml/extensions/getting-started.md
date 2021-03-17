---
description: Obtenez une vue d’ensemble de bout en bout du processus de développement depuis le début jusqu’à l’empaquetage des extensions Microsoft Edge.
title: 'Extensions : mise en place'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, javascript, développeur, extensions
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 52d0aa5c1968518194a4e3b90cb0cc876d0c7f86
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439716"
---
# <a name="getting-started-with-extensions"></a>Mise en place des extensions  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Que vous êtes un nouveau développeur souhaitant vous familiariser avec les extensions ou un expérimenté expérimenté avec une extension Chrome que vous souhaitez porter, ce guide contient toutes les informations dont vous avez besoin pour développer, tester, créer un package et publier une extension pour Microsoft Edge. 

## <a name="developing-an-extension"></a>Développement d’une extension

La première étape de ce parcours consiste à créer une extension Microsoft Edge : 
- Nouveauté des extensions ? Consultez notre [guide sur la création d’extensions](./guides/creating-an-extension.md) pour plus d’informations sur la création de votre première extension de navigateur ! 
- Déjà familiarisé avec les API d’extension ? Consultez notre [documentation de prise en](./api-support.md) charge des API pour obtenir les dernières informations sur les API qui sont pris en charge/en cours de développement. 
- Vous avez une extension Chrome que vous souhaitez porter vers Microsoft Edge ? Essayez [l’extension Microsoft Edge Shared Computer Toolkit](./guides/porting-chrome-extensions.md)!

## <a name="loading-and-debugging"></a>Chargement et débogage

Une fois que vous avez une extension qui fonctionne dans Microsoft Edge, chargez-la de côté pour la voir en action. La première étape consiste à vous assurer que les fonctionnalités de développement [d’extension sont activées.](./guides/adding-and-removing-extensions.md) Cela vous permettra de charger des fichiers d’extension de côté dans Microsoft Edge afin de pouvoir tester votre extension lors de son développement. En cas de problème, les outils de développement F12 vous permettent de déboguer les différents [contextes](./guides/debugging-extensions.md) de votre extension pour déterminer exactement ce qui se passe. Vous avez encore des problèmes ? Notre [guide de résolution des problèmes offre](./troubleshooting.md) des solutions à plusieurs gotchas courantes. 

## <a name="reporting-bugs-and-getting-help"></a>Signalement des bogues et obtention d’aide

Pensez-vous avoir trouvé un bogue dans notre plateforme d’extensions ? Si le problème est spécifique à Microsoft Edge, recherchez-le dans notre suivi des problèmes [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/issues/) pour voir s’il a déjà été signalé. Si c’est le cas, c’est bien ! Vous pouvez appuyer sur le bouton « + Moi aussi » pour lever le bogue et le bouton « Surveiller ce problème pour les mises à jour » pour être averti des modifications apportées au problème. Si vous ne trouvez pas le problème que vous recherchez, n’hésitez pas à ouvrir un nouveau problème et à fournir autant d’informations que possible afin que nos développeurs peuvent l’examiner. 

<!--Are we missing an API that your extension needs to work properly? If so, [we're always listening on UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). Feel free to upvote your API if it already exists, or to create a new feedback item so that other developers can upvote it too! -->  

Avez-vous une question à qui vous ne trouvez pas de réponse dans la documentation ? Nous vous recommandons vivement de rejoindre la communauté [des extensions Microsoft Edge](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) sur Stack Overflow et de le lui demander !

## <a name="testing-your-extension"></a>Test de votre extension

À la mise à jour anniversaire Windows, [Microsoft WebDriver](../webdriver/index.md) prend en charge le chargement latéral automatisé des extensions dans les sessions Microsoft Edge. Cela vous permettra d’écrire des tests simples pour vous assurer que toute extension destinée à modifier une page le fait de la manière attendue. Vous trouverez plus d’informations sur la façon de le faire dans notre [guide de test.](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver) Restez également informé des mises à jour, car nous prévoyons d’ajouter d’autres fonctionnalités spécifiques à l’extension à Microsoft WebDriver à l’avenir.

## <a name="adding-the-final-touches"></a>Ajout des touches finales

Votre extension fonctionne donc dans Microsoft Edge. Que se passe-t-il ensuite ? Avant de continuer à empaqueter votre extension, nous vous recommandons vivement de consulter ces guides pour vous assurer que votre extension suit nos stratégies recommandées : 
- Assurez-vous que vos [](./guides/design.md) icônes d’extension sont correctement re mesure et accessibles (ce qui signifie qu’elles sont [visibles](./guides/accessibility.md) dans les thèmes clair et foncé de Microsoft Edge, ainsi qu’en mode de contraste élevé). 
- Si votre extension doit prendre en charge plusieurs langues, assurez-vous que vous avez pris en compte notre [guide d’internationalisation.](./guides/internationalization.md) 

## <a name="packaging-an-extension"></a>Empaquetage d’une extension

Votre extension est enfin prête à être empaqueté. Que vous souhaitiez le mettre en package pour préparer sa soumission au Microsoft Store ou pour faciliter sa distribution au sein de vos équipes de développement/test, de nombreuses ressources sont disponibles pour vous aider : 

- Pour créer un package d’extension, nous vous recommandons de suivre notre guide d’empaquetage [ManifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) qui vous guidera dans les étapes d’utilisation d’un outil basé sur Node.js pour empaqueter facilement votre extension, quelle que soit la plateforme sur laquelle vous développez. Si vous souhaitez un examen plus manuel et approfondi de notre format d’empaquetage d’extension, reportez-vous à notre guide de création de [package AppX.](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder) 
- Si votre extension prend en charge plusieurs langues, vous devez également suivre notre guide sur la localisation des [packages d’extension afin](./guides/packaging/localizing-extension-packages.md) que les langues que vous avez dans votre extension soient correctement inscrites après l’empaquetage. 

Si vous êtes un client d’entreprise cherchant à distribuer vos extensions empaquetées via des canaux internes, consultez notre guide des [extensions](./extensions-for-enterprise.md) pour entreprise pour voir comment faire.  

## <a name="publishing-to-the-microsoft-store"></a>Publication dans le Microsoft Store

Étant donné que notre plateforme d’extensions est toujours en cours d’int ation, nous gérons de manière volontaire les envois d’extensions au Microsoft Store afin de pouvoir nous concentrer sur la livraison d’une expérience de qualité pour nos utilisateurs et développeurs. Cela étant dit, nous voulons que les développeurs publient leurs extensions aussi facilement que possible. Par conséquent, nous avons récemment lancé un nouveau formulaire de soumission [d’extension](https://aka.ms/extension-request) dans lequel les développeurs peuvent demander l’autorisation de soumettre leur extension AppX au Microsoft Store.
 
La première étape du processus de publication consiste à vous assurer que votre extension est conforme à notre stratégie **d’extension** de navigateur, ainsi qu’à la [section extensions Microsoft Edge](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)des stratégies du Microsoft Store.  

<!--  The first step of the publishing process is to make sure your extension conforms to our [browser extension policy](./microsoft-browser-extension-policy.md) as well as the [Microsoft Edge extensions section of the Microsoft Store Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).  -->  

Une fois que vous avez confirmé que votre extension suit les stratégies, vous devez vous inscrire pour un compte de développeur dans l’Partner Center et réserver le nom [de votre extension](./guides/packaging/extensions-in-the-windows-dev-center.md). Ensuite, vous devez envoyer une demande via notre formulaire de soumission [d’extension](https://aka.ms/extension-request) afin de demander l’autorisation de publier sur le Microsoft Store. Si vous essayez d’envoyer votre extension AppX sans obtenir d’autorisation préalable, vous recevrez l’erreur suivante :

```text
Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.
```  

Une fois que vous avez envoyé une demande, nous recevons une notification et nous essayons d’obtenir votre soumission dès que possible. Cela peut prendre un peu de temps en raison du volume élevé de soumissions que nous avons reçues, mais nous vous en informerons par courrier électronique dès que vous serez approuvé ! Une fois que vous avez reçu le courrier, vous pouvez envoyer votre extension AppX au Microsoft Store via l’Partner Center. Notez que vous n’avez pas besoin de signer votre AppX avant de l’envoyer . Le processus d’ingestion du Microsoft Store s’en chargera pour vous !
 
> [!NOTE]
> Le processus de publication d’une extension dans le Microsoft Store (qu’il s’agit d’une toute nouvelle extension ou d’une mise à jour vers une extension existante) peut prendre jusqu’à 72 heures. Afin d’accélérer ce processus, assurez-vous que vous avez vérifié ces gotchas courantes avant de soumettre pour éviter d’avoir à soumettre à nouveau ultérieurement : 
> - Vos captures d’écran sont correctement re taille et sont de votre extension en cours d’exécution dans Microsoft Edge 
> - La description de votre extension fait référence à « Microsoft Edge » au lieu de « Edge » (il s’agit d’une exigence légale) 
> - Votre icône 150 x 150 dans votre package d’extension [n’a](./guides/design.md#microsoft-store-icon) pas d’arrière-plan transparent (le client du Microsoft Store ne restituera pas correctement les images avec des arrière-plans transparents) 

En plus des informations ci-dessus et le cas échéant, assurez-vous que toutes les informations de disponibilité de plateforme sur votre site web mentionnent correctement la disponibilité de votre extension sur Microsoft Edge. Bien que le Microsoft Store n’autorise pas les installations d’extensions en ligne en un clic, vous pouvez établir un lien profond avec votre extension dans le Microsoft Store pour faciliter l’acquisition de [l’extension](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) par les utilisateurs. 

Le Microsoft Store vous permet également de contrôler la visibilité de votre [extension](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) dans le catalogue du Microsoft Store. Certains de nos partenaires ont tiré parti de cette fonctionnalité pour obtenir les avantages suivants : 
- Publication d’une deuxième version bêta de son extension comme masquée dans le Microsoft Store.
- Publication initiale de leur extension comme masquée pour surveiller la télémétrie initiale avant de modifier son état pour qu’il soit visible une fois qu’un certain niveau de confiance est atteint.

## <a name="thats-it"></a>Et voilà!

Si vous avez atteint le bas de ce guide, vous avez terminé le processus de développement d’une extension pour Microsoft Edge ! N’oubliez pas de consulter notre page [de conseils](./tips-and-tricks.md) et d’astuces pour obtenir des idées sur la manière de commercialiser votre extension et d’interagir avec vos utilisateurs.
