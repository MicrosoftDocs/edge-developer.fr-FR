---
description: Publiez les extensions Microsoft Edge (chrome) sur le magasin de modules complémentaires Microsoft Edge.
title: Publier votre extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 4f8433e74c0fd6dab3278792b94cf3cbaac05d2c
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015750"
---
# Publier votre extension  

Après avoir terminé le développement et le test de votre extension, il est possible que vous soyez prêt à distribuer votre extension à l’aide du catalogue des modules complémentaires Microsoft Edge.  Par ailleurs, si vous disposez d’une extension de chrome que vous voulez mettre à la disposition des utilisateurs Microsoft Edge, vous pouvez [porter votre extension de chrome actuelle][PortChromiumExtension] vers Microsoft Edge.  

La publication de votre extension dans le catalogue des modules complémentaires Microsoft Edge augmente la portée de votre extension et rend celle-ci disponible pour les utilisateurs finaux.  Cette rubrique fournit une procédure pas à pas illustrant le processus de soumission de votre extension au catalogue de modules complémentaires Microsoft Edge.  

## Avant de commencer  

À ce stade, vous devez être prêt à utiliser votre extension.  Pour plus d’informations sur la création d’une extension, voir le [didacticiel de mise en route][ExtensionsGettingStarted].  

Pour publier votre extension sur le site Web des modules complémentaires Microsoft Edge, vous devez disposer d’un compte de développeur actif dans le [Centre des partenaires][MicrosoftPartnerCenter].  Pour ouvrir un nouveau compte de développeur et vous inscrire au programme de modules complémentaires Microsoft Edge, suivez la procédure décrite dans le guide [d’inscription du développeur][DeveloperRegistration] .  

Créez un fichier zip qui représente votre package d’extension.  Votre package d’extension doit inclure les fichiers suivants.  

*   Le manifeste de l’extension spécifiant des détails tels que le nom de l’extension, une brève description, des autorisations et une langue par défaut.  
*   Images et autres fichiers requis par votre extension.  

Les champs suivants du manifeste sont inclus automatiquement dans les détails de votre description dans le Windows Store et ne peuvent pas être modifiés à partir de la page de description du Windows Store décrite plus loin dans cette rubrique.  Vérifiez que les champs sont remplis pour correspondre à l’affichage de votre choix dans la page de détails du magasin avant de télécharger votre package vers le Centre des partenaires.  Pour obtenir un exemple de code requis pour le fichier manifeste, voir notions de base du fichier manifeste.  

*   `Name` dans le fichier manifeste, qui est le **nom d’affichage** de la page de détails du magasin.  
*   `Description` dans le fichier manifeste, il s’agit de la **description courte** dans la page Détails du magasin.  Entrez une brève description à afficher en haut de la liste pour votre extension.  Dans le cas contraire, la description courte spécifiée dans le fichier manifeste de l’extension s’affiche dans votre description dans le Windows Store.  Si une brève description n’est pas incluse dans le fichier manifeste, les premières lignes de la description s’affichent.  Nous vous conseillons de fournir une brève description pour éviter le réaffichage du contenu de la page de description dans le Windows Store.  

## Envoyez votre extension au magasin de modules complémentaires Microsoft Edge  

Pour renvoyer votre extension au [Centre de partenariat][MicrosoftPartnerCenter], procédez comme suit.  

#### Étape 1: commencer une nouvelle soumission  

Accédez au [tableau de bord du développeur][MicrosoftPartnerCenter] et sélectionnez créer une **nouvelle extension** sur la page **vue d’ensemble** .  

#### Étape 2: Télécharger le package d’extension  

Utilisez la page **packages** pour télécharger le fichier zip de votre package d’extension.  Vous ne pouvez télécharger qu’un seul package à la fois.  Vous ne pouvez pas continuer avec la soumission si le chargement du package échoue sur la page **packages** .  

Chargez le package en le faisant glisser vers le champ charger, ou en sélectionnant **parcourir vos fichiers**.  Une fois le package téléchargé, votre package est validé.  Une fois la validation réussie, passez en revue les détails de l’extension, puis sélectionnez **suivant** pour continuer.  S’il existe des erreurs de validation, résolvez les problèmes et recommencez le téléchargement.  

#### Étape 3: fournir des informations de disponibilité  

Dans la page **disponibilité** , entrez les informations suivantes sur la disponibilité de votre extension.  

##### Visibilité  

Choisissez une des options de visibilité suivantes pour définir si votre extension est détectable dans le catalogue des modules complémentaires Microsoft Edge.  

*   `Public` \ (par défaut \)  
    Public permet de détecter les extensions de tout le monde via la recherche, de parcourir le catalogue des modules complémentaires Microsoft Edge ou d’utiliser l’URL de listing pour votre extension dans le magasin des modules complémentaires Microsoft Edge.  L’URL du listing est disponible dans le tableau de bord du centre de partenaires sur la page **vue d’ensemble** de l’extension.  

*   `Hidden`  
    Hidden supprime les extensions des résultats de la recherche ou navigation dans le catalogue des modules complémentaires Microsoft Edge.  Pour distribuer les extensions cachées dans le magasin des modules complémentaires Microsoft Edge, vous devez partager l’URL de l’entrée auprès de vos clients.  

> [!NOTE]
> Vous pouvez modifier la visibilité de votre poste du **public** en le **masquant**.  Les utilisateurs qui ont installé votre extension alors que la visibilité a été définie sur publique permettent de conserver l’accès à votre extension et de recevoir les mises à jour que vous apportez par le biais du site Web des modules complémentaires Microsoft Edge.  

##### Marchés  

Définissez les marchés spécifiques dans lesquels vous envisagez de fournir votre extension.  Par défaut, tous les marchés sont sélectionnés, y compris les marchés futurs ajoutés plus tard.  Vous pouvez également choisir des marchés spécifiques en sélectionnant **changer de marché**.  Vous pouvez désélectionner des marchés spécifiques pour les exclure, ou sélectionner **Tout désélectionner** , puis ajouter les marchés de votre choix.  

> [!NOTE]
> Vous pouvez modifier les marchés pour lesquels votre extension est proposée.  Les utilisateurs qui ont installé votre extension alors qu’ils étaient disponibles sur leur marché peuvent conserver votre extension.  Toutefois, vos utilisateurs ne peuvent plus accéder aux mises à jour ultérieures envoyées au catalogue des modules complémentaires Microsoft Edge.  

Cliquez sur **Enregistrer** pour accéder à la section **Propriétés** .  

#### Étape 4: sélectionner les propriétés pour votre extension  

Dans la **page Propriétés**, entrez les informations suivantes pour spécifier les propriétés de votre extension.  Les propriétés sont affichées aux utilisateurs dans le catalogue des modules complémentaires Microsoft Edge.  

| Nom de la propriété d’extension | Description |  
|:--- |:--- |  
| Category (obligatoire) | La catégorie qui décrit le mieux votre extension.  La liste de vos extensions dans la catégorie appropriée permet aux utilisateurs de trouver facilement votre extension et d’en savoir plus à son sujet.  |  
| Conditions de politique de confidentialité \ (obligatoire \) | Indiquez si votre extension accède à une extension, recueille ou transmet des informations personnelles.  Votre extension risque de ne pas être à l’étape de certification si vous choisissez **Oui** et que vous ne fournissez pas de `Privacy policy URL` .  |  
| URL de la politique de confidentialité | Une URL de politique de confidentialité valide pour communiquer le mode de conformité de votre extension aux lois et réglementations en matière de confidentialité.  Le cas échéant, vous êtes responsable de la conformité de votre extension aux lois et réglementations en matière de vie privée.  Fournissez une URL de politique de confidentialité si des informations personnelles sont consultées, transmises ou collectées par votre extension.  Pour savoir si votre extension nécessite une politique de confidentialité, consultez le [contrat du développeur Microsoft Edge][MicrosoftAppDeveloperAgreement] et les stratégies pour les [développeurs de catalogue des modules complémentaires Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  
| URL du site Web | Page Web qui fournit des informations supplémentaires sur votre extension.  Le `Website URL` point d’interrogation doit pointer vers une page de votre propre site Web, et non vers la liste de vos extensions dans le catalogue des modules complémentaires Microsoft Edge.  Le `Website URL` permet aux utilisateurs d’en savoir plus sur votre extension, ses fonctionnalités et toutes les autres informations utiles.  |  
| Coordonnées du support technique | URL de votre page Web d’assistance ou l’adresse de messagerie de votre équipe de support technique.  |  
| Contenu mûr | Activez cette case à cocher pour spécifier si votre extension inclut du contenu mûr.  Le classement des extensions permet de déterminer le groupe d’âge approprié du public cible de votre poste.  Pour vous aider à déterminer si le contenu de votre extension est mature, consultez la rubrique [stratégies pour les développeurs de catalogue de modules complémentaires Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Cliquez sur **Enregistrer** pour accéder à la section descriptions dans le Windows **Store** .  

#### Étape 5: ajouter les détails de la description dans le Windows Store pour votre extension  

Les informations fournies dans la section suivante sont affichées aux utilisateurs qui visitent votre annonce dans le catalogue des modules complémentaires Microsoft Edge.  Même si certains champs sont facultatifs, vous devez fournir autant d’informations que possible.  Les informations minimales requises pour votre extension de la liste dans le Windows Store, pour chaque langage mentionné dans votre package d’extension, sont la **Description** et le **logo du magasin d’extensions**.  

> [!NOTE]
> Les détails obligatoires de la description dans le Windows Store doivent être remplis pour chaque langue mentionnée dans votre package zip de poste.  Pour ajouter ou supprimer des langues dans votre description dans le Windows Store dans le catalogue des modules complémentaires Microsoft Edge, vous devez modifier la liste des langues prises en charge par votre extension dans le package d’extension, créer un package d’extension et le télécharger à nouveau.  

| Nom de la propriété de description dans le Windows Store | Description |  
|:--- |:--- |  
| Langues de la description dans le Windows Store \ (obligatoire \) | Sélectionnez une langue dans la liste déroulante **langues** et entrez les détails de la description dans le Windows Store pour cette langue.  Les extensions prenant en charge plusieurs langues doivent fournir une page de description dans le Windows Store pour chaque langue prise en charge.  |  
| Nom d’affichage \ (obligatoire \) | Nom de votre extension spécifié dans le fichier manifeste de votre extension.  Pour modifier le nom d’affichage du Windows Store après soumission, vous pouvez mettre à jour le nom dans le fichier manifeste, créer un nouveau package d’extension, puis le télécharger à nouveau.  |  
| Description \ (obligatoire \) | Le champ de description est axé sur l’explication de l’utilité de votre poste, la raison pour laquelle les utilisateurs l’installent ou les informations pertinentes que les utilisateurs doivent savoir.  Elle doit être inférieure à 10 000 caractères.  |  
| Logo de magasin d’extensions \ (obligatoire \) | Image représentant le logo de votre société ou extension avec des proportions de 1 et de taille recommandée de 300 x 300 pixels.  |  
| Petite vignette promotionnelle \ (facultatif \) | L' `Small promotional tile` image est utilisée pour afficher votre extension en même temps que d’autres extensions dans le Windows Store.  La taille de l’image doit être de 440 x 280 pixels.  |  
| Captures d’écran | Vous pouvez fournir un maximum de 10 captures d’écran décrivant en détail les fonctionnalités de votre extension.  La taille des captures d’écran doit être de 640 x 480 pixels ou 1280 x 800 pixels.  |  
| Grande vignette promotionnelle \ (facultatif \) | Les vignettes de grande taille sont utilisées de façon plus claire dans le Windows Store et les extensions de fonctionnalités sur le site Web des modules complémentaires Microsoft Edge.  Les images, si soumises, sont visibles par les utilisateurs.  La taille des fichiers PNG doit être de 1400 x 560 pixels.  |  
| URL de la vidéo YouTube \ (facultatif \) | Vous pouvez inclure une vidéo de votre poste YouTube.  La `YouTube video URL` vidéo est affichée dans la page de description du Windows Store de votre extension.  |  
| Brève description \ (obligatoire \) | Pour modifier la brève description, vous devez mettre à jour le champ de description dans votre fichier manifeste de votre package d’extension et le télécharger à nouveau.  |  
| Termes de recherche \ (facultatif \) | Les termes de recherche sont des mots ou des phrases uniques qui aident les utilisateurs à découvrir votre extension lors de la recherche dans le catalogue des modules complémentaires Microsoft Edge.  Les termes de recherche ne sont pas affichés aux utilisateurs.  |  

##### Exigences relatives aux URL vidéo YouTube  

Assurez-vous que votre vidéo répond à la configuration requise suivante.  

*   Vérifiez que le contenu de la vidéo YouTube est compatible avec la rubrique [stratégies développeurs du catalogue Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies] .  
*   Désactivez les annonces dans votre vidéo.  Pour plus d’informations, accédez à [la rubrique définir vos formats publicitaires et annonces par défaut dans les][GoogleYoutubeAnswer2531367Topic7072227] [vidéos incorporées][GoogleYoutubeAnswer132596].  
*   Activez l’incorporation pour vos vidéos.  Pour plus d’informations, accédez à [incorporer des vidéos & playlists][GoogleYoutubeAnswer171780].  

Pour transmettre l’URL vidéo YouTube de votre vidéo, procédez comme suit.  

1.  Sur YouTube, recherchez la vidéo que vous voulez ajouter à la page de description du Windows Store.  
1.  Sous la vidéo, sélectionnez **partager**l'  >  **incorporation**.  
1.  Copiez le code HTML qui s’affiche.  
1.  Dans la page Détails de la description dans le Windows Store, collez le code HTML dans le `YouTube video URL` champ.  

##### Conditions générales de recherche  

Les termes de recherche doivent respecter les exigences suivantes.  

*   Vous pouvez entrer des termes de recherche pour utiliser un maximum de 21 mots.  Qu’il s’agisse d’un mot, d’une expression unique ou d’une combinaison des deux, vous n’avez autorisé qu’un maximum de 21 mots.  
*   Jusqu’à sept termes de recherche: un seul mot ou une seule expression.  Chaque critère de recherche a une limite de 30 caractères.  

#### Étape 6: terminer votre soumission  

Dans la page **Envoyez votre extension** , ajoutez des notes de certification pour vous aider à tester votre extension.  

##### Remarques pour la certification (facultatif)  

Lorsque vous soumettez votre extension, utilisez la page **Remarques pour la certification** pour fournir des informations supplémentaires aux testeurs de certification.  Les informations supplémentaires permettent de vérifier que votre extension est testée correctement.  Si votre extension n’est pas entièrement testée, il est possible qu’elle ne soit pas certifiée.  

Veillez à inclure les informations suivantes, le cas échéant.  

*   Noms d’utilisateurs et mots de passe pour les comptes de test.  
*   Étapes à suivre pour accéder aux fonctionnalités masquées ou verrouillées.  
*   Différences attendues en fonction de la région ou des paramètres d’un utilisateur.  
*   Si votre soumission est une mise à jour d’une extension existante, incluez les informations relatives aux modifications apportées à l’extension.  
*   Toute information supplémentaire que les testeurs doivent comprendre sur votre soumission.  

Après avoir fourni les informations, sélectionnez **publier** pour l’enregistrer dans le catalogue des modules complémentaires Microsoft Edge.  Votre soumission s’exécute dans l’étape de certification.  Le processus de certification risque de durer jusqu’à sept jours ouvrables après votre soumission.  

Lorsque votre soumission passe une certification, votre extension est publiée dans le catalogue des modules complémentaires Microsoft Edge.  Le statut de votre poste dans le tableau de bord du centre de partenaires devient `In the Store` .  

> [!NOTE]
> Si vous rencontrez des problèmes dans le processus de soumission ou d’inscription, envoyez un ticket de support [ici][ExtensionsSupportForm] ou envoyez un e-mail à [ext_dev_support@microsoft.com](mailto:ext_dev_support@microsoft.com).  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Premiers pas avec les extensions Microsoft Edge (chrome) | Documents Microsoft"  
[DeveloperRegistration]: ./create-dev-account.md "S’inscrire en tant que développeur Microsoft Edge extensions | Documents Microsoft"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Porter votre extension de chrome vers Microsoft Edge | Documents Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Stratégies développeurs de catalogue Microsoft Edge addons | Documents Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrat du développeur de l’application | Documents Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centre de partenariat"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensions nouvelle demande d’assistance | Support Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Définir vos formats publicitaires par défaut-aide YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Publicités sur les vidéos incorporées-aide sur YouTube"
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Incorporation de vidéos & de playlists-aide sur YouTube"  
