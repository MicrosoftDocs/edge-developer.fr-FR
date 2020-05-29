---
description: Assurez-vous que votre PWA offre une excellente interface pour Xbox
title: Personnaliser votre PWA pour Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ms.openlocfilehash: 8c2660c8821826660d2030f832ae449ff4a061ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566630"
---
# Applications Web progressives pour Xbox One

Vous pouvez prolonger une application Web afin de la rendre disponible en tant qu’application Xbox One via le Microsoft Store tout en continuant à utiliser vos infrastructures existantes, votre réseau de distribution de contenu et votre serveur principal.  Comme toutes les applications de plateforme Windows universelle (UWP), les applications Web progressives (PWAs) qui s’exécutent sur Xbox One peuvent également appeler des API Windows 10 natives.  Un certain nombre de PWAs sont déjà disponibles pour Xbox One, en particulier dans la catégorie des [applications de lecture de contenu multimédia](#media-pwas-on-xbox).  

Dans la plupart des cas, vous pouvez empaqueter votre application Project Web App pour Xbox One de la [même manière que pour Windows](./windows-features.md), à l’aide des outils du [Concepteur PWA](https://www.pwabuilder.com/) ou de l’environnement IDE [Visual Studio](https://visualstudio.microsoft.com/vs/) pour générer le fichier *appxmanifest* requis pour l’exécution de votre application Project Web App. Néanmoins, il existe plusieurs différences principales que ce guide va vous guider.

## Déploiement et test de PWAs sur Xbox

Pour commencer, procédez comme [suit pour activer le *mode développeur Xbox One* ](/windows/uwp/xbox-apps/devkit-activation) . Le mode développeur étant activé, [configurez *Device Portal pour Xbox* ](/windows/uwp/debug-test-perf/device-portal-xbox) afin d’obtenir l’accès à distance à votre Xbox à partir du navigateur dans votre environnement de développement.

Vous êtes maintenant prêt à déployer votre application à des fins de test à l’aide de *PWA Builder* ou *Visual Studio*.

### Option 1: concepteur PWA

Le [Concepteur PWA](https://www.pwabuilder.com/) est une application nœud. js que vous pouvez installer à partir de node Package Manager (NPM). Il utilise les métadonnées de votre site Web pour générer des applications hébergées natives sur Android, iOS et Windows. Si votre site comporte déjà un [manifeste de l’application Web](https://developer.mozilla.org/docs/Web/Manifest), le concepteur PWA l’utilise pour générer des packages d’installation spécifiques à la plateforme. Dans le cas contraire, le concepteur PWA génère un fichier *Manifest. JSON* de base en fonction des caractéristiques de votre site.

#### Configuration requise
 - [Node. js](https://nodejs.org/en/), qui inclut NPM.

#### Configuration

1. Ouvrez une invite de commandes de nœud pour installer le générateur PWA:

    ```
    npm install pwabuilder --global
    ```

2. Exécutez le générateur PWA sur l’URL de votre site Web:

    ```
    pwabuilder https://example.com/ -windows10
    ```

    L’indicateur *-Windows 10* limite la génération du package à Windows 10 (UWP). Vous pouvez l’omettre pour générer des packages sur toutes les plateformes prises en charge, y compris iOS et Android. Pour plus d’informations, consultez les [documents du concepteur PWA](https://docs.pwabuilder.com/) .

3. À partir de [Device Portal pour Xbox](/windows/uwp/debug-test-perf/device-portal-xbox), accédez à **page d’accueil**,  >  Sélectionnez l’option à partir de **& applications**  >  **Add**, choisissez l’option de *téléchargement de fichiers libres*, puis sélectionnez le dossier de manifeste de l’application Windows 10 généré par le concepteur PWA dans le répertoire actif.

4. Suivez les instructions de l’Assistant pour terminer le processus d’installation. Une fois l’installation terminée. vous pourrez voir et lancer votre compte PWA à partir du tableau de bord Xbox One.


### Option 2: Visual Studio

La [Communauté Visual Studio](https://visualstudio.microsoft.com/vs/community/) gratuite et complète de la 2017 communauté inclut des outils de développement de Windows 10, des modèles d’application universelles, un éditeur de code, un débogueur puissant, des émulateurs Windows Mobile, une prise en charge de plusieurs langues et bien plus encore, le tout prêt à être utilisé en production. Les versions [ *professionnel* et *entreprise* ](https://visualstudio.microsoft.com/vs/compare/) fournissent encore plus de fonctionnalités.

#### Configuration requise

 - [**Visual Studio 2017**](https://visualstudio.microsoft.com/vs/
): n’importe quelle version, y compris la *communauté* gratuite Edition.
 - [**Kit de développement logiciel (SDK) Windows 10**](/windows/uwp/xbox-apps/development-environment-setup): sélectionnez ce composant facultatif dans le *programme d’installation de Visual Studio 2017*.

#### Configuration

1. Suivez les étapes de [configuration et d’exécution de votre PWA en tant qu’application Windows universelle](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#set-up-and-run-your-universal-windows-app). Vous aurez ainsi une application Windows 10 entièrement fonctionnelle capable d’accéder aux API Windows universelles.

2. Vous pouvez désormais déployer et déboguer votre PWA (en tant qu’application UWP) sur Xbox One (comme avec n’importe quel autre appareil distant Windows 10) à l’aide du [débogueur distant Visual Studio](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017
). Vous pouvez également installer votre système de Project Web App à l’aide [de Device Portal pour Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) en procédant comme suit.

3. À partir de Device Portal pour Xbox, accédez à Accueil > mes jeux & applications > ajouter, sélectionnez l’option permettant de télécharger le *package d’application et les dépendances*.

4. Accédez au dossier de package que vous avez généré pour votre application à l’étape 1, puis sélectionnez le fichier *. AppX* à télécharger. Le [fichier *. AppX* ](/windows/uwp/packaging/packaging-uwp-apps) est un fichier de package d’application UWP qui peut être chargée sur n’importe quel appareil à des fins de test.

5. Appuyez ensuite sur le bouton **dépendances** et sélectionnez le sous-dossier *Dependencies* pour votre application et chargez chacun d’eux. Cette étape est uniquement requise pour le déploiement d’applications à partir de Device Portal pour Xbox. Visual Studio fournit des dépendances lors du débogage distant et de l’ordinateur de l’utilisateur final disposant déjà de ces éléments installés lors de leur remise sur le Microsoft Store.

6. Lorsque le package d’application et les dépendances sont chargés, cliquez sur le bouton **Go** situé sous la section *Deploy* pour installer l’application. Vous êtes prêt à lancer votre application sur Xbox!

## Considérations relatives à l’expérience utilisateur pour PWAs sur Xbox

### Conception «10-foot»

La console Xbox One est considérée comme une «interface «10-foot», ce qui signifie que vos utilisateurs seront probablement assis à un minimum de 3 mètres de votre écran. Par exemple, considérez l’utilisation de votre application à cette distance par rapport à l’expérience de navigateur Web de bureau classique avec une souris et un clavier. Pour plus d’informations sur les recommandations en matière de conception et d’expérience utilisateur, voir [conception pour Xbox et télévision](/windows/uwp/design/devices/designing-for-tv).

### Comprendre les «SafeZone TV»

Les fabricants de télévision appliquent une [«zone sécurisée»](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) dans le contenu qui peut capturer votre application. Par défaut, nous appliquons une bordure sécurisée autour de votre application, mais vous pouvez vous assurer que votre application prend en compte la taille de l’écran en appelant [`setDesiredBoundsMode`](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) et en spécifiant [`useCoreWindow`](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode) :

```JavaScript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```

Pour plus d’informations, consultez la [`Windows.UI.ViewManagement`](/uwp/api/windows.ui.viewmanagement) documentation relative aux espaces de noms.

### Gérer le focus et la navigation XY

Les méthodes d’entrée utilisateur pour Xbox sont le boîtier de commande ou la télécommande qui utilise un [système de navigation](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction)en mode XY, ce qui permet à l’utilisateur de déplacer le focus d’un contrôle à l’autre en le déplaçant vers le haut, le bas, la gauche et la droite.

Par exemple, vous souhaiterez peut-être que votre application fonctionne correctement avec la navigation en mode XY. Veillez également à [désactiver le *mode souris*](/windows/uwp/xbox-apps/how-to-disable-mouse-mode), qui est activé par défaut pour les applications UWP (et probablement non applicable à l’interface Xbox de votre application).

Le code suivant désactive le `mouse` mode et permet l’entrée de boîtier de commande pour générer des événements de clavier DOM:

```JavaScript
navigator.gamepadInputEmulation = "keyboard";
```

Vous pouvez `gamepad` également spécifier, ce qui désactive la souris, ne génère pas d’événements de clavier DOM et vous permet d’utiliser les API de boîtier de connexion Web et/ou WinRT standard.

Pour activer la navigation directionnelle, voir la [bibliothèque TVJS](#tvjs), abordée plus loin.

### TVJS

[TVJS est une collection de bibliothèques d’assistance](https://github.com/Microsoft/TVHelpers) qui facilitent la création d’applications Web pour les téléviseurs. Si vous créez une application Web hébergée qui s’exécute également sur la console Xbox, TVJS peut vous aider à ajouter de la prise en charge de la *navigation directionnelle*, et fournir plusieurs contrôles qui simplifient l’interaction avec le contenu sur le téléviseur.

La [navigation directionnelle](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) est une fonctionnalité TVJS qui offre une navigation à deux dimensions automatique dans les pages de votre application de télévision. Il n’est pas nécessaire de détecter et de gérer la navigation dans les pages de votre application, ou de spécifier explicitement toutes les cibles de focus valides pour chaque élément de l’interface utilisateur. La gestion automatique du Focus permet aux utilisateurs de se déplacer d’une manière intuitive et fiable.

Lorsque l’utilisateur navigue dans l’interface utilisateur de l’application à l’aide des boutons d’orientation du contrôleur, l’algorithme de focus automatique examine l’ensemble des cibles de focus potentielles, détermine l’élément suivant sur lequel se déplacer, puis définit automatiquement le focus sur cet élément. Pour déterminer l’élément suivant, l’algorithme combine l’entrée directionnelle, l’historique du focus passé et la disposition physique des éléments d’interface utilisateur de la page.

Pour activer la navigation directionnelle, incluez la référence de script suivante:

```HTML
<script src="directionalnavigation-1.0.0.0.js"></script>
```

Par défaut, seuls `<a>` , `<button>` , `<input>` `<select>` et `<textarea>` les éléments peuvent être actifs. Pour activer le focus sur d’autres éléments, attribuez-leur une [IndexTabulation](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)valide.

```HTML
<div tabindex="0″>This div is eligible for focus</div>
```

Pour plus d’informations sur la façon de modifier l’élément racine, de définir le focus initial, de remplacer le focus suivant, d’optimiser les contrôles pour le focus, et de personnaliser l’entrée, consultez la documentation [DirectionalNavigation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) . Il existe également un certain nombre d’autres exemples utiles.

## Media PWAs sur Xbox

Si vous créez une lecture de contenu multimédia PWA pour Xbox One, tenez compte des points suivants.

### Extensions multimédias chiffrées (Encrypted) dans le navigateur

Le navigateur Microsoft Edge sur Xbox One ne prend pas en charge les [extensions multimédias chiffrées](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) (Encrypted). Si votre support de votre application Media App utilise la gestion des droits numériques (DRM), vous ne pouvez pas l’exécuter à partir du navigateur sur votre Xbox. Au lieu de cela, vous devez le prototyper et le tester en tant qu' [application Xbox One à l’aide de PWABuilder ou Visual Studio](#deploying-and-testing-pwas-on-xbox), comme décrit ci-dessus. Vous pouvez également l’exécuter sur le navigateur Microsoft Edge sous Windows, où Encrypted est entièrement pris en charge.

### Intégration aux contrôles de transport de média système

Si votre application est une application multimédia, il est important que votre application réponde aux contrôles multimédias initiés par l’utilisateur via des boutons à l’écran, des [commandes vocales Cortana](https://support.xbox.com/xbox-one/console/cortana-voice-commands), des [contrôles de transport de média système](/windows/uwp/audio-video-camera/system-media-transport-controls) dans le volet de navigation ou des applications [Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) et [Xbox One SmartGlass](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) sur d’autres appareils. Jetez un coup d’œil au contrôle [MediaPlayer](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) de la [bibliothèque TVJS](#tvjs), qui s’intègre automatiquement à ces contrôles. Vous pouvez également [intégrer manuellement les contrôles de transport de média système](https://msdn.microsoft.com/windows/uwp/audio-video-camera/system-media-transport-controls).

### Chiffrement de contenu PlayReady

Au moment de l’écriture, la [ `cbcs` prise en charge du codage est limitée](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) au client PlayReady pour Xbox One (version 1709 ou ultérieure). Si les éléments multimédias de votre application Project ne prennent pas en charge le chiffrement *CBCS* , sachez que les fonctionnalités de votre application seront probablement limitées (ou entièrement indisponibles) sur Windows.



## Voir également
[Vidéo d’arête du Sud](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video): exemple d’application de vidéo pour Xbox créée avec réagi. js et hébergée sur un serveur Web.

[Conception pour Xbox et TV](/windows/uwp/design/devices/designing-for-tv): concevez votre application de plateforme Windows universelle (UWP) de façon à ce qu’elle s’affiche correctement et qu’elle fonctionne bien sur les écrans Xbox One et de télévision.

[Meilleures pratiques Xbox](/windows/uwp/xbox-apps/tailoring-for-xbox): suivez ces meilleures pratiques pour personnaliser votre application pour Xbox One.

[PWAS dans le Microsoft Store](/microsoft-edge/progressive-web-apps-edgehtml/microsoft-store): Voici comment (et pourquoi!) transmettre votre PWA au Microsoft Store.

[UWP sur Xbox One](/windows/uwp/xbox-apps/): Guide complet du développement d’applications UWP pour Xbox One.
