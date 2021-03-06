---
description: Votre travail ne se termine pas par la garantie que votre site s’exécute bien sur Microsoft Edge et Android.  Même si le mode appareil est en mesure de simuler une plage d’autres appareils tels que les iPhones, nous vous encourageons à consulter des solutions pour l’émulation fournie par d’autres navigateurs.
title: Émuler et tester d'autres navigateurs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f2ca56c2e15f578a970e6ceb84b1554bfda53862
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564279"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="emulate-and-test-other-browsers"></a>Émuler et tester d'autres navigateurs  

Votre travail ne se termine pas par la garantie que votre site s’exécute bien sur Microsoft Edge et Android.  Même si le mode appareil est en mesure de simuler une plage d’autres appareils tels que les iPhones, nous vous encourageons à consulter des solutions pour l’émulation fournie par d’autres navigateurs.  

### <a name="summary"></a>Résumé  

*   Lorsque vous n’avez pas d’appareil particulier ou que vous souhaitez vérifier quelque chose, la meilleure option consiste à émuler l’appareil directement à l’intérieur de votre navigateur.  
*   Les émulateurs et simulateurs de périphériques vous permettent d’imiter votre site de développement sur une plage d’appareils de votre station de travail.  
*   Les émulateurs basés sur le cloud vous permettent d’automatiser des tests unitaires pour votre site sur différentes plateformes.  

## <a name="browser-emulators"></a>Émulateurs de navigateur  

Les émulateurs de navigateur sont parfaits pour tester la réactivité d’un site, mais ils n’émulent pas les différences d’API, de prise en charge CSS et de certains comportements affichés sur un navigateur mobile.  Testez votre site sur les navigateurs s’exécutant sur des appareils réels pour vérifier que tout se comporte comme prévu.  

### <a name="firefox-responsive-design-view"></a>Mode Création réactive Firefox  

Firefox dispose [][MDNResponsiveDesignMode] d’une vue de conception réactive qui vous encourage à cesser de penser en termes d’appareils spécifiques et à explorer la façon dont votre conception change à des tailles d’écran courantes ou à votre propre taille en faisant glisser les bords.  

### <a name="edgehtml-emulation"></a>Émulation EdgeHTML  

Pour émuler Windows téléphones, utilisez l’émulation intégrée Microsoft Edge [][ArchiveMicrosoftEdgeDevtoolsEmulation]\(EdgeHTML\).  

Utilisez [l’émulation d’Internet Explorer 11][Ie11DevToolsEmulation] pour simuler l’apparence de votre page dans les versions antérieures d’Internet Explorer.  

## <a name="device-emulators-and-simulators"></a>Émulateurs et simulateurs d’appareils  

Les simulateurs et émulateurs de périphériques simulent non seulement l’environnement du navigateur, mais l’ensemble de l’appareil.  Chacun d’eux est utile pour tester des éléments qui nécessitent une intégration du système d’exploitation, par exemple une entrée de formulaire avec des claviers virtuels.  

### <a name="android-emulator"></a>Émulateur Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

Pour le moment, il n’existe aucun moyen d’installer Microsoft Edge sur un émulateur Android.  Toutefois, vous pouvez utiliser le navigateur Android, Chromium Content Shell et Firefox pour Android que nous examinerons plus loin dans ce guide.  Chromium Content Shell exécute le même moteur de rendu Chromium que Microsoft Edge, mais n’offre aucune fonctionnalité spécifique au navigateur.  

L’émulateur Android est fourni avec le SDK Android que vous devez télécharger dans le cadre [d’Android Studio.][AndroidStudioDownload]  Suivez ensuite les instructions pour [configurer un périphérique virtuel][AndroidStudioCreateManageVirtualDevices] et démarrer [l’émulateur.][AndroidStudioRunAppsAndroidEmulator]  
Une fois votre émulateur démarré, sélectionnez l’icône Navigateur et testez votre site sur l’ancien navigateur Stock pour Android.  

#### <a name="chromium-content-shell-on-android"></a>Chromium shell de contenu sur Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Pour installer l’Chromium de contenu pour Android, laissez votre émulateur en cours d’exécution et exécutez la commande suivante.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Vous pouvez maintenant tester votre site avec l’Chromium de contenu.  

#### <a name="firefox-on-android"></a>Firefox sur Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

À l’Chromium de contenu, vous pouvez obtenir un APK pour installer Firefox sur l’émulateur.  

[Téléchargez le fichier .apk correct.][MozillaFirefoxDownload]  

Pour installer le fichier sur un émulateur ouvert ou un appareil Android connecté, exécutez la commande suivante.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a>Simulateur iOS  

Le simulateur iOS pour Mac OS X est livré avec Xcode, que vous [installez à partir de l’App Store.][MacAppStoreXcode]  

Lorsque vous avez terminé, découvrez comment travailler avec le simulateur à l’aide de la [documentation du développeur Apple.][AppleSimulatorHelp]  

> [!NOTE]
> Pour éviter d’avoir à ouvrir Xcode chaque fois que vous souhaitez utiliser le simulateur iOS, ouvrez-le, pointez sur l’icône simulateur iOS dans votre station d’accueil, ouvrez le menu contextuel \(clic droit\), puis choisissez Conserver dans la station **d’accueil.**  Maintenant, il vous suffit de choisir l’icône chaque fois que vous en avez besoin.  

###  <a name="microsoft-edge-edgehtml"></a>Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM IE moderne" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   VM IE moderne  
:::image-end:::  

Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) vous permettent d’accéder à différentes versions de EdgeHTML et d’IE sur votre ordinateur via VirtualBox \(ou VMWare\).  Choisissez une [machine virtuelle sur la page de téléchargement.][MicrosoftDeveloperEdgeVms]  

## <a name="cloud-based-emulators-and-simulators"></a>Émulateurs et simulateurs basés sur le cloud  

Si vous n’êtes pas en mesure d’utiliser les émulateurs et que vous n’avez pas accès à des appareils réels, les émulateurs basés sur le cloud sont la meilleure chose à faire.  L’un des grands avantages des émulateurs basés sur le cloud par rapport aux appareils réels et aux émulateurs locaux est que vous pouvez automatiser des tests unitaires pour votre site sur différentes plateformes.  

*   [BrowserStack (commercial)][|::ref1::|] est le plus simple à utiliser pour les tests manuels.  Vous sélectionnez un système d’exploitation, la version de votre navigateur et le type d’appareil, une URL à parcourir et une machine virtuelle hébergée avec laquelle vous pouvez interagir.  Vous pouvez également exécuter plusieurs émulateurs dans le même écran, ce qui vous permet de tester l’apparence de votre application sur plusieurs appareils en même temps.  
*   [Le contrôle ContrôleLabs (commercial)][SauceLabs] vous permet d’exécuter des tests unitaires à l’intérieur d’un émulateur, ce qui peut s’avérer très utile pour écrire des scripts dans votre site et regarder l’enregistrement vidéo de ce dernier sur différents appareils.  Vous pouvez également tester manuellement votre site.  
*   [Device Anywhere (commercial) n’utilise][AppExperience] pas d’émulateurs, mais des appareils réels que vous pouvez contrôler à distance.  Cela est très utile dans le cas où vous devez reproduire un problème sur un appareil spécifique et peut ne pas afficher le bogue à l’aide des options des guides précédents.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[ArchiveMicrosoftEdgeDevtoolsEmulation]: /archive/microsoft-edge/legacy/developer/devtools-guide/emulation "Émulation | Documents Microsoft"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Émuler les navigateurs, les tailles d’écran et les emplacements GPS | Documents Microsoft"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Télécharger des machines virtuelles"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Créer et gérer des périphériques virtuels | Développeurs Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Téléchargez les outils Android Studio et SDK | Développeurs Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Exécuter des applications sur l’émulateur Android | Développeurs Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Expérience d’application"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Aide du simulateur : | pomme"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode sur le Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Mode Création dynamique | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Télécharger firefox Browser"  
[SauceLabs]: https://saucelabs.com "Sauce Labs"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est co-auteure par [Meggin Kearney][MegginKearney] \(Tech Writer\) et [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate chez Google | [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) Outils, Performances, Animation, UX\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est sous [licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
