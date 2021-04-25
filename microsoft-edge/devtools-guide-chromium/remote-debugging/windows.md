---
description: Mise en place du débogage à distance des appareils Windows 10
title: Mise en place du débogage à distance des appareils Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, remote, debugging, windows 10, windows, device portal
ms.openlocfilehash: e3f60f07ba96aaed8cd9d7348eee1b0a846faecf
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519245"
---
# <a name="get-started-with-remote-debugging-windows-10-devices"></a>Mise en place du débogage à distance des appareils Windows 10  

Déboguer à distance du contenu en direct sur un appareil Windows 10 à partir de votre ordinateur Windows ou macOS.  Ce didacticiel vous apprend les tâches suivantes.  

*   Configurer votre appareil Windows 10 pour le débogage à distance et vous y connecter à partir de votre ordinateur de développement.  
*   Inspectez et déboguer le contenu en direct sur votre appareil Windows 10 à partir de votre ordinateur de développement.  
*   Contenu de la capture vidéo de votre appareil Windows 10 sur une instance DevTools sur votre ordinateur de développement.  
    
## <a name="step-1-set-up-the-host-debuggee-machine"></a>Étape 1 : Configurer l'hôte (ordinateur débogage)  

L'ordinateur hôte ou debuggee est l'appareil Windows 10 que vous souhaitez déboguer.  Il peut s'agir d'un appareil distant difficile à accéder physiquement ou de ne pas avoir de périphériques de clavier et de souris, ce qui rend difficile l'interaction avec microsoft Edge DevTools sur cet appareil.  Pour configurer l'ordinateur hôte \(debuggee\), vous devez effectuer les actions suivantes.  

*   Installer et configurer [Microsoft Edge (Chromium)][MicrosoftEdgeMain]  
*   Installer les [outils à distance pour Microsoft Edge (bêta)][MicrosoftStoreApps9p6cmfv44zlt] à partir du [Microsoft Store][MicrosoftStoreAppsWindows]  
*   Activer [le mode développeur][WindowsAppsGetStartedEnableYourDeviceForDevelopment] et Activer Device [Portal][WindowsUwpDebugTestPerfDevicePortal]  
    
### <a name="install-and-configure-microsoft-edge-chromium"></a>Installer et configurer Microsoft Edge (Chromium)  

Si vous ne l'avez pas déjà fait, installez Microsoft Edge \(Chromium\) à partir [de cette page.][MicrosoftEdgeMain]  Si vous utilisez une version préinstallée de Microsoft Edge sur l'ordinateur hôte \(debuggee\), vérifiez que vous avez Microsoft Edge \(Chromium\) et non Microsoft Edge \(EdgeHTML\).  Un moyen rapide de vérifier est de charger dans le navigateur et de confirmer que le numéro `edge://settings/help` de version est 75 ou supérieur.  

Accédez maintenant `edge://flags` à Microsoft Edge \(Chromium\).  Dans **les indicateurs de recherche,** tapez Activer le **débogage à distance via Windows Device Portal.**  Définissez cet indicateur sur **Activé.**  Ensuite, sélectionnez le **bouton Redémarrer** pour redémarrer Microsoft Edge \(Chromium\).  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png" alt-text="Définition de l'indicateur Activer le débogage à distance via Windows Device Portal sur Activé" lightbox="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png":::
   Définition de **l'indicateur Activer le débogage à distance via Windows Device Portal** sur **Activé**  
:::image-end:::  

### <a name="install-the-remote-tools-for-microsoft-edge-beta"></a>Installer les outils à distance pour Microsoft Edge (bêta)  

Installez les [outils à distance pour Microsoft Edge (bêta)][MicrosoftStoreApps9p6cmfv44zlt] à partir du [Microsoft Store.][MicrosoftStoreAppsWindows]  

> [!NOTE]
> Le **bouton** Obtenir pour les outils à distance pour [Microsoft Edge (bêta)][MicrosoftStoreApps9p6cmfv44zlt] peut être désactivé si vous êtes sur Windows 10 version 1809 ou antérieure.  Pour configurer l'ordinateur hôte \(debuggee\), il doit être en cours d'exécution windows 10 version 1903 ou ultérieure.  Mettez à jour l'ordinateur hôte \(debuggee\) pour acquérir les outils distants pour [Microsoft Edge (bêta).][MicrosoftStoreApps9p6cmfv44zlt]  

:::image type="complex" source="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png" alt-text="Outils à distance pour Microsoft Edge \(Bêta\) dans le Microsoft Store" lightbox="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png":::
   Outils [à distance pour Microsoft Edge (bêta)][MicrosoftStoreApps9p6cmfv44zlt] dans le Microsoft [Store][MicrosoftStoreAppsWindows]  
:::image-end:::  

Lancez [les outils à distance pour Microsoft Edge (bêta)][MicrosoftStoreApps9p6cmfv44zlt] et, si vous y êtes invité, acceptez la boîte de dialogue autorisations dans l'application.  Vous pouvez maintenant fermer les outils à distance pour [Microsoft Edge (bêta)][MicrosoftStoreApps9p6cmfv44zlt] et vous n'avez pas besoin de l'ouvrir pour les futures sessions de débogage à distance.

### <a name="activate-developer-mode-and-enable-device-portal"></a>Activer le mode développeur et Activer Device Portal  

Si vous êtes sur un réseau WiFi, assurez-vous que le réseau est marqué comme domaine **ou** **privé.**  Vous pouvez vérifier l'état en ouvrant l'application Sécurité **Windows,** en choisissant pare-feu **** **& protection** du réseau et en vérifiant si votre réseau est répertorié en tant que réseau de domaine ou **réseau** privé.  

S'il est répertorié comme **Public,** accédez à **Paramètres**  >  **Réseau & Internet**  >  **Wi-Fi** **** , choisissez **** sur votre réseau et basculez le bouton de profil réseau sur Privé .  

À présent, ouvrez **l'application Paramètres.**  Dans **Rechercher un paramètre,** `Developer settings` entrez-le et choisissez-le.  Bascule sur le **mode développeur.**  Vous pouvez maintenant activer **Device Portal** en activer les diagnostics distants sur les connexions réseau **locales.** ****  Vous pouvez ensuite **** activer l'authentification pour que l'appareil client \(débogger\) fournisse les informations d'identification correctes pour se connecter à cet appareil.  

> [!NOTE]
> Si **activer les diagnostics distants sur les connexions réseau de la zone locale.** a été précédemment allumé, vous devez le désactiver et le désactiver à nouveau pour **que Device Portal** fonctionne avec les outils à distance pour Microsoft Edge [(bêta).][MicrosoftStoreApps9p6cmfv44zlt]  Si **une** section Pour les développeurs n'est pas affichée dans **Paramètres,** **Device Portal** peut déjà être allumé. Essayez donc de redémarrer l'appareil Windows 10 à la place.

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings.msft.png" alt-text="Application Paramètres avec le mode développeur et Device Portal configurés" lightbox="../media/remote-debugging-windows-media-host-settings.msft.png":::
   Application **Paramètres avec** **le mode développeur et** Device **Portal** configurés  
:::image-end:::  

Notez l'adresse IP de l'ordinateur et le port de connexion affichés sous **Se connecter à l'aide de :**  L'adresse IP dans l'image ci-dessous `192.168.86.78` est et le port de connexion est `50080` .  

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png" alt-text="Notez l'adresse IP et le port de connexion dans les paramètres" lightbox="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png":::
   Notez l'adresse IP et le port de connexion dans **les paramètres**  
:::image-end:::  

Vous entrez les informations sur l'appareil client \(débogger\) dans la [section suivante.](#step-2-set-up-the-client-debugger-machine)  Ouvrez les onglets dans Microsoft Edge et les applications [web progressives (PWA)][DevtoolsProgressiveWebApps] sur l'ordinateur hôte \(debuggee\) que vous souhaitez déboguer à partir de l'ordinateur client \(déboguer\).  

## <a name="step-2-set-up-the-client-debugger-machine"></a>Étape 2 : Configurer le client (ordinateur débogger)  

L'ordinateur client ou déboguer est l'appareil à partir de qui vous souhaitez déboguer.  Cet appareil peut être votre ordinateur de développement quotidien ou simplement votre PC ou votre MacBook lorsque vous travaillez à domicile.  

Pour configurer l'ordinateur client \(débogger\), installez Microsoft Edge \(Chromium\) à partir de cette [page][MicrosoftEdgeMain] si vous ne l'avez pas déjà fait.  Si vous utilisez une version préinstallée de Microsoft Edge sur l'ordinateur hôte \(debuggee\), vérifiez que vous avez Microsoft Edge \(Chromium\) et non Microsoft Edge \(EdgeHTML\).  Un moyen rapide de vérifier est de charger dans le navigateur et de confirmer que le numéro `edge://settings/help` de version est 75 ou supérieur.  

Accédez maintenant `edge://flags` à Microsoft Edge \(Chromium\).  Dans **les indicateurs de recherche,** tapez Activer le débogage **d'appareil Windows**distant dans edge://inspect .  Définissez cet indicateur sur **Activé.**  Ensuite, sélectionnez le **bouton Redémarrer** pour redémarrer Microsoft Edge \(Chromium\).  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png" alt-text="Définition de l'indicateur Activer le débogage d'appareil Windows à distance edge://inspect sur Activé" lightbox="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png":::
   Définition de **l'indicateur Activer le débogage d'appareil Windows à** distance edge://inspect sur **Activé**  
:::image-end:::  

Accédez maintenant à `edge://inspect` la page dans Microsoft Edge \(Chromium\).  Par défaut, vous devez être dans la section **Appareils.**  Sous Se connecter à un appareil **Windows**distant, entrez l'adresse IP et le port de connexion de l'ordinateur hôte \(debuggee\) dans la zone de texte suivant ce modèle : http:// `IP address` : `connection port` .  Maintenant, choisissez **Se connecter à l'appareil.**  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect.msft.png" alt-text="Page edge://inspect sur le client" lightbox="../media/remote-debugging-windows-media-edge-inspect.msft.png":::
   Page `edge://inspect` sur le client  
:::image-end:::  

Si vous définissez l'authentification pour l'ordinateur hôte \(debuggee\), vous êtes invité à entrer le nom d'utilisateur et le mot de passe de l'ordinateur client \(déboguer\) pour vous connecter correctement. **** ****  

### <a name="using-https-instead-of-http"></a>Utilisation de https au lieu de http  

Si vous souhaitez vous connecter à l'ordinateur hôte \(debuggee\) à l'aide de la place, vous devez accéder à Microsoft Edge sur l'ordinateur `https` `http` client `http://IP address:50080/config/rootcertificate` \(déboguer\).  Cela télécharge automatiquement un certificat de sécurité nommé `rootcertificate.cer` .

Choose `rootcertificate.cer` .  Cela ouvre [l'outil Gestionnaire de certificats Windows.][DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]

Choose **Install certificate...**, ensure that **Current User** is turned on, and choose **Next**.  Maintenant, choisissez **Placer tous les certificats dans le magasin suivant** et choisissez **Parcourir...**.  Choisissez le **magasin Autorités de certification racines de** confiance et choisissez **OK.**  Choose **Next** and then choose **Finish**.  Si vous y êtes invité, confirmez que vous souhaitez installer ce certificat dans le magasin Autorités de **certification racines de** confiance.

Maintenant, lorsque vous vous connectez à l'ordinateur hôte \(debuggee\) à partir de l'ordinateur client \(déboguer\) à l'aide de la page, vous devez utiliser une `edge://inspect` valeur `connection port` différente.  Par défaut, pour windows de bureau, Device Portal utilise `50080` comme `connection port` pour `http` .  For `https` , the Device Portal uses so follow this `50043` pattern: https:// : on the `IP address` `50043` `edge://inspect` page.  [En savoir plus sur les ports par défaut utilisés par Device Portal.][WindowsUwpDebugTestPerfDevicePortalSetup]  

> [!NOTE]
> Le port par défaut est le port par défaut, mais ce n'est pas toujours le cas, car Device Portal sur le bureau demande des ports dans la plage éphémère `http` `50080` `https` `50043` \(\>50 000\) pour éviter les collisions avec les revendications de port existantes sur l'appareil.  Pour en savoir plus, accédez à la section  [Paramètres de][WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal] port pour Device Portal sur le bureau Windows.  

## <a name="step-3-debug-content-on-the-host-from-the-client"></a>Étape 3 : Déboguer le contenu sur l'hôte à partir du client  

Si l'ordinateur client \(déboguer\) se connecte avec succès à l'ordinateur hôte \(debuggee\), la page du client affiche désormais la liste des onglets dans Microsoft Edge et les PLA ouverts sur `edge://inspect` l'hôte.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png" alt-text="La page edge://inspect sur le client affiche les onglets dans Microsoft Edge et les P PWA sur l'hôte" lightbox="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png":::
   La page du client affiche les onglets dans Microsoft Edge et les P `edge://inspect` PWA sur l'hôte  
:::image-end:::  

Déterminez le contenu que vous souhaitez déboguer et choisissez **d'inspecter.**  Microsoft Edge DevTools s'ouvre dans un nouvel onglet et capture vidéo du contenu de l'ordinateur hôte \(debuggee\) vers l'ordinateur client \(débogueur\).  Vous pouvez désormais utiliser toute la puissance de Microsoft Edge DevTools sur le client pour le contenu en cours d'exécution sur l'hôte.  En savoir plus sur l'utilisation de Microsoft Edge DevTools [ici.][DevtoolsIndex]  

:::image type="complex" source="../media/remote-debugging-windows-media-devtools-client.msft.png" alt-text="Microsoft Edge DevTools sur le client débogage d'un onglet dans Microsoft Edge sur l'hôte" lightbox="../media/remote-debugging-windows-media-devtools-client.msft.png":::
   Microsoft [Edge DevTools sur][DevtoolsIndex] le client débogage d'un onglet dans Microsoft Edge sur l'hôte  
:::image-end:::  

### <a name="inspect-elements"></a>Inspecter les éléments  

Par exemple, essayez d'inspecter un élément.  Accédez à l'outil **Elements** de votre instance DevTools sur le client, puis pointez sur un élément pour le surligner dans laport d'affichage de l'appareil hôte.  

Vous pouvez également appuyer sur un élément sur l'écran de votre appareil hôte pour le choisir dans **l'outil Éléments.**  Choisissez **Select Element** sur votre instance DevTools sur le client, puis appuyez sur l'élément sur l'écran de votre appareil hôte.  

> [!NOTE]
> **Select Element** est désactivé après la première fonction tactile. Vous devez donc l'activer à nouveau chaque fois que vous souhaitez utiliser cette fonctionnalité.  

> [!IMPORTANT]
> Le **volet Écouteurs** d'événements de **l'outil Éléments** est vide sur Windows 10 version 1903.  Il s'agit d'un problème **** connu et l'équipe prévoit de résoudre le volet Écouteurs d'événements dans une mise à jour de maintenance vers Windows 10 version 1903.  

## <a name="step-4-screencast-your-host-screen-to-your-client-device"></a>Étape 4 : Capture d'écran de votre écran hôte sur votre appareil client  

Par défaut, la capture vidéo est désactivée pour l'instance DevTools sur le client, ce qui vous permet d'afficher le contenu sur l'appareil hôte dans votre instance DevTools sur votre appareil client.  Sélectionnez **Activer/désactiver la capture vidéo pour** désactiver ou activer cette fonctionnalité.  

:::image type="complex" source="../media/remote-debugging-windows-media-toggle-screencast.msft.png" alt-text="Bouton Bascule de la capture vidéo dans Microsoft Edge DevTools sur le client" lightbox="../media/remote-debugging-windows-media-toggle-screencast.msft.png":::
   Bouton **Bascule de la capture vidéo** dans Microsoft Edge DevTools sur le client  
:::image-end:::  

Vous pouvez interagir avec la capture vidéo de plusieurs manières :  
*   Les choix sont convertis en pressions, ce qui permet de tirer les événements tactiles appropriés sur l'appareil.  
*   Les frappes de touches sur votre ordinateur sont envoyées à l'appareil.  
*   Pour simuler un mouvement de pincement, maintenez le doigt `Shift` en cours de glissement.  
*   Pour faire défiler la souris, utilisez votre trackpad ou votre roulette de souris, ou fling avec votre pointeur de souris.  

Quelques remarques sur les captures vidéo :  
*   Les captures d'écran affichent uniquement le contenu de la page.  Les parties transparentes de la capture vidéo représentent des interfaces d'appareil, telles que la barre d'adresses Microsoft Edge, la barre des tâches Windows 10 ou le clavier Windows 10.  
*   Les captures vidéo affectent négativement les taux d'images.  Désactivez la capture vidéo lors de la mesure des défilements ou des animations pour obtenir une image plus précise des performances de votre page.  
*   Si l'écran de votre appareil hôte se verrouille, le contenu de votre capture vidéo disparaît.  Déverrouillez l'écran de votre appareil hôte pour reprendre automatiquement la capture vidéo.  

## <a name="known-issues"></a>Problèmes connus  

Le **volet Écouteurs** d'événements de l'outil **Éléments** est vide sur Windows 10 version 1903.  L'équipe prévoit de corriger le volet **Écouteurs** d'événements dans une mise à jour de maintenance vers Windows 10 version 1903.  

Le **volet Cookies** du panneau **Application** est vide sur Windows 10 version 1903.  L'équipe prévoit de corriger le volet **Cookies** dans une mise à jour de service vers Windows 10 version 1903.  

**L'outil Audits,** l'outil Affichage **3D,** la section **** **Appareils** émulés dans **Paramètres**et le volet d'arborescence Accessibilité de l'outil **Éléments** ne fonctionnent pas comme prévu.  L'équipe prévoit de corriger les outils répertoriés dans une prochaine mise à jour de Microsoft Edge.  

L'Explorateur de fichiers ne se lance pas à partir **** de DevTools dans l'outil **Sources** ou dans le panneau de sécurité lorsque vous déboguer à distance.  L'équipe prévoit de corriger les outils dans une prochaine mise à jour de Microsoft Edge.  

<!-- links -->

[DevtoolsIndex]: ../index.md "Vue d’ensemble des outils de développement Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Déboguer les applications web progressives | Documents Microsoft"  

[DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]: /dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool "Afficher les certificats à l'aide de l'outil Gestionnaire de certificats : comment : afficher les certificats à l'aide du logiciel en | Documents Microsoft"  

[WindowsAppsGetStartedEnableYourDeviceForDevelopment]: /windows/apps/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d'ensemble de Windows Device Portal | Documents Microsoft"  
[WindowsUwpDebugTestPerfDevicePortalSetup]: /windows/uwp/debug-test-perf/device-portal#setup "Programme d'installation : vue d'ensemble de Windows Device Portal | Documents Microsoft"  
[WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal]: /windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal "Configuration basée sur le Registre pour Device Portal - Device Portal pour Windows Desktop | Documents Microsoft"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[MicrosoftStoreApps9p6cmfv44zlt]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils à distance pour microsoft Edge (bêta) | Microsoft Store"  
