---
description: Accédez au monde des clients Windows 10 en distribuant votre PWA via le Microsoft Store
title: Applications Web progressives dans la boutique Microsoft
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, Microsoft Store, index de Bing PWA
ms.openlocfilehash: a4491f19b89e8b0f6fa511f146744499e2074f22
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566627"
---
# Applications Web progressives dans la boutique Microsoft

Lorsque vous publiez votre application Web progressive sur le [Microsoft Store](https://developer.microsoft.com/store), le public de votre application potentiel s’étend sur la base de l’ensemble de l’installation de Windows 10, qui est proche de 700 millions utilisateurs du mois actif. 

PWAs dans le Microsoft Store bénéficiez de nombreux avantages:

- **Détectabilité** : les applications du Microsoft Store sont présentées dans différentes catégories, collections et filtres de recherche, offrant ainsi une simplicité de navigation et d’achat pour les clients potentiels de votre application. Vous pouvez même [améliorer votre](/windows/uwp/publish/app-screenshots-and-images) Description dans le Windows Store à l’aide d’une capture d’écran, d’une image de héros et de bandes vidéo.

- **Fiabilité** -les clients Windows savent qu’ils peuvent faire confiance à leurs achats et téléchargements de Microsoft Store, car ils respectent les [normes de qualité et de sécurité](/legal/windows/agreements/store-policies)rigoureuses de Microsoft.

- **Installation facile** -le Microsoft Store fournit une interface utilisateur cohérente et conviviale pour [toutes les applications Windows 10](https://www.microsoft.com/store/apps/windows?icid=CNavAppsWindowsApps), ce qui permet à tous les clients d’installer votre application PWA, quel que soit le niveau de confort technique.

- **Business Insights** -tableau de bord du centre de développement Windows pour le Microsoft Store fournit des informations [détaillées](/windows/uwp/publish/analytics) sur l’utilisation du [tableau de bord du centre de développement Windows](/windows/uwp/publish/using-the-windows-dev-center-dashboard) , ainsi que son utilisation. Vous pouvez également rechercher des données de mesure et de télémétrie sur l’état de l’application, l’utilisation des publicités, etc.

Deux options s’offrent à vous pour obtenir votre PWA dans le Microsoft Store:

1. Vous pouvez [le faire manuellement](#submitting-your-pwa-manually)ou

2. Si votre PWA répond à [certains critères](#criteria-for-automatic-submission), il peut être [automatiquement indexé](#automatic-pwa-importing-with-bing) par l’analyseur Web Bing. (Vous avez également la possibilité de [refuser](#opting-out-of-automatic-microsoft-store-import) la soumission automatique.)

Quelle que soit la méthode de soumission, une fois que votre PWA est accepté pour le Microsoft Store, vous pouvez accéder à tous les avantages décrits ci-dessus.

## Soumission manuelle de votre PWA

Pour distribuer et promouvoir une application via le Microsoft Store, vous devez la valider en tant que package d’application Windows (fichier *. AppX* ).  Pour les applications Web hébergées sur serveur, telles que PWAs, ce package contient simplement les métadonnées de l’application et les icônes de l’écran de démarrage (et aucune du code de l’application). Dans ce cadre, vous pouvez installer et lancer votre application Web à partir de l’écran d’accueil parallèlement à d’autres [applications Windows 10](/windows/uwp/get-started/whats-a-uwp) en les exécutant dans un wrapper d’application (*WWAHost. exe* ) léger, indépendamment de la fenêtre du navigateur Microsoft Edge.  

> [!IMPORTANT]
> Le moteur de plateforme Web EdgeHTML est utilisé par le wrapper de l’application WWAHost, qui peut introduire des différences de compatibilité pour votre compte Microsoft Edge (chrome).  Veillez à effectuer une passe de test complète sur votre application à l’aide de Microsoft Edge (EdgeHTML) avant de soumettre votre application au Microsoft Store, car le moteur EdgeHTML n’est plus mis à jour avec les nouvelles normes Web.  

Voici comment procéder.

### Conditions préalables

- **Un PWA existant**. Voici comment [convertir votre application Web vers une page de Project Web App](./get-started.md) , le cas échéant. 
- **Outil de création de packages Windows AppX pour PWAS**. Voici comment [générer et exécuter votre document PWA sur Windows](./windows-features.md) à l’aide de Visual Studio. Vous pouvez également utiliser le [Générateur PWA](https://www.pwabuilder.com/) pour créer un package Windows.
- [**Compte de développeur de l’application Microsoft Store**](/windows/uwp/publish/opening-a-developer-account). Il existe des [frais](/windows/uwp/publish/account-types-locations-and-fees) uniques en fonction du type de compte et de l’emplacement que vous avez choisis, et l’inscription nécessite un [compte Microsoft](https://account.microsoft.com/)valide.


### Soumission du Windows Store via *Visual Studio* 

Suivez ces étapes pour [créer un fichier de chargement de package d’application](/windows/uwp/packaging/packaging-uwp-apps#create-an-app-package-upload-file) pour votre application Project Web App dans Visual Studio. Pour plus d’informations générales sur ce processus, consultez [*la rubrique empaqueter une application UWP avec Visual Studio*](/windows/uwp/packaging/packaging-uwp-apps) .

Ces instructions vous guideront également dans le cadre de l’utilisation du [**Kit de certification des applications Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit) pour tester la conformité de votre application aux exigences du Microsoft Store. Facultatif, mais fortement recommandé.

### Soumission du Windows Store via le *Centre de développement Windows*

Voici comment utiliser le *Générateur PWA* pour générer un package d’application à télécharger dans le centre de développement Windows.

1. Générez votre application Windows 10. Voici comment exécuter votre document [PWA en tant qu’application Windows avec Visual Studio](./windows-features.md). Vous pouvez également utiliser le [Générateur PWA](https://www.pwabuilder.com/) pour générer votre application Windows 10.

2. Réservez le nom de votre application pour le Microsoft Store en vous connectant au [tableau de bord du centre de développement Windows](https://developer.microsoft.com/dashboard/windows/overview) avec les informations de votre compte et en suivant les étapes de [création de votre application en réservant un nom](/windows/uwp/publish/create-your-app-by-reserving-a-name). Chaque nom réservé doit être unique à travers le MicrosoftStore.

3. Quand vous chargez les packages de votre application, les valeurs *DisplayName*, *Name*, *Publisher*et *PublisherDisplayName* dans votre fichier *. appxmanifest* doivent correspondre aux valeurs affectées à votre application dans le tableau de bord du centre de développement Windows, au moment de réserver le nom. 

    Connectez-vous au [tableau de bord du centre de développement Windows](https://developer.microsoft.com/dashboard/windows/overview)et recherchez les valeurs d’identité de votre application sous identité de l’application gestion des **applications**  >  **App identity**:

    ![Tableau de bord du centre de développement Windows, paramètres d’identité des applications](./media/dashboard-app-identity.png)

    Recherchez ensuite votre `appxmanifest.xml` fichier et remplacez les valeurs suivantes par celles affectées dans le tableau de bord du centre de développement Windows:

    - **<nom d’identité = «** *package/identité/nom* »
    - **<éditeur d’identité = «** *package/identité/Publisher* »
    - **<DisplayName** **>** *Nom que vous avez réservé pour votre application* 
    - **<PublisherDisplayName** **>** *Package/propriétés/PublisherDisplayName***</PublisherDisplayName>**

4. Vous êtes maintenant prêt à compiler toutes les ressources de Project Web App dans un seul `.appx` fichier que vous pouvez télécharger sur le Microsoft Store. À partir d’une invite de commandes, accédez au répertoire de votre manifeste Web et créez un package Windows 10 (spécifié en dessous de w/journal de débogage facultatif):

    ```
    pwabuilder package -p windows10 -l debug
    ```

    Votre fichier. AppX sera généré à cet `PWA\Store packages\windows10\package\windows.appx` emplacement:

5. Avant de télécharger votre application pour submisison sur le Microsoft Store, il est recommandé de tester votre application conformément aux politiques du Windows Store. Pour cela, téléchargez le kit de [**certification des applications Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit), lancez-le, puis sélectionnez le fichier *. AppX* de votre application à des fins de test. Vous recevrez un rapport des zones à adresse une fois tous les tests terminés.

6. Chargez votre package et terminez la soumission en vous connectant à nouveau dans le [tableau de bord du centre de développement Windows](https://developer.microsoft.com/dashboard/windows/overview) et en développant le panneau des **soumissions**  >  **submisison 1** . Suivez la liste de vérification pour remplir les informations de description du Windows [Store requises](/windows/uwp/publish/app-submissions) et [Télécharger votre package d’application](/windows/uwp/publish/upload-app-packages).

Pour plus d’informations sur l’ensemble des fonctionnalités et services disponibles pour les développeurs d’applications du Microsoft Store, voir [*publier des applications Windows*](https://developer.microsoft.com/store/publish-apps) dans le [Centre de développement Windows](https://developer.microsoft.com/windows).

## Importation automatique de Project Web App avec Bing

Comme le manifeste de votre [application Web](https://developer.mozilla.org/docs/Web/Manifest) PWA est un signal de prise en charge de plateformes que votre application est en mode hors connexion et prête à être présentée comme une interface d’application entièrement intégrée, il s’agit également d’une astuce du robot Web de Bing, qui doit être envisagé pour une inclusion automatique du Microsoft Store. 

Si votre compte onedrive répond à la configuration requise ci-dessous, le service d’indexation de Bing empaquetera automatiquement votre PWA au format [*. AppX*](#submitting-your-pwa-manually) requis pour l’installation sur Windows 10 et assembler la page de produit Windows Store de votre application en fonction des métadonnées de son manifeste de l’application Web. Après avoir réclamé votre PWA, vous serez en mesure de personnaliser davantage votre page du Windows Store et d’accéder à des outils d’analyse des utilisateurs et d’autres outils de gestion des applications par le biais du tableau de bord du centre de développement Windows.

### Critères de soumission automatique

Pour être automatiquement conditionné et répertorié pour le Microsoft Store, vous devez disposer des éléments suivants:

- [X] fichier manifeste de l’application Web non vide, avec au minimum:

  - Nom
  - Description
  - Icône d’application d’au moins 512 x 512 pixels

- [X] logique principale unique (pas de code à modification minimum d’un modèle [réutilisable](https://en.wikipedia.org/wiki/Boilerplate_code) par une application)

- [X] pour être fourni sur une connexion sécurisée (HTTPs)

- [X] script du ou des threads de service

- [X] ne violer aucune législation ou [politique du Microsoft Store](/legal/windows/agreements/store-policies).

Nous n’informerons pas toutes les applications qui répondent à ces critères, mais inclurons celles-ci dans la mesure où nous développons progressivement notre programme.

### Désactivation de l’importation automatique du Microsoft Store

Votre PWA peut annuler l’importation automatique sur le Microsoft Store en fournissant un `robots.txt` fichier contenant ce qui suit:

```
User-agent: bingbot
Disallow: /manifest.json
```

Cela permet de diriger le robot Web robot (bingbot) pour ignorer votre fichier manifeste Web à des fins d’indexation dans Project Web App. Cela n’affectera pas le classement de recherche de votre site dans le [processus d’indexation Web](https://www.bing.com/webmaster/help/help-center-661b2d18)standard de Bing.
