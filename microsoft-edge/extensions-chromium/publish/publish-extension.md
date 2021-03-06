---
description: Publier des extensions Microsoft Edge (Chromium) dans le magasin de modules extensions Microsoft Edge
title: Publier votre extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 67fdbdb39f3ef0b2b6cef2831520849933ffeeec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399126"
---
# <a name="publish-your-extension"></a>Publier votre extension  

Après avoir développé et testé votre extension, vous êtes prêt à distribuer votre extension. Utilisez le microsoft Edge Add-ons Store pour distribuer votre extension.  Pour libérer votre extension Chromium existante pour les utilisateurs de Microsoft Edge, accédez au portage de votre [extension Chromium existante.][PortChromiumExtension]  

Publiez votre extension dans le magasin de modules extensions Microsoft Edge pour en augmenter la portée et la rendre accessible aux utilisateurs de Microsoft Edge.  Cet article fournit le processus de soumission de votre extension au magasin de modules extensions Microsoft Edge.  

## <a name="before-you-begin"></a>Avant de commencer  

Vous devez avoir un prototype de travail de votre extension prêt.  Pour plus d’informations sur la création d’une extension, reportez-vous au [didacticiel de mise en place.][ExtensionsGettingStarted]  

Pour publier votre extension dans le magasin de modules de développement Microsoft Edge, utilisez votre compte de développeur actif dans [l’Partner Center][MicrosoftPartnerCenter].  Si vous n’avez pas de compte de développeur, créez-en un.  Pour ouvrir un nouveau compte de développeur et vous inscrire au programme de modules de développement Microsoft Edge, accédez à [l’inscription du développeur.][DeveloperRegistration]  

Créez un fichier zip qui représente votre package d’extension.  Votre package d’extension doit inclure les fichiers suivants.  

*   Manifeste d’extension spécifiant des détails tels que le nom de l’extension, la description courte, les autorisations et la langue par défaut.  
*   Images et autres fichiers requis par votre extension.  

Les champs suivants du manifeste sont automatiquement inclus dans les détails de votre description dans le Store.  Les champs sont en lecture seule sur la page **de listes du Store.**  La page des descriptions dans le Store est décrite plus loin dans cet article.  Assurez-vous que les valeurs de champ correspondent à votre affichage préféré sur la page des détails du Store avant de télécharger votre package dans l’Partner Center.  Pour obtenir un exemple du code requis pour le fichier manifeste, examinez les principes de base du fichier manifeste.  

*   `Name` dans le fichier manifeste, qui est le nom **complet** sur la page de détails de la boutique.  
*   `Description` dans le fichier manifeste, qui est la **description** courte sur la page de détails de la boutique.  Fournissez une description courte et brève à afficher en haut de la liste pour votre extension.  Lorsqu’elle est incluse, la description courte spécifiée dans le fichier manifeste d’extension s’affiche dans votre description dans le Store.  Si aucune description courte n’est incluse dans le fichier manifeste, les premières lignes de Description s’affichent.  Fournissez une brève description pour éviter la répétition du contenu sur votre page de description dans le Store.  

## <a name="submit-your-extension-to-microsoft-edge-add-ons-store"></a>Envoyer votre extension au magasin de modules extensions Microsoft Edge  

Pour envoyer votre extension à [l’Partner Center,][MicrosoftPartnerCenter]utilisez les étapes suivantes.  

#### <a name="step-1--start-a-new-submission"></a>Étape 1 : Démarrer une nouvelle soumission  

Accédez au tableau [de bord du développeur][MicrosoftPartnerCenter] et choisissez Créer une **extension** dans la page **Vue d’ensemble.**  

#### <a name="step-2--upload-the-extension-package"></a>Étape 2 : Télécharger le package d’extension  

Utilisez la page **Packages** pour télécharger le fichier zip de votre package d’extension.  Vous ne pouvez télécharger qu’un seul package à la fois.  Vous ne pouvez pas poursuivre la soumission si le chargement du package n’a pas réussi sur la page **Packages.**  

Pour télécharger le package, choisissez et faites glisser le package vers le champ de chargement. Vous pouvez également choisir **Parcourir vos fichiers.**  Une fois le package téléchargé, votre package est validé.  Une fois la validation validée, examinez les détails de l’extension, puis choisissez **Suivant** pour continuer.  S’il existe des erreurs de validation, résolvez les problèmes et essayez à nouveau de télécharger.  

#### <a name="step-3--provide-availability-details"></a>Étape 3 : Fournir des détails sur la disponibilité  

Dans la page **Disponibilité,** entrez les informations suivantes sur la disponibilité de votre extension.  

##### <a name="visibility"></a>Visibilité  

Choisissez l’une des options de visibilité suivantes pour définir si votre extension est découvrable dans le magasin de modules supplémentaires Microsoft Edge.  

*   `Public` \(default\)  
    Public permet à tout le monde de découvrir votre extension par le biais de la recherche, de la navigation dans le magasin de modules extensions Microsoft Edge ou à l’aide de l’URL de référencement de votre extension dans le magasin de modules de microsoft Edge.  L’URL de description est disponible dans le tableau de bord de l’Partner Center dans la page Vue d’ensemble de **l’extension.**  
    
*   `Hidden`  
    Hidden supprime les extensions des résultats de la recherche ou de la navigation dans le magasin des extensions Microsoft Edge.  Pour distribuer des extensions masquées dans le magasin des extensions Microsoft Edge, vous devez partager l’URL de référencement vers l’extension avec vos clients.  
    
> [!NOTE]
> Vous pouvez modifier la visibilité de votre extension de **Public** à **Masqué.**  Les utilisateurs qui ont installé votre extension alors que la visibilité était définie sur public conservent l’accès à votre extension et reçoivent les mises à jour que vous rendez disponibles via le site web des extensions Microsoft Edge.  

##### <a name="markets"></a>Marchés  

Définissez les marchés spécifiques dans lesquels vous envisagez d’offrir votre extension.  Le paramètre par défaut pour les marchés est tous les marchés et inclut les marchés futurs qui seront ajoutés ultérieurement.  Pour choisir des marchés spécifiques, choisissez **Modifier les marchés.**  Basculez les marchés individuels pour exclure chacun d’eux, ou choisissez **Désélectionner** tout, puis ajoutez les marchés de votre choix.  

> [!NOTE]
> Vous pouvez modifier les marchés où votre extension est proposée.  Un utilisateur qui installe votre extension alors qu’elle est disponible sur le marché de l’utilisateur conserve l’accès à votre extension.  Toutefois, l’utilisateur n’a pas accès aux futures mises à jour envoyées au magasin de modules de développement Microsoft Edge.  

Sélectionnez **Enregistrer** pour continuer à la section **Propriétés.**  

#### <a name="step-4-select-properties-for-your-extension"></a>Étape 4 : Sélectionner les propriétés de votre extension  

Dans la **page Propriétés,** entrez les informations suivantes pour spécifier les propriétés de votre extension.  Les propriétés sont affichées pour les utilisateurs dans le magasin de modules de microsoft Edge.  

| Nom de la propriété d’extension | Description |  
|:--- |:--- |  
| Catégorie \(obligatoire\) | Catégorie qui décrit le mieux votre extension.  Le fait de répertorier votre extension dans la catégorie de droite permet aux utilisateurs de trouver facilement votre extension et d’en comprendre davantage.  |  
| Exigences en matière de politique de confidentialité \(obligatoire\) | Indiquez si votre extension accède, collecte ou transmet des informations personnelles.  Votre extension peut échouer à l’étape de certification si vous choisissez **Oui** et que vous ne fournissez pas de `Privacy policy URL` .  |  
| URL de la politique de confidentialité | URL valide de la politique de confidentialité pour communiquer comment votre extension suit les lois et réglementations en matière de confidentialité.  Vous devez vous assurer que votre extension suit les lois et réglementations en matière de confidentialité.  Vous êtes également responsable de la fourniture d’une URL de stratégie de confidentialité si des informations personnelles sont accessibles, transmises ou collectées par votre extension.  Pour déterminer si votre extension nécessite une politique de confidentialité, accédez au contrat du développeur [Microsoft Edge][MicrosoftAppDeveloperAgreement] et aux stratégies de développement des modules de développement des modules de développement microsoft [Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  
| URL du site web | Page web qui fournit des informations supplémentaires sur votre extension.  Vous devez pointer vers une page de votre propre site web, et non vers la liste web de votre extension dans le magasin de modules de développement `Website URL` Microsoft Edge.  Il `Website URL` permet aux utilisateurs d’en savoir plus sur votre extension, ses fonctionnalités et toute autre information pertinente.  |  
| Coordonnées du support technique | URL de votre page web de support ou adresse de messagerie pour contacter votre équipe de support technique.  |  
| Contenu mature | Cochez la case pour spécifier si votre extension inclut du contenu mature.  L’évaluation de l’extension permet de déterminer le groupe d’âge approprié de l’audience cible de votre extension.  Pour déterminer si votre extension possède du contenu mature, accédez aux stratégies de développement du magasin de [modules de][MicrosoftEdgeAddonsCatalogDeveloperPolicies]microsoft Edge.  |  

Choose **Save** to continue to the **Store listings** section.  

> [!Important]
> Le nom de votre développeur/organisation, l’URL du site web et les coordonnées du support que vous avez envoyées lors de l’inscription sont affichés pour les utilisateurs dans le magasin de modules de développement Microsoft Edge.  

#### <a name="step-5-add-store-listing-details-for-your-extension"></a>Étape 5 : Ajouter des détails de description dans le Store pour votre extension  

Les informations fournies dans la section suivante s’affichent pour les utilisateurs qui examinent votre liste dans le magasin de modules complémentaires Microsoft Edge.  Même si certains champs sont facultatifs, vous devez fournir autant d’informations que possible.  Pour obtenir la liste de votre extension dans le store, les informations suivantes sont requises.  

*   **Description** de chaque langue de votre package d’extension.  
*   **Logo du magasin d’extensions** pour chaque langue de votre package d’extension.  
    
> [!NOTE]
> Les détails minimaux requis de la description dans le Store doivent être remplis pour au moins l’une des langues mentionnées dans votre package zip d’extension.  Pour ajouter ou supprimer des langues dans la liste de votre **** magasin dans le magasin des modules de microsoft Edge, utilisez la liste ajouter une langue dans la page Des **listes dans le Store.**  En outre, vous pouvez choisir de dupliquer vos ressources d’une langue à une autre à l’aide du bouton de fonctionnalité en double sur la page des détails de la langue.  

| Nom de la propriété Détails de la langue | Description |  
|:--- |:--- |  
| Nom complet \(obligatoire\) | `name`L’extension spécifiée dans le fichier manifeste de votre extension.  Pour modifier le nom complet de la boutique après l’envoi, vous pouvez mettre à jour le nom dans le fichier manifeste, créer un package d’extension, puis le recharger.  |  
| Description \(obligatoire\) | Le champ se concentre sur l’explication de ce que fait votre extension, pourquoi les utilisateurs doivent l’installer ou d’autres informations pertinentes que les `description` utilisateurs doivent connaître.  Elle doit être inférieure à 10 000 caractères.  |  
| Logo du magasin d’extensions \(requis\) | Image qui représente votre entreprise ou avec un rapport d’aspect de 1 et une taille recommandée de `extension logo` 300 x 300 pixels.  En outre, vous pouvez choisir de copier la bien d’une langue vers toutes les autres langues à l’aide du bouton dupliqué.  Le bouton se trouve à la suite du champ après avoir téléchargé votre logo pour la langue.  |  
| Petite vignette promotionnelle \(facultatif\) | L’image est utilisée pour afficher votre extension avec `Small promotional tile` d’autres extensions dans le store.  La taille de l’image doit être de 440 x 280 pixels.  En outre, vous pouvez choisir de copier la bien d’une langue vers toutes les autres langues à l’aide du bouton dupliqué.  Le bouton se trouve à la suite du champ après le téléchargement d’une vignette promotionnelle pour la langue.  |  
| Captures d’écran \(facultatif\) | Vous pouvez envoyer un maximum de 10 descriptions détaillées des `screenshots` fonctionnalités de votre extension.  La taille des captures d’écran doit être de 640 x 480 pixels ou de 1280 x 800 pixels.  En outre, vous pouvez choisir de copier la bien d’une langue vers toutes les autres langues à l’aide du bouton dupliqué.  Le bouton se trouve à la suite du champ après avoir téléchargé au moins une langue.|  
| Grande vignette promotionnelle \(facultatif\) | `Large promotion tiles` sont utilisés dans le Store pour mettre en évidence les extensions de fonctionnalités sur le site web des extensions Microsoft Edge.  Les images, si elles sont envoyées, sont visibles pour les utilisateurs.  La taille des fichiers PNG doit être de 1 400 x 560 pixels.  En outre, vous pouvez choisir de copier la bien d’une langue vers toutes les autres langues à l’aide du bouton dupliqué.  Le bouton se trouve à la suite du champ après le téléchargement d’une vignette promotionnelle pour la langue.  |  
| URL de vidéo YouTube \(facultatif\) | Vous pouvez inclure une vidéo YouTube promotionnelle de votre extension.  La `YouTube video URL` vidéo s’affiche sur la page de liste du Store de votre extension.  |  
| Description courte \(obligatoire\) | Pour modifier le package d’extension, vous devez mettre à jour le champ de description dans votre fichier manifeste de votre package d’extension et `short description` le recharger.  |  
| Termes de recherche \(facultatif\) | `Search terms` sont des mots ou des expressions qui aident les utilisateurs à découvrir votre extension lors d’une recherche dans le magasin de modules extensions Microsoft Edge.  Les termes de recherche ne sont pas affichés pour les utilisateurs.  |  

##### <a name="youtube-video-url-requirements"></a>Exigences relatives à l’URL de la vidéo YouTube  

Assurez-vous que votre vidéo répond aux exigences suivantes.  

*   Vérifiez que le contenu de la vidéo YouTube suit les stratégies de développement du magasin de [modules de développement Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Désactiver les publicités sur votre vidéo.  Pour plus d’informations, [accédez à Définir][GoogleYoutubeAnswer2531367Topic7072227] vos formats de publicité par défaut et les publicités sur les vidéos [incorporées.][GoogleYoutubeAnswer132596]  
*   Activer l’incorporation de vos vidéos.  Pour plus d’informations, [accédez à Incorporer des vidéos & playlists.][GoogleYoutubeAnswer171780]  
    
Pour soumettre l’URL de la vidéo YouTube de votre vidéo, complétez les étapes suivantes.  

1.  Sur YouTube, localisez la vidéo que vous souhaitez ajouter à votre page de référencement dans le Store.  
1.  Under the video, choose **Share**  >  **Embed**.  
1.  Copiez le code HTML qui s’affiche.  
1.  Dans la page des détails de la description dans le Store, collez le code HTML dans le `YouTube video URL` champ.  
    
##### <a name="search-terms-requirements"></a>Conditions requises pour les termes de recherche  

Les termes de recherche doivent respecter les conditions suivantes.  

*   Vous pouvez entrer des termes de recherche pour utiliser jusqu’à 21 mots au maximum.  Que vous utilisiez des mots simples, des expressions ou une combinaison des deux, vous n’êtes autorisé qu’à un maximum de 21 mots.  
*   Jusqu’à sept termes de recherche maximum : un seul mot ou une seule expression.  Chaque terme de recherche est limité à 30 caractères.  
    
#### <a name="step-6-complete-your-submission"></a>Étape 6 : Terminer votre soumission  

Dans la page **Envoyer votre extension,** ajoutez des notes de certification pour vous aider à tester votre extension.  

##### <a name="notes-for-certification-optional"></a>Remarques pour la certification (facultatif)  

Lorsque vous soumettez votre extension, utilisez la page **Remarques** pour la certification pour fournir des informations supplémentaires aux testeurs de certification.  Les informations supplémentaires permettent de s’assurer que votre extension est testée correctement.  Si votre extension n’est pas entièrement testée, elle risque d’échouer à la certification.  

Veillez à inclure les informations suivantes, si nécessaire.  

*   Noms d’utilisateur et mots de passe pour les comptes de test.  
*   Étapes pour accéder aux fonctionnalités masquées ou verrouillées.  
*   Différences attendues de fonctionnalités basées sur la région ou d’autres paramètres utilisateur.  
*   Si votre envoi est une mise à jour d’une extension existante, incluez des informations sur les modifications apportées à l’extension.  
*   Toute information supplémentaire que les testeurs doivent comprendre sur votre soumission.  

Après avoir fourni les informations, choisissez **Publier** pour envoyer votre extension au magasin de modules complémentaires Microsoft Edge.  Votre envoi est soumis à l’étape de certification.  Le processus de certification peut prendre jusqu’à sept jours ou jours après votre envoi.  

Lorsque votre soumission a été certification, votre extension est publiée dans le magasin de modules extensions Microsoft Edge.  L’état de votre extension dans le tableau de bord de l’Centre de partenaires change en `In the Store` .  

> [!NOTE]
> Si vous rencontrez des problèmes dans le processus de soumission ou d’inscription, déposez un ticket de support sur la nouvelle demande de support [extensions][ExtensionsSupportForm] ou envoyez un e-mail [à ext_dev_support@microsoft.com][MailtoExtDevSupportMicrosoftCom].  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Mise en place des extensions Microsoft Edge (Chromium) | Documents Microsoft"  
[DeveloperRegistration]: ./create-dev-account.md "S’inscrire en tant que développeur d’extensions Microsoft Edge | Documents Microsoft"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Portez votre extension Chromium vers Microsoft Edge | Documents Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Les modules de développement Microsoft Edge stockent les stratégies de | Documents Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrat du développeur d’applications | Documents Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensions New Support Request | Microsoft Support"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Définir les formats de votre | Aide de YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Publicités sur des vidéos incorporées | Aide de YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Incorporer des vidéos & playlists | Aide de YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Envoyer un courrier électronique à ext_dev_support@microsoft.com" 
