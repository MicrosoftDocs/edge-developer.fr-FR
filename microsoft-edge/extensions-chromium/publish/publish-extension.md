---
description: Processus étape par étape de la publication d’extensions de périphérique (chrome) sur le Microsoft Store.
title: Publier une extension
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607377"
---
# Publier une extension  

Publiez votre extension sur le catalogue Microsoft Edge addons \ (Microsoft Edge addons \).  Vous devez commencer par créer une soumission dans le [Centre de partenariat][MicrosoftPartnerCenter] et la soumettre.  Ce document recense tous les détails que vous devez fournir pour créer une soumission d’extension.  

## Avant de commencer  

*   Vous devez disposer d’un compte de développeur actif dans le [Centre des partenaires][MicrosoftPartnerCenter] pour pouvoir faire votre extension dans Microsoft Edge addons.  Si vous n’en avez pas, [créez un compte de développeur][MicrosoftPartnerCenter].  
*   Créez un fichier zip de votre package d’extension et assurez-vous qu’il contient les fichiers suivants:  
    *   Le fichier manifeste et il doit définir le nom et la version de votre extension.  
    *   Les images et autres fichiers requis pour votre extension.  


Si vous n’avez pas encore créé de poste, vous pouvez consulter le didacticiel de [mise en route][ExtensionsGettingStarted] pour la création d’une extension de chrome Microsoft Edge.  

Pour créer une soumission d’extension dans le [Centre de partenariat][MicrosoftPartnerCenter], procédez comme suit.  

## Étape 1: commencer une nouvelle soumission  

Accédez au [tableau de bord][MicrosoftPartnerCenter]de votre développeur.  Sur la page vue d’ensemble, cliquez sur **créer une nouvelle extension**.  

## Étape 2: Télécharger le fichier zip de votre extension  

La page **package** est l’endroit où vous chargez le fichier zip de votre soumission d’extension.  Il est possible que vous ne puissiez télécharger qu’un seul package à la fois, et si votre extension n’est pas terminée, il est possible que vous receviez un package en cours de travail et une mise à jour à tout moment avant de le publier.  Assurez-vous que votre package contient le `manifest.json` fichier et qu’il fonctionne correctement sur Microsoft Edge avant de le télécharger.  
Téléchargez le package en le faisant glisser dans le champ de chargement ou en sélectionnant **parcourir vos fichiers**.  La page package valide le fichier zip extensions et affiche l' **État de réussite ou d’échec de votre chargement**.  Si le package est validé; Il est chargé avec succès et un message de réussite s’affiche.  Si la validation du package échoue; le package n’est pas accepté et un message d’erreur s’affiche.  Si le package contient des erreurs, résolvez les problèmes et essayez de le télécharger à nouveau.  

Une fois le téléchargement terminé, passez en revue les détails de votre poste, puis cliquez sur **suivant** pour continuer.  

## Étape 3: fournir des informations de disponibilité  

### Définir la visibilité  

Sélectionnez une option de **visibilité** pour définir le public qui est susceptible de détecter et d’acquérir votre extension.  Cela vous permet de spécifier si les utilisateurs doivent trouver votre extension dans les compléments Microsoft Edge ou consulter le contenu de la liste.  Pour l’instant, vous avez le choix entre deux options sous Visibility:  

*   `Public`  
    Il s’agit de l’option par défaut.  
    Si vous sélectionnez `Public` , votre extension est disponible et détectable par tout le monde dans les modules complémentaires Microsoft Edge.  Laissez cette option sélectionnée si vous voulez que votre extension soit répertoriée dans les modules complémentaires Microsoft Edge pour les utilisateurs à rechercher via la recherche, la navigation et le lien direct de votre extension.  

*   `Hidden`  
    Si vous sélectionnez cette option `Hidden` , votre extension est masquée dans les modules complémentaires Microsoft Edge lors de la recherche ou de la navigation des utilisateurs; vous devez partager votre URL d’entrée pour distribuer votre extension.  Les utilisateurs disposant d’un lien direct vers l’entrée peuvent télécharger l’application sur Microsoft Edge \ (il est possible que vous trouviez votre URL de référencement dans la page de **Présentation** de l’extension \).  

> [!NOTE]
> Si vous envoyez une extension **publique** et que vous la définissez ultérieurement sur **privée**, les utilisateurs qui ont installé l’extension quand elle était publique continuent d’avoir accès et de recevoir des mises à jour ultérieures.  

### Définir des marchés  

Vous devez définir les marchés spécifiques dans lesquels vous proposez votre extension, puis sélectionnez **afficher les options** dans la section **marchés** de la page **disponibilité** .  La fenêtre contextuelle de sélection du marché s’affiche, qui vous permet de choisir les marchés.  Par défaut, tous les marchés sont sélectionnés, y compris tous les **marchés futurs** qui pourront être ajoutés plus tard.  Vous pouvez désélectionner des marchés spécifiques pour les exclure, ou cliquer sur **Désélectionner tout** , puis ajouter les marchés de votre choix.  

> [!NOTE]
> Si les utilisateurs ont déjà votre extension dans un certain marché et que vous supprimez ensuite ce marché, les utilisateurs disposant déjà de l’extension sur ce marché peuvent continuer à l’utiliser, mais ils ne reçoivent pas les mises à jour que vous avez apportées ultérieurement.  

Cliquez sur **Enregistrer** pour accéder à la section **Propriétés** .  

## Étape 4: sélectionner les propriétés pour votre extension  

### Propriétés d’extension  

*   [Catégorie](#category)  
*   [Politique de confidentialité](#privacy-policy-requirements)  
*   [URL de la politique de confidentialité](#privacy-policy-url)  
*   [URL du site Web](#website-url)  
*   [URL/adresse e-mail du support technique](#support-urlemail-address)  
*   [Niveau d’extension](#extension-rating)  

#### Catégorie  

La liste de vos extensions dans la catégorie appropriée permet aux utilisateurs de trouver facilement votre extension et d’en savoir plus à son sujet.  Sélectionnez une catégorie qui décrit le mieux votre extension.  

**Valeurs possibles**:  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### Politique de confidentialité  

Indiquez si votre extension accède à une extension, collecte ou transmet des informations personnelles.  

> [!NOTE]
> Si votre extension nécessite une politique de confidentialité et que vous ne l’avez pas fournie, votre soumission risque de ne pas obtenir de certification.  

**Valeurs possibles**:  

*   `No`: Une URL de politique de confidentialité est facultative.  
*   `Yes`: Une URL de politique de confidentialité est requise.  

#### URL de la politique de confidentialité  

Le cas échéant, vous êtes responsable de la conformité de votre extension aux lois et réglementations en matière de vie privée.  Vous devez fournir une URL de politique de confidentialité si des informations personnelles sont consultées, transmises ou collectées par votre extension.  
Pour savoir si votre extension nécessite une politique de confidentialité, consultez le [contrat du développeur Microsoft Edge][MicrosoftAppDeveloperAgreement] et le document des stratégies pour les [développeurs du catalogue Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valeurs possibles**:  

*   `{url}`  

#### URL du site Web  

Propriété facultative.  
URL de la page Web de votre extension.  Cette URL doit pointer vers une page de votre propre site Web, et non vers la liste des sites Web de votre extension dans les modules complémentaires Microsoft Edge.  

**Valeurs possibles**:  

*   `{url}`  

#### URL/adresse e-mail du support technique  

Propriété facultative.  
URL de la page Web dans laquelle les utilisateurs accèdent à la prise en charge de votre extension ou une adresse de messagerie pour vous contacter.  Vous incluez des informations de support pour toutes les soumissions, de sorte que vos utilisateurs sachent comment obtenir une assistance technique.  

**Valeurs possibles**:  

*   `{email_address}`  
*   `{url}`  

#### Niveau d’extension  

Le taux d’extension nous permet de déterminer l’âge du public cible de votre poste.  
Pour vous aider à déterminer si le contenu de vos extensions est mature, consultez le [document stratégies pour les développeurs du catalogue Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valeurs possibles**:  

*   Mature \ (case à cocher \): activez cette case à cocher si votre extension contient du contenu mûr.  Si vous avez sélectionné l’option mature pour votre extension, votre entrée est disponible avec une balise séparée pour indiquer que l’extension contient du contenu mûr.  

Cliquez sur **Enregistrer** pour accéder à la section liste.  

## Étape 5: ajouter des informations de référencement pour votre extension  

Voici les informations que voient les utilisateurs lors de l’affichage de votre entrée dans les compléments Microsoft Edge.  La plupart des champs d’une liste sont facultatifs, mais nous vous suggérons de fournir autant d’informations que possible pour faire ressortir votre annonce.  Le minimum requis pour que votre liste des modules complémentaires Microsoft Edge soit considéré comme complet est la [Description du texte](#description), le logo de l' [extension](#store-logo)et la [vignette promotionnelle de petite taille](#small-promotional-tile) dans chaque langage mentionné dans votre package d’extension.  

### Champs d’annonce dans le Windows Store  

*   [Langues des descriptions dans le Store](#store-listing-languages)  
*   [Nom complet du Windows Store](#store-display-name)  
*   [Description](#description)  
*   [Logo du Windows Store](#store-logo)  
*   [Petite vignette promotionnelle](#small-promotional-tile)  
*   [Support](#media)  
*   [Description courte](#short-description)  
*   [Termes de recherche](#search-terms)  

#### Langues des descriptions dans le Store  

Si votre package d’extension prend en charge plusieurs langues, votre extension doit être associée à une page de listing pour chacun d’eux.  
Vous devez compléter les détails de la liste \ (description du texte, images, etc.) pour chaque langue séparément, même si vous utilisez le même contenu pour chaque langue.  Si votre extension est localisée dans plusieurs langues, celles-ci s’affichent en haut de la page de description.  

1.  Sélectionnez un nom de langue dans la liste déroulante **langues** .  
1.  Remplissez les détails de la liste.  
1.  Cliquez sur **Save**.  
1.  Répétez l’opération pour toutes les langues prises en charge.  

> [!NOTE]
> Pour ajouter ou supprimer des langues pour votre liste dans les modules complémentaires Microsoft Edge, vous devez modifier la liste des langues prises en charge par votre package d’extension et le télécharger à nouveau.  

**Valeurs possibles**:  

*   `English (United States)`: Il s’agit de la valeur par défaut.  Si vous n’indiquez aucune langue dans votre package, nous définissons votre langue par défaut sur français (France), et vous devez fournir une entrée en anglais (États-Unis).  
*   `{language}` \(`{Country}`\)  

#### Nom complet du Windows Store  

Nom de l’extension, tel que mentionné dans le manifeste de votre package d’extension.  

> [!NOTE]
> Pour modifier le nom, vous devez mettre à jour le manifeste dans votre package d’extension et le télécharger à nouveau.  

#### Description  

Ce champ est obligatoire.  
Description de la fonction de votre extension par vos utilisateurs.  

**Valeurs possibles**:  

*   {plain_text}: moins de 10 000 caractères.  

#### Logo du Windows Store  

Ce champ est obligatoire.  
Image 1:1 du logo de votre poste.  

**Valeurs possibles**:  

*   128px x 128px, PNG \ (. png \)  
*   150px x 140px, PNG \ (. png \)  
*   300px x 300px, PNG \ (. png \): taille recommandée.  

#### Petite vignette promotionnelle  

Ce champ est obligatoire.  
Vignette promotionnelle de petite taille.  Votre entrée est affichée sur cette vignette.  

**Valeurs possibles**:  

*   440px x 280x, PNG \ (. png \)  

#### Support  

Il est obligatoire.  
Nous vous conseillons de fournir ces ressources pour vous aider à optimiser l’affichage de votre produit.  

*   Captures d’écran  
    Les images de votre extension qui décrivent ce que fait votre extension.  
    
*   Tuiles de grande promotion  
    Une vignette promotionnelle de grande taille pour pouvoir présenter plus clairement votre extension dans les compléments Microsoft Edge.  
    
*   URL de la vidéo YouTube  
    [URL vidéo YouTube valide pour votre extension][MicrosoftEdgeAddonsUploadYouTubeVideo].  Votre vidéo devrait être de bonne qualité et de longueur minimale.  Votre vidéo YouTube doit réussir la certification avant de publier votre extension dans les compléments Microsoft Edge.  Vérifiez que votre vidéo YouTube est compatible avec le [document des stratégies du développeur Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valeurs possibles**:  

*   10 captures d’écran maximum.  
    *   640 pixels x 480px, PNG \ (. png \): captures d’écran.  
    *   1280px x 800px, PNG \ (. png \): captures d’écran.  
*   1400px x 560px, PNG \ (. png \): grande vignette de promotion.  
*   URL de la vidéo YouTube de 60 secondes ou courtes de 2 Go ou moins.  

#### Description courte  

Brève description qui est susceptible d’être utilisée en haut de la liste pour votre produit.  Si ce n’est pas le cas, les premières lignes de votre description plus longue seront utilisées à la place.  Dans la mesure où votre description apparaît également sous ce texte, vous devez fournir une courte description contenant un texte différent de sorte que votre liste soit moins répétitive.  La brève description de votre extension est choisie directement dans le fichier manifeste de votre package.  

> [!NOTE]
> Pour modifier la brève description, vous devez mettre à jour le manifeste dans votre package d’extension et le télécharger à nouveau.  

#### Termes de recherche  

Les termes de recherche sont des mots uniques ou des phrases courtes qui ne sont pas visibles pour les utilisateurs, mais aident à rendre votre extension détectable par les modules complémentaires Microsoft Edge lorsque les utilisateurs effectuent des recherches en utilisant ces termes.  

**Configuration requise**:  

*   7 ou moins termes de recherche  
*   30 caractères au maximum par critère de recherche  
*   21 ou moins de mots pour les termes de recherche combinés  

Cliquez sur **Enregistrer** pour continuer pour enregistrer la section de votre annonce.  Cliquez sur **publier** pour fournir des informations de soumission.  

## Étape 6: terminer votre soumission et cliquer sur publier  

La page d’options de soumission du processus de soumission d’extension vous permet de fournir des informations supplémentaires pour nous aider à tester correctement votre produit.  Il s’agit d’une étape facultative, mais elle est recommandée pour de nombreux envois.  

### Options de mise en attente de publication  

Par défaut, votre soumission est publiée dès qu’elle passe une certification.  Vous pouvez décider de mettre en attente la publication de votre soumission jusqu’à une date spécifique.  Les options disponibles dans cette section sont décrites ci-dessous.  

*   **Publier votre soumission dès qu’elle passe la certification**  

    Il s’agit de la sélection par défaut.  Cela signifie que votre soumission commence le processus de publication dès qu’il passe une certification.  

*   **Démarrer la publication de votre soumission à une date donnée**  

    Pour vous assurer que la soumission ne sera pas publiée avant une date spécifique, sélectionnez **commencer la publication de votre soumission à une date donnée** .  Avec cette option, votre soumission est publiée aussitôt que possible à la date spécifiée ou après.  La date doit être postérieure de 24 heures au moins.  Parallèlement à la date, vous pouvez spécifier l’heure à laquelle la publication de la soumission doit commencer.  

### Remarques pour la certification  

Lorsque vous envoyez votre extension, vous avez la possibilité d’utiliser la page remarques pour la certification pour fournir des informations supplémentaires aux testeurs de certification.  Ces informations permettent de vérifier que votre extension est testée correctement.  Si nous ne sommes pas en mesure d’effectuer un test total de votre soumission, la certification peut échouer.  

Veillez à inclure les éléments suivants (le cas échéant):  

*   Noms d’utilisateurs et mots de passe pour les comptes de test.  
*   Étapes à suivre pour accéder aux fonctionnalités masquées ou verrouillées.  
*   Différences attendues du comportement en fonction de la région ou d’autres paramètres utilisateur.  
*   Informations sur les modifications apportées à la mise à jour d’une application.  
*   Tout d’abord, vous pensez que les testeurs doivent comprendre votre soumission.  

Après avoir rempli les informations ci-dessus, cliquez sur **publier** pour valider votre extension dans les compléments Microsoft Edge.  

Lorsque vous avez terminé de créer la soumission pour votre extension et cliqué sur **publier**, la soumission entre dans l’étape de certification.  Ce processus s’effectue généralement dans un délai de deux jours, mais dans certains cas cela peut prendre jusqu’à 7 jours ouvrables.  Une fois votre soumission certifiée, votre extension est publiée dans les modules complémentaires Microsoft Edge, sauf si vous avez sélectionné les options de conservation de publication pour spécifier qu’elle ne doit pas être publiée avant une date donnée.  Vous êtes averti lorsque votre soumission est publiée et que le statut de votre extension dans le tableau de bord devient `In the Store` .  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Mise en route des extensions Microsoft Edge \ (chrome \) | Documents Microsoft"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Télécharger une vidéo YouTube | Documents Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Stratégies développeurs de catalogue Microsoft Edge addons | Documents Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrat du développeur de l’application | Documents Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centre de partenariat"  
