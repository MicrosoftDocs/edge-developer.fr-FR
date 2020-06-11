---
title: Découvrir les appareils Android de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: c77633c4844f0e576b7dff6574000a78c8c083da
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708535"
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

# Découvrir les appareils Android de débogage à distance  

Déboguez à distance le contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.  La page du didacticiel suivante vous explique comment effectuer les opérations suivantes.  

*   Configurez votre appareil Android pour le débogage à distance et découvrez-le à partir de votre ordinateur de développement.  
*   Inspectez et déboguez le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.  
*   Contenu Screencast de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Le débogage à distance de l’application Microsoft Edge sur les appareils iOS n’est pas pris en charge pour le moment.  Le guide suivant est particulièrement axé sur le débogage à distance de Microsoft Edge sur les appareils Android.
> Si vous avez un appareil macOS, suivez le [Guide de débogage de Brightcove][BrightcoveSupportDebuggingMobileDevices] pour déboguer à distance Microsoft Edge sur un appareil iOS à l’aide de Safari.  Pour plus d’informations sur l’outil inspecteur Web dans Safari, voir [outils de développement Web Safari][AppleDeveloperSafariTools].  

## Étape 1: découvrir votre appareil Android  

Le flux de travail suivant fonctionne pour la plupart des utilisateurs.  Pour obtenir de l’aide, consultez la rubrique [résolution des problèmes: devtools ne détecte pas la section appareil Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Ouvrez l’écran **options de développement** sur votre téléphone Android.  Pour plus d’informations, reportez-vous à [configurer les options pour les développeurs dans l’appareil][AndroidDeveloperStudioDevOptions].  
1.  Sélectionnez **activer le débogage USB**.  
1.  Sur votre ordinateur de développement, ouvrez Microsoft Edge.  
1.  Accédez à la `edge://inspect` page dans Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Page edge://inspect dans Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Figure1.  `edge://inspect`Page dans Microsoft Edge  
    :::image-end:::  
    
1.  Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.  Lorsque vous tentez de vous connecter pour la première fois, vous êtes généralement invité à DevTools détecter un appareil inconnu.  Autorisez l’invite d’autorisation de **débogage USB** sur votre appareil Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Invite autoriser le débogage USB sur un appareil Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Figure2.  Invite **autoriser le débogage USB** sur un appareil Android  
    :::image-end:::  
    
1.  Si vous voyez le nom de modèle de votre appareil Android, Microsoft Edge a correctement établi la connexion à votre appareil.  Passez à la section [étape 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### Résolution des problèmes: DevTools ne détecte pas l’appareil Android  

Les conseils suivants vous aideront à résoudre les problèmes liés à la configuration de votre matériel.  

*   Si vous utilisez un concentrateur USB, essayez de connecter votre appareil Android directement à votre ordinateur de développement.  
*   Essayez de débrancher le câble USB entre votre appareil et votre machine de développement Android, puis de reconnecter le câble USB.  Terminez la tâche lorsque les écrans de votre ordinateur Android et de développement sont déverrouillés.  
*   Assurez-vous que le câble USB fonctionne.  Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.  

Pour vérifier que votre logiciel est correctement configuré, suivez les conseils ci-dessous.  

*   Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB pour votre appareil Android.  Pour plus d’informations, voir [installer les pilotes USB du fabricant][AndroidDeveloperToolsOemUsb].  
*   Quelques combinaisons de périphériques Windows et Android (en particulier Samsung \) requièrent des paramètres supplémentaires.  Pour plus d’informations, consultez la section [devtools appareils ne détecte pas le périphérique en cas de branchement][Stackoverflow21925992].  

Pour résoudre les problèmes liés à l’invite de **débogage USB** sur votre appareil Android, suivez les conseils ci-dessous.  

*   En vous déconnectant puis en rouvrant le câble USB alors que DevTools est en focus sur votre ordinateur de développement et votre écran d’accueil Android s’affiche.  
    
    > [!NOTE]
    > L’invite risque de ne pas s’afficher si l’écran de votre appareil Android ou de développement est verrouillé.  

*   Mise à jour des paramètres d’affichage de votre appareil et de votre appareil Android de sorte qu’ils ne soient jamais en veille.  
*   Définir le mode USB pour Android sur la norme PTP.  Pour plus d’informations, reportez-vous à [la section Galaxy S4 ne pas afficher la boîte de dialogue autoriser le débogage USB][StackexchangeAndroid101933].  
*   Sélectionnez **révoquer les autorisations de débogage USB** à partir de l’écran Options pour les **développeurs** sur votre appareil Android pour rétablir l’état de votre choix.  

Si vous trouvez une solution qui n’est pas mentionnée sur cette page ou dans devtools appareils, la détection de l' [appareil n’est pas détectée lors][Stackoverflow21925992] du dépassement de capacité de la pile.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Étape 2: déboguer du contenu sur votre appareil Android à partir de votre ordinateur de développement  

1.  Ouvrez Microsoft Edge sur votre appareil Android.  
1.  À partir de la `edge://inspect` page, vous pouvez voir le nom du modèle de votre appareil Android, puis le numéro de série de l’appareil.  En dessous, vous devez voir la version de Microsoft Edge en cours d’exécution sur l’appareil, avec le numéro de version entre parenthèses.  Chaque onglet Microsoft Edge ouvert obtient une section unique.  Vous pouvez interagir avec cet onglet à partir d’une section.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un appareil distant connecté" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Figure3.  Un appareil distant connecté  
    :::image-end:::  
    
1.  Dans l' **onglet Ouvrir avec** la zone de texte URL, entrez une URL, puis sélectionnez **ouvrir**.  La page s’ouvre dans un nouvel onglet sur votre appareil Android.  
1.  Sélectionnez **inspecter** en regard de l’URL que vous venez d’ouvrir.  Une nouvelle instance de DevTools s’ouvre.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### Autres actions: mettre au point, recharger ou fermer un onglet  

Sélectionnez l' **onglet Focus**, **Reload**ou **Fermer** en regard de l’onglet que vous voulez mettre au point, recharger ou fermer.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Boutons de focalisation, de rechargement et de fermeture d’un onglet" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Figure4.  Boutons de focalisation, de rechargement et de fermeture d’un onglet  
:::image-end:::  

### Inspecter les éléments  

Accédez au panneau **éléments** de votre instance devtools, puis pointez sur un élément pour le mettre en surbrillance dans la fenêtre d’affichage de votre appareil Android.  

Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans le panneau **éléments** .  Sélectionnez **Select Element** ![ l’icône sélectionner un élément ][ImageSelectElementIcon] de votre instance devtools, puis sélectionnez l’élément sur l’écran de votre appareil Android.  

> [!NOTE]
> **Sélectionner l’élément** est désactivé après la première sélection; vous devez donc le réactiver chaque fois que vous souhaitez utiliser la fonctionnalité.  

### Capturez l’écran de votre téléphone Android sur votre ordinateur de développement.  

**Toggle Screencast** ![ ][ImageToggleScreencastIcon] Pour afficher le contenu de votre appareil Android dans votre instance devtools, sélectionnez l’icône d’activation/désactivation de la capture d’écran.  

Vous pouvez interagir avec la capture vidéo de l’une des manières suivantes.  

*   Les clics sont convertis en pressions et déclenchent les événements d’effleurement appropriés sur l’appareil.  
*   Les séquences de touches de votre ordinateur sont envoyées à l’appareil.  
*   Pour simuler un mouvement de pincement, maintenez la touche enfoncée `Shift` pendant que vous faites glisser.  
*   Pour faire défiler, utilisez votre pavé tactile ou votre volant de souris, ou glissement rapide avec le pointeur de la souris.

> [!NOTE]
> Pour plus d’informations, suivez les conseils ci-dessous.  
> 
> *   Les screencasts affichent uniquement le contenu de la page.  Les parties transparentes de l’enregistrement vidéo représentent des interfaces de périphériques, comme la barre d’adresses Microsoft Edge, la barre d’État Android ou le clavier Android.  
> *   Les screencasts ont un impact négatif sur les taux d’images.  Désactivez la capture d’images lors du mesurage des défilement ou des animations pour obtenir une image plus précise des performances de votre page.  
> *   Si l’écran de votre appareil Android est verrouillé, le contenu de votre screencast disparaît.  Déverrouillez l’écran de votre appareil Android pour la reprise automatique.  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurer les options pour les développeurs sur un appareil Développeur pour Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Outils de développement Web Safari | Développeur Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Débogage sur les appareils mobiles | Support Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB: échange d’une pile enthousiaste pour Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "DevToolsx XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
