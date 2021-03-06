---
description: Débogage à distance du contenu en direct sur un appareil Android à partir d’un ordinateur Windows ou macOS.
title: Mise en place du débogage à distance des appareils Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 61fad793ca03dbef68a5f769dbfd25e780fd9930
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398258"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="get-started-with-remote-debugging-android-devices"></a>Mise en place du débogage à distance des appareils Android  

Déboguer à distance du contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.  La page de didacticiel suivante vous apprend à effectuer les actions suivantes.  

*   Configurer votre appareil Android pour le débogage à distance et le découvrir à partir de votre ordinateur de développement.  
*   Inspectez et déboguer le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.  
*   Contenu de la capture vidéo de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Le débogage à distance de l’application Microsoft Edge sur les appareils iOS n’est actuellement pas pris en charge.  Le guide suivant est spécifiquement axé sur le débogage à distance de Microsoft Edge sur les appareils Android.
> Si vous avez un appareil macOS, suivez le guide de [débogage Brightcove][BrightcoveSupportDebuggingMobileDevices] pour déboguer Microsoft Edge à distance sur un appareil iOS à l’aide de Safari.  Pour plus d’informations sur l’outil Inspecteur web dans Safari, accédez à [Safari Web Development Tools][AppleDeveloperSafariTools].  

## <a name="step-1-discover-your-android-device"></a>Étape 1 : Découvrir votre appareil Android  

Le flux de travail ci-dessous fonctionne pour la plupart des utilisateurs.  Pour plus d’aide, accédez à Résolution des problèmes [: DevTools](#troubleshooting-devtools-is-not-detecting-the-android-device) ne détecte pas la section d’appareil Android.  

1.  Ouvrez **l’écran Options du** développeur sur votre android.  Pour plus d’informations, [accédez à Configurer les options du développeur sur appareil.][AndroidDeveloperStudioDevOptions]  
1.  Choisissez **Activer le débogage USB.**  
1.  Sur votre ordinateur de développement, ouvrez Microsoft Edge.  
1.  Accédez à `edge://inspect` la page dans Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Page de edge://inspect dans Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Figure1.  Page `edge://inspect` dans Microsoft Edge  
    :::image-end:::  
    
1.  Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.  La première fois que vous essayez de vous connecter, une invite doit s’afficher sur DevTools détectant un appareil inconnu.  Acceptez **l’invite d’autorisation Autoriser le débogage USB** sur votre appareil Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Invite d’autorisation Autoriser le débogage USB sur un appareil Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Figure2.  Invite **d’autorisation Autoriser le débogage USB** sur un appareil Android  
    :::image-end:::  
    
1.  Si le nom de modèle de votre appareil Android s’affiche, Microsoft Edge a correctement établi la connexion à votre appareil.  Continuez [jusqu’à la section Étape 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a>Résolution des problèmes : DevTools ne détecte pas l’appareil Android  

Utilisez les conseils suivants pour vous aider à résoudre les problèmes de paramètres corrects pour votre matériel.  

*   Si vous utilisez un concentrateur USB, essayez de connecter votre appareil Android directement à votre ordinateur de développement.  
*   Essayez de débrancher le câble USB entre votre appareil Android et votre ordinateur de développement, puis de le brancher à nouveau.  Terminez la tâche pendant que vos écrans d’ordinateur Android et de développement sont déverrouillés.  
*   Assurez-vous que votre câble USB fonctionne.  Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.  

Utilisez les conseils suivants pour vérifier que votre logiciel est correctement installé.  

*   Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB de votre appareil Android.  Pour plus d’informations, [accédez à Installer des pilotes USB OEM.][AndroidDeveloperToolsOemUsb]  
*   Certaines combinaisons d’appareils Windows et Android \(notamment Samsung\) nécessitent des paramètres supplémentaires.  Pour plus d’informations, accédez [à DevTools Devices does not detect device when plugged in][Stackoverflow21925992].  

Utilisez les conseils suivants pour vous aider à résoudre les problèmes si l’invite Autoriser le **débogage USB** n’est pas affichée sur votre appareil Android.  

*   Déconnexion, puis nouvelle connexion du câble USB pendant que DevTools est en focus sur votre ordinateur de développement et que votre écran d’accueil Android s’affiche.  
    
    > [!NOTE]
    > L’invite s’affiche si vos écrans d’ordinateur Android ou de développement sont verrouillés.  

*   Mise à jour des paramètres d’affichage de votre appareil Android et de votre ordinateur de développement afin que chacun ne soit jamais mis en veille.  
*   Définition du mode USB pour Android sur PTP.  Pour plus d’informations, accédez à La boîte de dialogue Autoriser le débogage USB n’apparaît pas dans La boîte de dialogue Autoriser le [débogage USB.][StackexchangeAndroid101933]  
*   Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.  

Si vous trouvez une solution qui n’est pas mentionnée sur cette page ou dans [DevTools Devices][Stackoverflow21925992] ne détecte pas l’appareil lorsqu’il est branché sur Stack Overflow, ajoutez votre solution à la question Stack Overflow.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->.  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a>Étape 2 : Déboguer le contenu de votre appareil Android à partir de votre ordinateur de développement  

1.  Ouvrez Microsoft Edge sur votre appareil Android.  
1.  Accédez `edge://inspect` à , le nom de modèle de votre appareil Android s’affiche, suivi du numéro de série de l’appareil.  En dessous de cela, la version de Microsoft Edge en cours d’exécution sur l’appareil doit être affichée, avec le numéro de version entre parenthèses.  Chaque onglet Microsoft Edge ouvert obtient une section unique.  Vous pouvez interagir avec cet onglet à partir d’une section.  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un appareil distant connecté" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Figure3.  Un appareil distant connecté  
    :::image-end:::  
    
1.  Dans **l’onglet Ouvrir avec une zone** de texte d’URL, entrez une URL, puis choisissez **Ouvrir**.  La page s’ouvre dans un nouvel onglet sur votre appareil Android.  
1.  Sélectionnez **Inspecter** en côté de l’URL que vous ouvrez.  Une nouvelle instance DevTools s’ouvre.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a>Autres actions : mise au point, actualisation ou fermeture d’un onglet  

Choisissez **l’onglet Focus,** **rechargez**ou fermez-le à côté de l’onglet que vous souhaitez mettre au point, actualiser ou fermer. ****  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Boutons de mise au point, d’actualisation ou de fermeture d’un onglet" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Figure4.  Boutons de mise au point, d’actualisation ou de fermeture d’un onglet  
:::image-end:::  

### <a name="inspect-elements"></a>Inspecter les éléments  

Accédez à **l’outil Elements** de votre instance DevTools et pointez sur un élément pour le mettre en surbrillation dans la vue de votre appareil Android.  

Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans **l’outil Éléments.**  Sélectionnez **l’icône** Select Element \( Select Element \) sur votre ![ instance DevTools, puis sélectionnez l’élément sur l’écran de ][ImageSelectElementIcon] votre appareil Android.  

> [!NOTE]
> **Select Element** est désactivé après la première sélection. Vous devez donc le réactiver chaque fois que vous souhaitez utiliser la fonctionnalité.  

### <a name="screencast-your-android-screen-to-your-development-machine"></a>Capture d’écran de votre écran Android sur votre ordinateur de développement  

Choisissez **l’icône Deggle Screencast** \( Toggle Screencast \) pour afficher le contenu de votre appareil Android dans votre ![ instance ][ImageToggleScreencastIcon] DevTools.  

Vous pouvez interagir avec la capture vidéo des manières suivantes.  

*   Les choix sont convertis en pressions, ce qui permet de tirer les événements tactiles appropriés sur l’appareil.  
*   Les frappes de touches sur votre ordinateur sont envoyées à l’appareil.  
*   Pour simuler un mouvement de pincement, maintenez le doigt `Shift` en cours de glissement.  
*   Pour faire défiler la souris, utilisez votre trackpad ou votre roulette de souris, ou fling avec votre pointeur de souris.

> [!NOTE]
> Utilisez les conseils suivants pour vous aider à faire une capture vidéo.  
> 
> *   Les captures d’écran affichent uniquement le contenu de la page.  Les parties transparentes de la capture vidéo représentent des interfaces d’appareil, telles que la barre d’adresses Microsoft Edge, la barre d’état Android ou le clavier Android.  
> *   Les captures vidéo affectent négativement les taux d’images.  Désactivez la capture vidéo lors de la mesure des défilements ou des animations pour obtenir une image plus précise des performances de votre page.  
> *   Si l’écran de votre appareil Android se verrouille, le contenu de votre capture vidéo disparaît.  Déverrouillez l’écran de votre appareil Android pour reprendre automatiquement la capture vidéo.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurer les options du développeur sur l’appareil | Développeur Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Outils de développement web Safari | Développeur Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Débogage sur les appareils mobiles | Prise en charge de Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb - Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevTools Devices does not detect device when plugged in - Stack Overflow"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
