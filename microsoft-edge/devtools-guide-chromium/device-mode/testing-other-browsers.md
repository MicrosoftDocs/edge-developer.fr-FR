---
description: Votre travail ne se termine pas par la garantie que votre site s’exécute bien sur Microsoft Edge et Android.  Même si le mode appareil est en mesure de simuler une plage d’autres appareils tels que les iPhones, nous vous encourageons à consulter des solutions pour l’émulation fournie par d’autres navigateurs.
title: Émuler et tester d'autres navigateurs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 22153a54df7c5b92236a745be8e3bbac9a52d247
ms.sourcegitcommit: fa8bedfc83fbd1c4ce7bda8c69586c4f24007beb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11481365"
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
# <a name="emulate-and-test-other-browsers"></a><span data-ttu-id="4848c-105">Émuler et tester d'autres navigateurs</span><span class="sxs-lookup"><span data-stu-id="4848c-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="4848c-106">Votre travail ne se termine pas par la garantie que votre site s’exécute bien sur Microsoft Edge et Android.</span><span class="sxs-lookup"><span data-stu-id="4848c-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="4848c-107">Même si le mode appareil est en mesure de simuler une plage d’autres appareils tels que les iPhones, nous vous encourageons à consulter des solutions pour l’émulation fournie par d’autres navigateurs.</span><span class="sxs-lookup"><span data-stu-id="4848c-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <a name="summary"></a><span data-ttu-id="4848c-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4848c-108">Summary</span></span>  

*   <span data-ttu-id="4848c-109">Lorsque vous n’avez pas d’appareil particulier ou que vous souhaitez vérifier quelque chose, la meilleure option consiste à émuler l’appareil directement à l’intérieur de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="4848c-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="4848c-110">Les émulateurs et simulateurs de périphériques vous permettent d’imiter votre site de développement sur une plage d’appareils de votre station de travail.</span><span class="sxs-lookup"><span data-stu-id="4848c-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="4848c-111">Les émulateurs basés sur le cloud vous permettent d’automatiser des tests unitaires pour votre site sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="4848c-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <a name="browser-emulators"></a><span data-ttu-id="4848c-112">Émulateurs de navigateur</span><span class="sxs-lookup"><span data-stu-id="4848c-112">Browser emulators</span></span>  

<span data-ttu-id="4848c-113">Les émulateurs de navigateur sont parfaits pour tester la réactivité d’un site, mais ils n’émulent pas les différences d’API, de prise en charge CSS et de certains comportements affichés sur un navigateur mobile.</span><span class="sxs-lookup"><span data-stu-id="4848c-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that is displayed on a mobile browser.</span></span>  <span data-ttu-id="4848c-114">Testez votre site sur les navigateurs s’exécutant sur des appareils réels pour vérifier que tout se comporte comme prévu.</span><span class="sxs-lookup"><span data-stu-id="4848c-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <a name="firefox-responsive-design-view"></a><span data-ttu-id="4848c-115">Mode Création réactive Firefox</span><span class="sxs-lookup"><span data-stu-id="4848c-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="4848c-116">Firefox dispose [][MDNResponsiveDesignMode] d’une vue de conception réactive qui vous encourage à cesser de penser en termes d’appareils spécifiques et à explorer la façon dont votre conception change à des tailles d’écran courantes ou à votre propre taille en faisant glisser les bords.</span><span class="sxs-lookup"><span data-stu-id="4848c-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <a name="edgehtml-emulation"></a><span data-ttu-id="4848c-117">Émulation EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="4848c-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="4848c-118">Pour émuler les Windows Phone, utilisez [l’émulation][ArchiveMicrosoftEdgeDevtoolsEmulation]intégrée Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="4848c-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][ArchiveMicrosoftEdgeDevtoolsEmulation].</span></span>  

<span data-ttu-id="4848c-119">Utilisez [l’émulation d’Internet Explorer 11][Ie11DevToolsEmulation] pour simuler l’apparence de votre page dans les versions antérieures d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4848c-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <a name="device-emulators-and-simulators"></a><span data-ttu-id="4848c-120">Émulateurs et simulateurs d’appareils</span><span class="sxs-lookup"><span data-stu-id="4848c-120">Device emulators and simulators</span></span>  

<span data-ttu-id="4848c-121">Les simulateurs et émulateurs de périphériques simulent non seulement l’environnement du navigateur, mais l’ensemble de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4848c-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="4848c-122">Chacun d’eux est utile pour tester les éléments qui nécessitent une intégration du système d’exploitation, par exemple une entrée de formulaire avec des claviers virtuels.</span><span class="sxs-lookup"><span data-stu-id="4848c-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <a name="android-emulator"></a><span data-ttu-id="4848c-123">Émulateur Android</span><span class="sxs-lookup"><span data-stu-id="4848c-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="4848c-124">Pour le moment, il n’existe aucun moyen d’installer Microsoft Edge sur un émulateur Android.</span><span class="sxs-lookup"><span data-stu-id="4848c-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="4848c-125">Toutefois, vous pouvez utiliser le navigateur Android, l’Chromium Content Shell et Firefox pour Android que nous examinerons plus loin dans ce guide.</span><span class="sxs-lookup"><span data-stu-id="4848c-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="4848c-126">Chromium Content Shell exécute le même moteur de rendu Chromium que Microsoft Edge, mais n’offre aucune fonctionnalité spécifique au navigateur.</span><span class="sxs-lookup"><span data-stu-id="4848c-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="4848c-127">L’émulateur Android est fourni avec le SDK Android que vous devez télécharger dans le cadre [d’Android Studio.][AndroidStudioDownload]</span><span class="sxs-lookup"><span data-stu-id="4848c-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="4848c-128">Suivez ensuite les instructions pour [configurer un périphérique virtuel et][AndroidStudioCreateManageVirtualDevices] démarrer [l’émulateur.][AndroidStudioRunAppsAndroidEmulator]</span><span class="sxs-lookup"><span data-stu-id="4848c-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="4848c-129">Une fois votre émulateur démarré, sélectionnez l’icône Navigateur et testez votre site sur l’ancien navigateur Stock pour Android.</span><span class="sxs-lookup"><span data-stu-id="4848c-129">Once your emulator is booted, choose on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <a name="chromium-content-shell-on-android"></a><span data-ttu-id="4848c-130">Shell de contenu Chromium sur Android</span><span class="sxs-lookup"><span data-stu-id="4848c-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="4848c-131">Pour installer l’Chromium Content Shell pour Android, laissez votre émulateur en cours d’exécution et exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="4848c-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="4848c-132">Vous pouvez maintenant tester votre site avec l’Chromium Content Shell.</span><span class="sxs-lookup"><span data-stu-id="4848c-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <a name="firefox-on-android"></a><span data-ttu-id="4848c-133">Firefox sur Android</span><span class="sxs-lookup"><span data-stu-id="4848c-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="4848c-134">À l’exemple de l’Chromium Content Shell, vous pouvez obtenir un APK pour installer Firefox sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="4848c-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="4848c-135">[Téléchargez le fichier .apk correct.][MozillaFirefoxDownload]</span><span class="sxs-lookup"><span data-stu-id="4848c-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="4848c-136">Pour installer le fichier sur un émulateur ouvert ou un appareil Android connecté, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="4848c-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a><span data-ttu-id="4848c-137">Simulateur iOS</span><span class="sxs-lookup"><span data-stu-id="4848c-137">iOS simulator</span></span>  

<span data-ttu-id="4848c-138">Le simulateur iOS pour Mac OS X est livré avec Xcode, que vous [installez à partir de l’App Store.][MacAppStoreXcode]</span><span class="sxs-lookup"><span data-stu-id="4848c-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="4848c-139">Lorsque vous avez terminé, découvrez comment travailler avec le simulateur à l’aide de la [documentation du développeur Apple.][AppleSimulatorHelp]</span><span class="sxs-lookup"><span data-stu-id="4848c-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="4848c-140">Pour éviter d’avoir à ouvrir Xcode chaque fois que vous souhaitez utiliser le simulateur iOS, ouvrez-le, pointez sur l’icône simulateur iOS dans votre station d’accueil, ouvrez le menu contextuel \(clic droit\), puis choisissez Conserver dans la station **d’accueil.**</span><span class="sxs-lookup"><span data-stu-id="4848c-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, hover on the iOS Simulator icon in your dock, open the contextual menu \(right-click\), and choose **Keep in Dock**.</span></span>  <span data-ttu-id="4848c-141">Maintenant, il vous suffit de choisir l’icône chaque fois que vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="4848c-141">Now just choose the icon whenever you need it.</span></span>  

###  <a name="microsoft-edge-edgehtml"></a><span data-ttu-id="4848c-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4848c-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM IE moderne" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="4848c-144">VM IE moderne</span><span class="sxs-lookup"><span data-stu-id="4848c-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="4848c-145">Les machines virtuelles Microsoft Edge \(EdgeHTML\) \(VMs\) vous permettent d’accéder à différentes versions de EdgeHTML et d’Internet IE sur votre ordinateur via VirtualBox \(ou VMWare\).</span><span class="sxs-lookup"><span data-stu-id="4848c-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="4848c-146">Choisissez une [machine virtuelle sur la page de téléchargement.][MicrosoftDeveloperEdgeVms]</span><span class="sxs-lookup"><span data-stu-id="4848c-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <a name="cloud-based-emulators-and-simulators"></a><span data-ttu-id="4848c-147">Émulateurs et simulateurs basés sur le cloud</span><span class="sxs-lookup"><span data-stu-id="4848c-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="4848c-148">Si vous n’êtes pas en mesure d’utiliser les émulateurs et que vous n’avez pas accès à des appareils réels, les émulateurs basés sur le cloud sont la meilleure chose à faire.</span><span class="sxs-lookup"><span data-stu-id="4848c-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="4848c-149">L’un des grands avantages des émulateurs basés sur le cloud par rapport aux appareils réels et aux émulateurs locaux est que vous pouvez automatiser des tests unitaires pour votre site sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="4848c-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="4848c-150">[BrowserStack (commercial)][|::ref1::|] est le plus simple à utiliser pour les tests manuels.</span><span class="sxs-lookup"><span data-stu-id="4848c-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="4848c-151">Vous sélectionnez un système d’exploitation, la version de votre navigateur et le type d’appareil, une URL à parcourir et une machine virtuelle hébergée avec laquelle vous pouvez interagir.</span><span class="sxs-lookup"><span data-stu-id="4848c-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="4848c-152">Vous pouvez également exécuter plusieurs émulateurs dans le même écran, ce qui vous permet de tester l’apparence de votre application sur plusieurs appareils en même temps.</span><span class="sxs-lookup"><span data-stu-id="4848c-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="4848c-153">[Le contrôle ContrôleLabs (commercial)][SauceLabs] vous permet d’exécuter des tests unitaires à l’intérieur d’un émulateur, ce qui peut s’avérer très utile pour écrire des scripts dans votre site et regarder l’enregistrement vidéo de ce dernier sur différents appareils.</span><span class="sxs-lookup"><span data-stu-id="4848c-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="4848c-154">Vous pouvez également tester manuellement votre site.</span><span class="sxs-lookup"><span data-stu-id="4848c-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="4848c-155">[Device Anywhere (commercial) n’utilise][AppExperience] pas d’émulateurs, mais des appareils réels que vous pouvez contrôler à distance.</span><span class="sxs-lookup"><span data-stu-id="4848c-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="4848c-156">Ceci est très utile dans le cas où vous devez reproduire un problème sur un appareil spécifique et peut ne pas afficher le bogue à l’aide des options des guides précédents.</span><span class="sxs-lookup"><span data-stu-id="4848c-156">This is very useful in the event where you need to reproduce a problem on a specific device and may not display the bug using any of the options in the previous guides.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4848c-157">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="4848c-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="4848c-171">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4848c-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4848c-172">La page d’origine est trouvée ici et est co-auteure par [Meggin Kearney][MegginKearney] \(Tech Writer\) et [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate chez Google | [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) Outils, Performances, Animation, UX\).</span><span class="sxs-lookup"><span data-stu-id="4848c-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4848c-174">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4848c-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
