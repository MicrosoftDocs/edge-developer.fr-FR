---
title: Émuler et tester d’autres navigateurs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d5eb33ea4cd1224930e91898d2c711310202cfc0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984978"
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





# Émuler et tester d’autres navigateurs   




Votre travail ne se termine pas par le bon fonctionnement de votre site sur Microsoft Edge et Android.  Même si le mode périphérique est en mesure de simuler une gamme d’autres appareils tels que les iPhone, nous vous encourageons à consulter des solutions d’émulation fournies par d’autres navigateurs.  

### Résumé  

*   Si vous n’avez pas de périphérique particulier ou si vous voulez effectuer une vérification ponctuelle sur un événement, la meilleure option consiste à émuler l’appareil directement dans votre navigateur.  
*   Les émulateurs et simulateurs d’appareil vous permettent de reproduire votre site de développement sur une gamme d’appareils de votre station de travail.  
*   Les émulateurs basés sur le Cloud vous permettent d’automatiser les tests unitaires de votre site sur différentes plateformes.  

## Émulateurs de navigateur  

Les émulateurs de navigateur permettent de tester la réactivité d’un site, mais chacun n’émule pas les différences de l’API, de la prise en charge CSS et de certains comportements que vous voyez dans un navigateur mobile.  Testez votre site dans les navigateurs qui s’exécutent sur des appareils réels pour être certain que tout se passe comme prévu.  

### Mode de création réactif de Firefox  

Firefox est doté d’un [mode de création réactif][MDNResponsiveDesignMode] qui vous encourage à ne pas réfléchir en termes de périphériques spécifiques et à envisager la modification de votre conception au sein de la taille d’écran courante ou en faisant glisser les bords.  

### Émulation EdgeHTML  

Pour émuler des téléphones Windows, utilisez l' [émulation intégrée de][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).  

Utilisez l' [émulation Internet Explorer 11][Ie11DevToolsEmulation] pour simuler l’aspect de votre page dans les versions antérieures d’Internet Explorer.  

## Émulateurs et simulateurs de périphériques  

Les simulateurs de périphériques et émulateurs simulent pas uniquement l’environnement de navigateur, mais aussi l’appareil complet.  Chacun s’avère utile pour tester des éléments qui nécessitent une intégration du système d’exploitation (par exemple, l’entrée de formulaire avec un clavier virtuel).  

### Émulateur Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

Pour le moment, il n’existe aucun moyen d’installer Microsoft Edge sur un émulateur Android.  Toutefois, vous pouvez utiliser le navigateur Android, l’interpréteur de contenus de chrome et Firefox pour Android, que nous allons examiner plus loin dans ce guide.  Le interpréteur de contenus de chrome exécute le même moteur de rendu de chrome que Microsoft Edge, mais sans fonctionnalités spécifiques du navigateur.  

L’émulateur Android est fourni avec le SDK Android que vous devez télécharger dans le cadre de [Android Studio][AndroidStudioDownload].  Puis suivez les instructions de [configuration d’un appareil virtuel][AndroidStudioCreateManageVirtualDevices] et de [démarrage de l’émulateur][AndroidStudioRunAppsAndroidEmulator].  
Une fois votre émulateur démarré, cliquez sur l’icône du navigateur et testez votre site dans l’ancien navigateur de cotation pour Android.  

#### Interpréteur de contenus de chrome sur Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Pour installer l’interpréteur de contenus de chrome pour Android, laissez votre émulateur en cours d’exécution et exécutez la commande suivante.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Vous pouvez à présent tester votre site à l’aide de l’interpréteur de contenus de chrome.  

#### Firefox sur Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Comme pour l’interpréteur de contenus de chrome, vous pouvez obtenir un APK pour installer Firefox sur l’émulateur.  

[Téléchargez le fichier. apk approprié][MozillaFirefoxDownload].  

Pour installer le fichier sur un émulateur ouvert ou un appareil Android connecté, exécutez la commande suivante.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### simulateur iOS  

Le simulateur iOS pour Mac OS X est fourni avec Xcode, que vous [Installez à partir de l’App Store][MacAppStoreXcode].  

Lorsque vous avez travaillé, Apprenez à utiliser le simulateur dans la [documentation Apple pour développeurs][AppleSimulatorHelp].  

> [!NOTE]
> Pour éviter d’avoir à ouvrir Xcode chaque fois que vous voulez utiliser le simulateur iOS, ouvrez-le, puis cliquez avec le bouton droit sur l’icône du simulateur iOS dans votre Dock et sélectionnez **garder dans le Dock**.  Cliquez sur cette icône dès que vous en avez besoin.  

###  Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM d’Internet Explorer modernes" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   VM d’Internet Explorer modernes  
:::image-end:::  

Les machines virtuelles Microsoft Edge \ (EdgeHTML \) \ (VM \) vous permettent d’accéder aux différentes versions d’EdgeHTML et d’Internet Explorer sur votre ordinateur via VirtualBox \ (ou VMWare \).  [Dans la page de téléchargement][MicrosoftDeveloperEdgeVms], sélectionnez une machine virtuelle.  

## Émulateurs et simulateurs basés sur le Cloud  

Si vous n’êtes pas en mesure d’utiliser les émulateurs et que vous n’avez pas accès à des appareils réels, les émulateurs de type Cloud sont les plus avantageux.  L’un des principaux avantages des émulateurs Cloud sur des appareils réels et des émulateurs locaux est que vous pouvez automatiser les tests unitaires de votre site sur différentes plateformes.  

*   [BrowserStack (commercial)][|::ref1::|] est le moyen le plus facile à utiliser pour le test manuel.  Sélectionnez un système d’exploitation, sélectionnez la version de votre navigateur et le type de votre appareil, sélectionnez une URL pour la navigation, et il tourne sur un ordinateur virtuel hébergé avec lequel vous pouvez interagir.  Vous pouvez également exécuter plusieurs émulateurs dans le même écran, ce qui vous permet de tester l’apparence de votre application sur plusieurs appareils en même temps.  
*   [SauceLabs (commercial)][SauceLabs] vous permet d’exécuter des tests unitaires au sein d’un émulateur, qui peuvent être très utiles pour l’écriture de scripts d’un flux sur votre site, ainsi que pour visionner l’enregistrement vidéo de cela sur différents appareils.  Vous pouvez également effectuer un test manuel sur votre site.  
*   [Device Anywhere (commercial)][AppExperience] n’utilise pas d’émulateurs mais de véritables périphériques que vous pouvez contrôler à distance.  Cela est très utile dans les cas où vous avez besoin de reproduire un problème sur un appareil spécifique et que vous ne pouvez pas voir le bogue à l’aide de l’une des options dans les guides précédents.  

<!--  
 


-->  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML)-émulation | Documents Microsoft"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Émuler les navigateurs, les tailles d’écran et les emplacements GPS | Documents Microsoft"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Télécharger des machines virtuelles"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Créer et gérer des périphériques virtuels | Développeurs Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Télécharger les outils Android Studio et SDK | Développeurs Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Exécuter des applications sur l’émulateur Android | Développeurs Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Interface de l’application"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Aide du simulateur-actuel | pomme"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "XCode sur le Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Mode création réactif | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Télécharger le navigateur Firefox"  
[SauceLabs]: https://saucelabs.com "Ateliers de sauce"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Paul Bakaus][PaulBakaus] \ (Open Web Developer défenseur sur Google | Outils, performances, animation, UX.  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
