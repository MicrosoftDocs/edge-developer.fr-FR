---
description: Obtenez une vue d’ensemble de bout en bout du voyage entre le début du développement et l’empaquetage d’extensions Microsoft Edge.
title: Extensions-mise en route
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, extensions
ms.openlocfilehash: 5d2bf0ea2236e36b9e6205e13291ffee4118d9d7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565383"
---
# Premiers pas avec les extensions  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Que vous soyez un nouveau développeur souhaitant vous familiariser avec les extensions ou un ancien combattant grâce à une extension chrome que vous souhaitez porter, ce guide contient toutes les informations dont vous avez besoin pour développer, tester, empaqueter et publier une extension pour Microsoft Edge. 

## Développement d’une extension

La première étape consiste à créer une extension Microsoft Edge: 
- Vous débutez avec les extensions? Consultez notre [Guide sur la création d’extensions](./guides/creating-an-extension.md) pour plus d’informations sur la création de votre première extension de navigateur. 
- Vous connaissez déjà les API d’extension? Consultez notre documentation sur la [prise en charge](./api-support.md) de l’API pour obtenir les dernières informations sur les API prises en charge/en développement. 
- Vous souhaitez porter une extension chrome vers Microsoft Edge? Essayez le [Kit de connaissances Microsoft Edge extension](./guides/porting-chrome-extensions.md).

## Chargement et débogage

Une fois que vous avez une extension qui fonctionne dans Microsoft Edge, vous pouvez la charger latéralement pour la voir en action. Pour cela, la première étape consiste à vérifier que vous avez [activé les fonctionnalités de développement d’extensions](./guides/adding-and-removing-extensions.md). Cela vous permettra de charger les fichiers d’extension dans Microsoft Edge afin de pouvoir tester votre extension lors de sa création. Si vous rencontrez des problèmes, les outils de développement F12 vous permettent de [déboguer les différents contextes de votre extension](./guides/debugging-extensions.md) pour déterminer exactement ce qui se passe. Vous rencontrez encore des problèmes? Notre [Guide de résolution des problèmes propose des](./troubleshooting.md) solutions à plusieurs pièges courants. 

## Signaler des bogues et obtenir de l’aide

Imaginons que vous ayez trouvé un bogue dans notre plateforme d’extensions? Si le problème est spécifique à Microsoft Edge, recherchez-le dans notre service de [suivi des problèmes Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/issues/) pour savoir s’il a déjà été signalé. Si c’est bien! Vous pouvez appuyer sur le bouton «+ moi» pour envoyer le bogue et le bouton «regarder ce problème pour les mises à jour» pour être averti de toute modification apportée au problème. Si vous ne trouvez pas le problème que vous rencontrez, n’hésitez pas à ouvrir un nouveau problème et fournir autant d’informations que possible pour que nos développeurs y aient accès. 

Est-il manquant une API que votre extension doit fonctionner correctement? Si tel est [le cas, nous sommes toujours à l’écoute de UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). N’hésitez pas à voter votre API s’il existe déjà, ou pour créer un nouvel élément de commentaires de sorte que d’autres développeurs puissent le voter. 

Vous avez des questions auxquelles vous ne trouvez pas de réponse dans la documentation? Nous vous conseillons vivement de rejoindre la [communauté d’extensions Microsoft Edge](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) sur le débordement de pile et de lui demander le service informatique.

## Test de votre extension

Dans le cadre de la mise à jour anniversaire de Windows, [Microsoft WebDriver](../dev-guide/tools/webdriver.md) prend en charge le chargement automatisé des extensions dans les sessions Microsoft Edge. Cela vous permet d’écrire des tests simples pour s’assurer que toute extension destinée à modifier une page le fait de la façon escomptée. Pour plus d’informations sur la façon de procéder, consultez notre [Guide de test](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver). De plus, restez informé des mises à jour à mesure que nous prévoyons d’ajouter des fonctionnalités spécifiques à l’extension à Microsoft WebDriver à l’avenir.

## Ajouter les touches finales

Votre extension fonctionne donc dans Microsoft Edge. Que se passe-t-il? Avant de continuer à empaqueter votre extension, nous vous conseillons de consulter ces guides pour vous assurer que votre extension suit nos meilleures pratiques: 
- Assurez-vous que vos icônes d’extension sont [correctement dimensionnées](./guides/design.md) et [accessibles](./guides/accessibility.md) (c’est-à-dire qu’elles sont visibles dans les thèmes clairs et sombres de Microsoft Edge ainsi que dans le mode contraste élevé). 
- Si votre extension doit prendre en charge plusieurs langues, assurez-vous d’avoir consulté notre [Guide international](./guides/internationalization.md). 

## Empaquetage d’une extension

À présent, votre extension est finalement impeccable et prête à être empaquetée. Que vous souhaitiez créer un package pour préparer la soumission à la boutique Microsoft ou faciliter la distribution au sein de vos équipes de développement et de test, il existe de nombreuses ressources disponibles pour vous aider: 

- Notre solution recommandée pour la création d’un package d’extension consiste à suivre notre [Guide d’emballage de ManifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) , qui vous guidera tout au long des étapes d’utilisation d’un outil de création de nœud. js pour empaqueter facilement votre extension, quelle que soit la plateforme sur laquelle vous développez. Si vous avez besoin d’une présentation plus détaillée et détaillée de notre format d’emballage d’extension, consultez notre [Guide de création de package AppX](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder). 
- Si votre extension prend en charge plusieurs langues, vous devez également suivre notre guide sur la [localisation des packages d’extension](./guides/packaging/localizing-extension-packages.md) pour que les langues que vous avez dans votre extension soient correctement enregistrées après l’emballage. 

Si vous êtes un client d’entreprise cherchant à distribuer vos extensions empaquetées via des canaux internes, consultez notre [Guide sur les extensions pour les entreprises](./extensions-for-enterprise.md) pour découvrir comment procéder.  

## Publication sur le Microsoft Store

Comme notre plate-forme d’extensions est toujours incomplète, nous sommes en mesure de gérer les soumissions de poste sur le Microsoft Store, afin que nous puissions vous concentrer sur la fourniture d’une qualité d’utilisation pour nos utilisateurs et nos développeurs. C’est pourquoi nous voulons que les développeurs publient le plus facilement possible leurs extensions. Par conséquent, nous avons récemment lancé un nouveau [formulaire de soumission d’extension](https://aka.ms/extension-request) dans lequel les développeurs peuvent demander l’autorisation de soumettre leur extension AppX au Microsoft Store.
 

La première étape du processus de publication consiste à veiller à ce que votre extension soit conforme à la [stratégie d’extension du navigateur](./microsoft-browser-extension-policy.md) ainsi qu’à la [section Microsoft Edge extensions des politiques du Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12). 

Une fois que vous avez confirmé que votre extension suit les stratégies, vous devez vous inscrire pour obtenir un [compte de développeur dans le centre de partenariat et réserver le nom de votre extension](./guides/packaging/extensions-in-the-windows-dev-center.md). Ensuite, vous devez soumettre une demande par le biais de notre [formulaire de soumission d’extension](https://aka.ms/extension-request) afin de demander l’autorisation de publier sur le Microsoft Store. Si vous essayez d’envoyer votre extension AppX sans d’abord obtenir l’autorisation, vous recevez le message d’erreur suivant:

`Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.`

Une fois que vous avez envoyé une demande, nous recevrons une notification et tenterons d’accéder à votre soumission le plus rapidement possible. Cela peut prendre un certain temps en raison du volume élevé de soumissions que nous avons reçu, mais nous vous informerons par courrier électronique du moment où vous êtes approuvé. Après avoir reçu le message, vous pouvez envoyer votre extension AppX au Microsoft Store via le centre de partenariat. Veuillez noter que vous n’avez pas besoin de signer votre AppX avant de l’envoyer; le processus d’intégration de Microsoft Store s’en charge.
 
> [!NOTE]
> Le processus de publication d’une extension sur le Microsoft Store (qu’il s’agisse d’une nouvelle extension ou d’une mise à jour d’une extension existante) peut durer jusqu’à 72 heures. Pour accélérer ce processus, assurez-vous que vous avez vérifié les problèmes courants suivants avant de procéder à la soumission pour éviter d’avoir à soumettre de nouveau votre soumission ultérieure: 
> - Vos captures d’écran sont correctement dimensionnées et sont celles de votre extension exécutée dans Microsoft Edge 
> - La description de votre extension fait référence à «Microsoft Edge» au lieu de «Edge» (il s’agit d’une exigence légale) 
> - Votre 150 x 150 icône dans votre package d’extension n’est pas associée à [un arrière-plan transparent](./guides/design.md#microsoft-store-icon) (le client Microsoft Store ne restitue pas correctement les images avec des arrière-plans transparents) 

Outre les informations ci-dessus, et le cas échéant, vérifiez que les informations de disponibilité de la plateforme sur votre site Web mentionnent correctement la disponibilité de votre extension sur Microsoft Edge. Même si le Microsoft Store n’autorise pas les installations en ligne d’un clic, vous pouvez créer [des liens hypertexte vers votre extension dans le Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) pour faciliter l’acquisition. 

Le Microsoft Store vous permet également de [contrôler la visibilité de votre extension](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) dans le catalogue Microsoft Store. Certains de nos partenaires ont tiré profit de cette fonctionnalité pour accomplir les tâches suivantes: 
- Publication d’une deuxième version bêta de leur extension telle qu’elle est cachée dans le Microsoft Store.
- À l’origine de la publication de leur extension comme étant cachée pour surveiller la télémétrie initiale avant de modifier son statut sur visible une fois un certain niveau de confiance atteinte.

## Et voilà!

Si vous avez atteint la fin de ce guide, vous avez terminé le processus de développement d’une extension pour Microsoft Edge. N’hésitez pas à consulter notre page [conseils et astuces](./tips-and-tricks.md) pour découvrir comment commercialiser votre extension et communiquer avec vos utilisateurs.
