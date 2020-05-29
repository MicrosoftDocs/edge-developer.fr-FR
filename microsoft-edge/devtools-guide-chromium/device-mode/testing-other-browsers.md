---
title: Émuler et tester d’autres navigateurs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 65ad10ff89d3e4c27abc97cea0eb18b15853dd2e
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607316"
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





# <span data-ttu-id="20150-103">Émuler et tester d’autres navigateurs</span><span class="sxs-lookup"><span data-stu-id="20150-103">Emulate and Test Other Browsers</span></span>   




<span data-ttu-id="20150-104">Votre travail ne se termine pas par le bon fonctionnement de votre site sur Microsoft Edge et Android.</span><span class="sxs-lookup"><span data-stu-id="20150-104">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="20150-105">Même si le mode périphérique est en mesure de simuler une gamme d’autres appareils tels que les iPhone, nous vous encourageons à consulter des solutions d’émulation fournies par d’autres navigateurs.</span><span class="sxs-lookup"><span data-stu-id="20150-105">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <span data-ttu-id="20150-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="20150-106">Summary</span></span>  

*   <span data-ttu-id="20150-107">Si vous n’avez pas de périphérique particulier ou si vous voulez effectuer une vérification ponctuelle sur un événement, la meilleure option consiste à émuler l’appareil directement dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="20150-107">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="20150-108">Les émulateurs et simulateurs d’appareil vous permettent de reproduire votre site de développement sur une gamme d’appareils de votre station de travail.</span><span class="sxs-lookup"><span data-stu-id="20150-108">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="20150-109">Les émulateurs basés sur le Cloud vous permettent d’automatiser les tests unitaires de votre site sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="20150-109">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <span data-ttu-id="20150-110">Émulateurs de navigateur</span><span class="sxs-lookup"><span data-stu-id="20150-110">Browser emulators</span></span>  

<span data-ttu-id="20150-111">Les émulateurs de navigateur permettent de tester la réactivité d’un site, mais chacun n’émule pas les différences de l’API, de la prise en charge CSS et de certains comportements que vous voyez dans un navigateur mobile.</span><span class="sxs-lookup"><span data-stu-id="20150-111">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that you see on a mobile browser.</span></span>  <span data-ttu-id="20150-112">Testez votre site dans les navigateurs qui s’exécutent sur des appareils réels pour être certain que tout se passe comme prévu.</span><span class="sxs-lookup"><span data-stu-id="20150-112">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <span data-ttu-id="20150-113">Mode de création réactif de Firefox</span><span class="sxs-lookup"><span data-stu-id="20150-113">Firefox Responsive Design View</span></span>  

<span data-ttu-id="20150-114">Firefox est doté d’un [mode de création réactif][MDNResponsiveDesignMode] qui vous encourage à ne pas réfléchir en termes de périphériques spécifiques et à envisager la modification de votre conception au sein de la taille d’écran courante ou en faisant glisser les bords.</span><span class="sxs-lookup"><span data-stu-id="20150-114">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <span data-ttu-id="20150-115">Émulation EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="20150-115">EdgeHTML Emulation</span></span>  

<span data-ttu-id="20150-116">Pour émuler des téléphones Windows, utilisez l' [émulation intégrée de][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="20150-116">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="20150-117">Utilisez l' [émulation Internet Explorer 11][Ie11DevToolsEmulation] pour simuler l’aspect de votre page dans les versions antérieures d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="20150-117">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <span data-ttu-id="20150-118">Émulateurs et simulateurs de périphériques</span><span class="sxs-lookup"><span data-stu-id="20150-118">Device emulators and simulators</span></span>  

<span data-ttu-id="20150-119">Les simulateurs de périphériques et émulateurs simulent pas uniquement l’environnement de navigateur, mais aussi l’appareil complet.</span><span class="sxs-lookup"><span data-stu-id="20150-119">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="20150-120">Chacun s’avère utile pour tester des éléments qui nécessitent une intégration du système d’exploitation (par exemple, l’entrée de formulaire avec un clavier virtuel).</span><span class="sxs-lookup"><span data-stu-id="20150-120">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <span data-ttu-id="20150-121">Émulateur Android</span><span class="sxs-lookup"><span data-stu-id="20150-121">Android Emulator</span></span>  

<!--
> ##### Figure old 1  
> Stock Browser in Android Emulator  
> ![Stock Browser in Android Emulator][ImageAndroidEmulatorStockBrowser]  
-->

<span data-ttu-id="20150-122">Pour le moment, il n’existe aucun moyen d’installer Microsoft Edge sur un émulateur Android.</span><span class="sxs-lookup"><span data-stu-id="20150-122">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="20150-123">Toutefois, vous pouvez utiliser le navigateur Android, l’interpréteur de contenus de chrome et Firefox pour Android, que nous allons examiner plus loin dans ce guide.</span><span class="sxs-lookup"><span data-stu-id="20150-123">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="20150-124">Le interpréteur de contenus de chrome exécute le même moteur de rendu de chrome que Microsoft Edge, mais sans fonctionnalités spécifiques du navigateur.</span><span class="sxs-lookup"><span data-stu-id="20150-124">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="20150-125">L’émulateur Android est fourni avec le SDK Android que vous devez télécharger dans le cadre de [Android Studio][AndroidStudioDownload].</span><span class="sxs-lookup"><span data-stu-id="20150-125">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="20150-126">Puis suivez les instructions de [configuration d’un appareil virtuel][AndroidStudioCreateManageVirtualDevices] et de [démarrage de l’émulateur][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="20150-126">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="20150-127">Une fois votre émulateur démarré, cliquez sur l’icône du navigateur et testez votre site dans l’ancien navigateur de cotation pour Android.</span><span class="sxs-lookup"><span data-stu-id="20150-127">Once your emulator is booted, click on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <span data-ttu-id="20150-128">Interpréteur de contenus de chrome sur Android</span><span class="sxs-lookup"><span data-stu-id="20150-128">Chromium Content Shell on Android</span></span>  

<!--
> ##### Figure old 2  
> Android Emulator Content Shell  
> ![Android Emulator Content Shell][ImageAndroidEmulatorContentShell]  
-->

<span data-ttu-id="20150-129">Pour installer l’interpréteur de contenus de chrome pour Android, laissez votre émulateur en cours d’exécution et exécutez les commandes suivantes à l’invite de commandes:</span><span class="sxs-lookup"><span data-stu-id="20150-129">To install the Chromium Content Shell for Android, leave your emulator running and run the following commands at a command prompt:</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="20150-130">Vous pouvez à présent tester votre site à l’aide de l’interpréteur de contenus de chrome.</span><span class="sxs-lookup"><span data-stu-id="20150-130">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <span data-ttu-id="20150-131">Firefox sur Android</span><span class="sxs-lookup"><span data-stu-id="20150-131">Firefox on Android</span></span>  

<!--
> ##### Figure old 3  
> Firefox Icon on Android Emulator  
> ![Firefox Icon on Android Emulator][ImageAndroidEmulatorFirefoxBrowser]  
-->

<span data-ttu-id="20150-132">Comme pour l’interpréteur de contenus de chrome, vous pouvez obtenir un APK pour installer Firefox sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="20150-132">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="20150-133">[Téléchargez le fichier. apk approprié][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="20150-133">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="20150-134">À partir de cet emplacement, vous pouvez installer le fichier sur un émulateur ouvert ou un appareil Android connecté à l’aide de la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="20150-134">From here, you are able to install the file onto an open emulator or connected Android device with the following command:</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <span data-ttu-id="20150-135">Simulateur iOS</span><span class="sxs-lookup"><span data-stu-id="20150-135">iOS Simulator</span></span>  

<span data-ttu-id="20150-136">Le simulateur iOS pour Mac OS X est fourni avec Xcode, que vous [Installez à partir de l’App Store][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="20150-136">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="20150-137">Lorsque vous avez travaillé, Apprenez à utiliser le simulateur dans la [documentation Apple pour développeurs][AppleSimulatorHelp].</span><span class="sxs-lookup"><span data-stu-id="20150-137">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="20150-138">Pour éviter d’avoir à ouvrir Xcode chaque fois que vous voulez utiliser le simulateur iOS, ouvrez-le, puis cliquez avec le bouton droit sur l’icône du simulateur iOS dans votre Dock et sélectionnez **garder dans le Dock**.</span><span class="sxs-lookup"><span data-stu-id="20150-138">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, then right-click the iOS Simulator icon in your dock and select **Keep in Dock**.</span></span>  <span data-ttu-id="20150-139">Cliquez sur cette icône dès que vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="20150-139">Now just click this icon whenever you need it.</span></span>  

###  <span data-ttu-id="20150-140">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="20150-140">Microsoft Edge (EdgeHTML)</span></span>  

> ##### <span data-ttu-id="20150-141">Figure1</span><span class="sxs-lookup"><span data-stu-id="20150-141">Figure 1</span></span>  
> <span data-ttu-id="20150-142">VM d’Internet Explorer modernes</span><span class="sxs-lookup"><span data-stu-id="20150-142">Modern IE VM</span></span>  
> <span data-ttu-id="20150-143">! [VM d’Internet Explorer moderne] [ImageVMModernIe]</span><span class="sxs-lookup"><span data-stu-id="20150-143">![Modern IE VM][ImageVMModernIe]</span></span>  

<span data-ttu-id="20150-144">Les machines virtuelles Microsoft Edge \ (EdgeHTML \) \ (VM \) vous permettent d’accéder aux différentes versions d’EdgeHTML et d’Internet Explorer sur votre ordinateur via VirtualBox \ (ou VMWare \).</span><span class="sxs-lookup"><span data-stu-id="20150-144">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="20150-145">[Dans la page de téléchargement][MicrosoftDeveloperEdgeVms], sélectionnez une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="20150-145">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <span data-ttu-id="20150-146">Émulateurs et simulateurs basés sur le Cloud</span><span class="sxs-lookup"><span data-stu-id="20150-146">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="20150-147">Si vous n’êtes pas en mesure d’utiliser les émulateurs et que vous n’avez pas accès à des appareils réels, les émulateurs de type Cloud sont les plus avantageux.</span><span class="sxs-lookup"><span data-stu-id="20150-147">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="20150-148">L’un des principaux avantages des émulateurs Cloud sur des appareils réels et des émulateurs locaux est que vous pouvez automatiser les tests unitaires de votre site sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="20150-148">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="20150-149">[BrowserStack (commercial)][|::ref1::|] est le moyen le plus facile à utiliser pour le test manuel.</span><span class="sxs-lookup"><span data-stu-id="20150-149">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="20150-150">Sélectionnez un système d’exploitation, sélectionnez la version de votre navigateur et le type de votre appareil, sélectionnez une URL pour la navigation, et il tourne sur un ordinateur virtuel hébergé avec lequel vous pouvez interagir.</span><span class="sxs-lookup"><span data-stu-id="20150-150">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="20150-151">Vous pouvez également exécuter plusieurs émulateurs dans le même écran, ce qui vous permet de tester l’apparence de votre application sur plusieurs appareils en même temps.</span><span class="sxs-lookup"><span data-stu-id="20150-151">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="20150-152">[SauceLabs (commercial)][SauceLabs] vous permet d’exécuter des tests unitaires au sein d’un émulateur, qui peuvent être très utiles pour l’écriture de scripts d’un flux sur votre site, ainsi que pour visionner l’enregistrement vidéo de cela sur différents appareils.</span><span class="sxs-lookup"><span data-stu-id="20150-152">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="20150-153">Vous pouvez également effectuer un test manuel sur votre site.</span><span class="sxs-lookup"><span data-stu-id="20150-153">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="20150-154">[Device Anywhere (commercial)][AppExperience] n’utilise pas d’émulateurs mais de véritables périphériques que vous pouvez contrôler à distance.</span><span class="sxs-lookup"><span data-stu-id="20150-154">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="20150-155">Cela est très utile dans les cas où vous avez besoin de reproduire un problème sur un appareil spécifique et que vous ne pouvez pas voir le bogue à l’aide de l’une des options dans les guides précédents.</span><span class="sxs-lookup"><span data-stu-id="20150-155">This is very useful in the event where you need to reproduce a problem on a specific device and are not able to see the bug using any of the options in the previous guides.</span></span>  

 



<!-- image links -->  

<!--[ImageAndroidEmulatorStockBrowser]: /microsoft-edge/devtools-guide-chromium/media/device-mode-android-emulator-stock-browser.msft.png "Figure old 1: Stock Browser in Android Emulator"  -->  
<!--[ImageAndroidEmulatorContentShell]: /microsoft-edge/devtools-guide-chromium/media/device-mode-android-avd-contentshell.msft.png "Figure old 2: Android Emulator Content Shell"  -->  
<!--[ImageAndroidEmulatorFirefoxBrowser]: /microsoft-edge/devtools-guide-chromium/media/device-mode-ff-on-android-emulator.msft.png "Figure old 3: Firefox Icon on Android Emulator"  -->  
[ImageVMModernIe]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Device-mode-Modern-IE-VM.msft.png "figure 1: VM de l’Internet Explorer moderne"  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML)-émulation"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Émuler les navigateurs, les tailles d’écran et les emplacements GPS"  

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
> <span data-ttu-id="20150-170">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20150-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="20150-171">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Paul Bakaus][PaulBakaus] \ (Open Web Developer défenseur sur Google | Outils, performances, animation, UX.</span><span class="sxs-lookup"><span data-stu-id="20150-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="20150-173">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20150-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
