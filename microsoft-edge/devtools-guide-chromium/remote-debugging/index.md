---
title: Découvrir les appareils Android de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611818"
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




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# Découvrir les appareils Android de débogage à distance   



Déboguez à distance le contenu en direct sur un appareil Android à partir de votre ordinateur Windows ou macOS.  Ce didacticiel vous explique comment:  

*   Configurez votre appareil Android pour le débogage à distance et découvrez-le à partir de votre ordinateur de développement.  
*   Inspectez et déboguez le contenu en direct sur votre appareil Android à partir de votre ordinateur de développement.  
*   Contenu Screencast de votre appareil Android sur une instance DevTools sur votre ordinateur de développement.  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## Étape 1: découvrir votre appareil Android   

Le flux de travail suivant fonctionne pour la plupart des utilisateurs.  Pour plus d’informations, reportez-vous à [la rubrique résolution des problèmes: devtools ne détecte pas l’appareil Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Ouvrez l’écran **options de développement** sur votre téléphone Android.  Voir [configurer les options pour les développeurs sur un appareil](https://developer.android.com/studio/debug/dev-options.html).  
1.  Sélectionnez **activer le débogage USB**.  
1.  Sur votre ordinateur de développement, ouvrez Microsoft Edge.  
1.  [Ouvrez devtools][DevToolsOpen].  
1.  Dans devtools, sélectionnez le **menu principal** , `...` puis sélectionnez **plus d’outils**  >  **distants de périphériques distants**.  
    
    > ##### Figure1  
    > Ouverture de l’onglet **équipements distants** par le biais du **menu principal**  
    > ! [Ouverture de l’onglet équipements distants par le biais du menu principal] [ImageOpenRemoteDevices]  

1.  Dans DevTools, ouvrez l’onglet **paramètres** .  

1.  Vérifiez que la case **détecter les périphériques USB** est activée.  
    
    > ##### Figure 2  
    > La case **détecter les périphériques USB** est activée  
    > ! [La case détecter les périphériques USB est activée] [ImageDiscoverUSBDevices]  

1.  Connectez votre appareil Android directement à votre ordinateur de développement à l’aide d’un câble USB.  La première fois que vous effectuez cette opération, vous observez généralement que DevTools a détecté un appareil inconnu.  Si vous voyez un point vert et le texte **connecté** sous le nom de modèle de votre appareil Android, devtools a correctement établi la connexion à votre appareil.  Passez à l' [étape 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  Si votre appareil s’affiche comme **inconnu**, acceptez l’invite d’autorisation de **débogage USB** sur votre appareil Android.  

### Résolution des problèmes: DevTools ne détecte pas l’appareil Android   

Assurez-vous que votre matériel est correctement configuré:  

*   Si vous utilisez un concentrateur USB, essayez plutôt de connecter votre appareil Android directement à votre ordinateur de développement.  
*   Essayez de débrancher le câble USB de votre appareil et de votre ordinateur de développement Android, puis de le réactiver.  Faites-le pendant que vos écrans d’appareil Android et de développement sont déverrouillés.  
*   Assurez-vous que le câble USB fonctionne.  Vous devriez être en mesure d’inspecter les fichiers sur votre appareil Android à partir de votre ordinateur de développement.  

Assurez-vous que votre logiciel est correctement configuré:  

*   Si votre ordinateur de développement exécute Windows, essayez d’installer manuellement les pilotes USB pour votre appareil Android.  Voir [installer les pilotes USB OEM][AndroidUSBDrivers].  
    
*   Quelques combinaisons de périphériques Windows et Android (en particulier, Samsung) nécessitent une configuration supplémentaire.  Reportez-vous à la section [DevTools appareils ne détecte pas le périphérique connecté] [StackOverflowDevicesNotDetected].  
    
Si vous ne voyez pas l’invite **autoriser le débogage USB** sur votre appareil Android, procédez comme suit:  

*   En vous déconnectant puis en rouvrant le câble USB alors que DevTools est en focus sur votre ordinateur de développement et votre écran d’accueil Android s’affiche.  En d’autres termes, il est possible que l’invite ne s’affiche pas lorsque les écrans de votre ordinateur Android ou de développement sont verrouillés.
*   Mise à jour des paramètres d’affichage de votre appareil et de votre ordinateur de développement Android pour qu’ils ne soient jamais en veille.  
*   Définir le mode USB pour Android sur la norme PTP.  Reportez-vous à [la section Galaxy S4 ne pas afficher la boîte de dialogue autoriser le débogage USB][StackExchangeGalaxyS4DoesNotShowDialogBox].  
*   Sélectionnez **révoquer les autorisations de débogage USB** à partir de l’écran Options pour les **développeurs** sur votre appareil Android pour rétablir l’état de votre choix.  

Si vous trouvez une solution qui n’est pas mentionnée dans cette section ou dans [DevTools appareils ne détecte aucun appareil lorsque branché] [StackOverflowDevicesNotDetected] ou ajoutez une réponse à cette question de dépassement de pile<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Étape 2: déboguer du contenu sur votre appareil Android à partir de votre ordinateur de développement   

1.  Ouvrez Microsoft Edge sur votre appareil Android.  

1.  Dans l’onglet **équipements distants** , sélectionnez l’onglet qui correspond à votre nom de modèle d’appareil Android.  
    Dans la partie supérieure de cette page, vous pouvez voir le nom du modèle de votre appareil Android, puis son numéro de série.  En dessous, vous devez voir la version de Microsoft Edge en cours d’exécution sur l’appareil, avec le numéro de version entre parenthèses.  Chaque onglet Microsoft Edge ouvert dispose de sa propre section.  Vous pouvez interagir avec cet onglet à partir de cette section.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  Dans la zone de texte **nouvel onglet** , entrez une URL, puis sélectionnez **ouvrir**.  La page s’ouvre dans un nouvel onglet sur votre appareil Android.  

1.  Sélectionnez **inspecter** en regard de l’URL que vous venez d’ouvrir.  Une nouvelle instance de DevTools s’ouvre.  La version de Microsoft Edge qui s’exécute sur votre appareil Android détermine la version d’DevTools qui s’ouvre sur votre ordinateur de développement.  
    Par conséquent, si votre appareil Android exécute une vieille version de Microsoft Edge, l’instance DevTools peut s’avérer très différente de celle utilisée.  

### Autres actions: recharger, mettre au point ou fermer un onglet   

Sélectionnez **autres options** `...` en regard de l’onglet à recharger, mettre au point ou fermer.  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### Inspecter les éléments   

Accédez au panneau **éléments** de votre instance devtools, puis pointez sur un élément pour le mettre en surbrillance dans la fenêtre d’affichage de votre appareil Android.  

Vous pouvez également sélectionner un élément sur l’écran de votre appareil Android pour le sélectionner dans le panneau **éléments** .  Sélectionnez **Sélectionner** ![ l’élément sélectionner ][ImageSelectElementIcon] l’élément dans votre instance de devtools, puis sélectionnez l’élément sur l’écran de votre appareil Android.  

> [!NOTE]
> **Sélectionner l’élément** est désactivé après la première sélection; vous devez donc le réactiver chaque fois que vous souhaitez utiliser cette fonctionnalité.  

### Capturez l’écran de votre téléphone Android sur votre ordinateur de développement.   

Sélectionnez activer **/** désactiver ![ le bouton bascule capture ][ImageToggleScreencastIcon] d’écran pour afficher le contenu de votre appareil Android dans votre instance devtools.  

Vous pouvez interagir avec le screencast de plusieurs manières:  

*   Les clics sont convertis en pressions et déclenchent les événements d’effleurement appropriés sur l’appareil.  
*   Les séquences de touches de votre ordinateur sont envoyées à l’appareil.  
*   Pour simuler un mouvement de pincement, maintenez la touche enfoncée `Shift` pendant que vous faites glisser.  
*   Pour faire défiler, utilisez votre pavé tactile ou votre volant de souris, ou glissement rapide avec le pointeur de la souris.

Quelques remarques sur les screencasts:  

*   Les screencasts affichent uniquement le contenu de la page.  Les parties transparentes de l’enregistrement vidéo représentent des interfaces de périphériques, comme la barre d’adresses Microsoft Edge, la barre d’État Android ou le clavier Android.  
*   Les screencasts ont un impact négatif sur les taux d’images.  Désactivez la capture d’images lors du mesurage des défilement ou des animations pour obtenir une image plus précise des performances de votre page.  
*   Si l’écran de votre appareil Android est verrouillé, le contenu de votre screencast disparaît.  Déverrouillez l’écran de votre appareil Android pour la reprise automatique.  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-More-Tools-Remote-Devices.msft.png "figure 1: ouverture de l’onglet équipements distants par le biais du menu principal"  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.msft.png "figure 2: la case à cocher découvrir les appareils USB est activée"  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Installer les pilotes USB OEM | Développeurs Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 «les appareils devtools ne détectent pas l’appareil en cas de dépassement de la pile connectée»  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB: échange d’une pile enthousiaste pour Android"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
