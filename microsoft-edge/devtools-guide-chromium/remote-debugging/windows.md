---
title: Prendre en main les appareils Windows 10 de débogage à distance
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, distant, débogage, Windows 10, Windows, Device Portal
ms.openlocfilehash: b944e1f16d4c26f4db83e3eb131f1da8ea938c97
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565629"
---
# Prendre en main les appareils Windows 10 de débogage à distance  

Déboguez à distance le contenu en direct sur un appareil Windows 10 à partir de votre ordinateur Windows ou macOS.  Ce didacticiel vous explique comment:  

*   Configurez votre appareil Windows 10 pour le débogage à distance et connectez-vous à partir de votre ordinateur de développement.  
*   Inspectez et déboguez le contenu en direct sur votre appareil Windows 10 à partir de votre ordinateur de développement.  
*   Contenu Screencast de votre appareil Windows 10 sur une instance DevTools sur votre ordinateur de développement.  

## Étape 1: configurer l’hôte (machine déboguée)  

L’ordinateur hôte ou débogué est l’appareil Windows 10 que vous voulez déboguer.  Il peut s’agir d’un périphérique distant qui vous permet d’accéder physiquement ou de ne pas disposer de périphériques de clavier et de souris, ce qui complique l’interaction avec Microsoft Edge DevTools sur cet appareil.  Pour configurer l’ordinateur hôte (débogueur), vous devez effectuer les opérations suivantes:  

*   Installer et configurer [Microsoft Edge (chrome)](https://www.microsoft.com/edge)  
*   Installer les [outils de contrôle à distance pour Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) à partir du [Microsoft Store](https://www.microsoft.com/store/apps/windows)  
*   Activez le [mode développeur](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development) et activez [Device Portal](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal) .  

### Installer et configurer Microsoft Edge (chrome)  

Si ce n’est déjà fait, installez Microsoft Edge (chrome) à partir de [cette page](https://www.microsoft.com/edge).  Si vous utilisez une version préinstallée de Microsoft Edge sur l’ordinateur hôte (débogué), vérifiez que vous disposez de Microsoft Edge (chrome) et non de Microsoft Edge (EdgeHTML).  Une méthode rapide pour vérifier est de charger `edge://settings/help` dans le navigateur et de vérifier que le numéro de version est 75 ou version ultérieure.  

Vous pouvez désormais accéder à `edge://flags` dans Microsoft Edge (chrome).  Dans **indicateurs de recherche**, tapez **activer le débogage à distance à l’aide de Windows Device Portal**.  Activez **l’option indicateur.**  Cliquez ensuite sur le bouton **redémarrer** pour redémarrer Microsoft Edge (chrome).  

> ##### Figure1  
> Définition de l’option **activer le débogage à distance via Windows Device Portal** sur **activée**  
> ![Définition de l’option Activer le débogage à distance via Windows Device Portal sur activée](./windows-media/edge-flags-on-host.png)  

### Installer les outils de contrôle à distance de Microsoft Edge (Beta)  

Installez les [outils de contrôle à distance pour Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) à partir du [Microsoft Store](https://www.microsoft.com/store/apps/windows).  

> [!NOTE]
> Le bouton **obtenir** pour les [outils de contrôle à distance de Microsoft Edge (bêta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) est susceptible d’être désactivé si vous utilisez Windows 10 version 1809 ou une version antérieure.  Pour configurer l’ordinateur hôte (débogueur), il doit exécuter Windows 10 version 1903 ou une version ultérieure.  Mettez à jour l’ordinateur hôte (débogué) pour acquérir les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT).  

> ##### Figure 2  
> [Outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) dans la [Boutique Microsoft](https://www.microsoft.com/store/apps/windows)  
> ![Outils de contrôle à distance de Microsoft Edge (Beta) dans la boutique Microsoft](./windows-media/remote-tools-in-store.png)  

Lancez les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) et, si vous y êtes invité, acceptez la boîte de dialogue autorisations dans l’application. Vous pouvez maintenant fermer les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) et vous n’avez pas besoin de l’ouvrir pour les futures sessions de débogage à distance.

### Activez le mode développeur et activez Device Portal.  

Si vous utilisez un réseau WiFi, assurez-vous que le réseau est marqué comme **domaine** ou **privé**.  Pour ce faire, ouvrez l’application de **sécurité Windows** , cliquez sur **pare-feu & protection du réseau** et vérifiez si votre réseau figure en tant que réseau de **domaine** ou réseau **privé** .  

S’il est répertorié comme étant **public**, accédez **à paramètres**  >  **réseau & Internet**  >  **Wi-Fi**, cliquez sur votre réseau et basculez le bouton de **profil réseau** sur **privé**.  

À présent, ouvrez l’application **paramètres** .  Dans **Rechercher un paramètre**, entrez les **paramètres du développeur** et sélectionnez-le.  Activez le **mode développeur**.  Vous pouvez désormais activer **Device Portal** en définissant **activer les diagnostics à distance sur connexions au réseau local** **.**  Si vous le souhaitez, vous pouvez activer ou désactiver l' **authentification** de manière à ce que l’appareil du client (débogueur) doit fournir les informations d’identification appropriées pour vous connecter à cet appareil.  

> [!NOTE]
> Si vous **activez les diagnostics distants sur les connexions au réseau local.** a été activé, vous devez le désactiver et le réactiver pour **Device Portal** pour fonctionner avec les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT). Si vous ne voyez pas la section **pour les développeurs dans les** **paramètres**, **Device Portal** est déjà activé, essayez de redémarrer l’appareil Windows 10.

> ##### Figure3  
> Application **paramètres** avec le **mode développeur** et **Device Portal** configurés  
> ![Application paramètres avec le mode développeur et Device Portal configurés](./windows-media/host-settings.png)  

Notez l’adresse IP et le port de connexion de l’ordinateur affiché sous **se connecter à l’aide de:**.  Dans l’image ci-dessous, l’adresse IP correspond au `192.168.86.78` port de connexion `50080` .  

> ##### Figure 4  
> Notez l’adresse IP et le port de connexion dans les **paramètres** .  
> ![Notez l’adresse IP et le port de connexion dans les paramètres.](./windows-media/host-settings-ip-address.png)  

Vous devez entrer ces informations dans la [section suivante](#step-2-set-up-the-client-debugger-machine)de l’appareil client (débogueur).  Ouvrez les onglets dans Microsoft Edge et les [applications Web progressives (PWAS)](../progressive-web-apps.md) sur l’ordinateur hôte (débogueur) que vous souhaitez déboguer de l’ordinateur client (débogueur).  

## Étape 2: configurer le client (machine de débogueur)  

Le client ou le débogueur est l’appareil à partir duquel vous voulez procéder au débogage.  Il est possible qu’il s’agit de votre ordinateur de développement quotidien ou qu’il s’agissait de votre PC ou MacBook lorsque vous travaillez chez vous.  

Pour configurer l’ordinateur client (débogueur), installez Microsoft Edge (chrome) à partir de [cette page](https://www.microsoft.com/edge) si vous ne l’avez pas déjà fait.  Si vous utilisez une version préinstallée de Microsoft Edge sur l’ordinateur hôte (débogué), vérifiez que vous disposez de Microsoft Edge (chrome) et non de Microsoft Edge (EdgeHTML).  Une méthode rapide pour vérifier est de charger `edge://settings/help` dans le navigateur et de vérifier que le numéro de version est 75 ou version ultérieure.  

Vous pouvez désormais accéder à `edge://flags` dans Microsoft Edge (chrome).  Dans **indicateurs de recherche**, tapez **activer le débogage de périphériques Windows distants dans Edge://Inspect**.  Activez **l’option indicateur.**  Cliquez ensuite sur le bouton **redémarrer** pour redémarrer Microsoft Edge (chrome).  

> ##### Figure 5  
> Définir le **débogage de l’appareil Windows distant via Edge://Inspect** Flag sur **activé**  
> ![Définir le débogage de l’appareil Windows distant via edge://inspect Flag sur activé](./windows-media/edge-flags-on-client.png)  

Accédez à la `edge://inspect` page dans Microsoft Edge (chrome).  Par défaut, vous devez vous trouver dans la section **périphériques** .  Sous **se connecter à un appareil Windows distant**, entrez l’adresse IP et le port de connexion de l’ordinateur hôte (débogueur) dans le champ TextBox suivant ce modèle: http:// `IP address` : `connection port` .  Cliquez à présent sur **connexion au périphérique**.  

> ##### Figure 6  
> `edge://inspect`Page sur le client  
> ![Page edge://inspect sur le client](./windows-media/edge-inspect.png)  

Si vous configurez l’authentification pour l’ordinateur hôte (débogueur), vous serez invité à entrer le **nom d’utilisateur** et le **mot de passe** pour que l’ordinateur client (débogueur) se connecte correctement.  

### Utiliser HTTPS au lieu de http  

Si vous voulez vous connecter à l’ordinateur hôte (débogueur) à l’aide de la fonction à la `https` place `http` , vous devez Navgiate à `http://IP address:50080/config/rootcertificate` Microsoft Edge sur l’ordinateur client (débogueur). Le certificat de sécurité intitulé sera automatiquement téléchargé `rootcertificate.cer` .

Cliquez sur activer `rootcertificate.cer` . L' [outil Gestionnaire de certificats Windows](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool)s’ouvre.

Cliquez sur **installer le certificat...**, assurez-vous que l' **utilisateur actuel** est sélectionné, puis cliquez sur **suivant**. Sélectionnez **Placer tous les certificats dans le magasin suivant** , puis cliquez sur **Parcourir...**. Sélectionnez le magasin **autorités de certification racines de confiance** , puis cliquez sur **OK**. Cliquez sur **Suivant**, puis sur **Terminer**. Si vous y êtes invité, confirmez que vous voulez installer ce certificat sur le magasin des **autorités de certification racines de confiance** .

À présent, lors de la connexion à l’ordinateur hôte (débogueur) à partir de l’ordinateur client (débogueur) à l’aide de la `edge://inspect` page, vous devez utiliser une `connection port` valeur différente.  Par défaut, pour les fenêtres de bureau, Device Portal est utilisé `50080` comme `connection port` pour `http` .  Pour cela `https` , Device Portal utilise `50043` alors ce modèle: https:// `IP address` : `50043` sur la `edge://inspect` page.  [En savoir plus sur les ports par défaut utilisés par Device Portal](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal#setup).  

> [!NOTE]
> Le port par défaut de `http` is `50080` et le port par défaut pour `https` est, `50043` mais ce n’est pas toujours le cas car Device Portal sur le bureau revendique des ports dans la plage éphémère (>50 000) pour éviter les collisions avec les déclarations de port existant sur l’appareil.  Pour plus d’informations, consultez la section [paramètres de port](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal) pour Device Portal sur le bureau Windows.  

## Étape 3: déboguer du contenu sur l’hôte à partir du client  

Si l’ordinateur client (débogueur) se connecte à l’ordinateur hôte (débogueur), la `edge://inspect` page sur le client affiche désormais une liste des onglets dans Microsoft Edge et toute PWAS ouverte sur l’hôte.  

> ##### Figure 7  
> La `edge://inspect` page sur le client affiche les onglets dans Microsoft Edge et PWAS sur l’hôte  
> ![La page edge://inspect sur le client affiche les onglets dans Microsoft Edge et PWAs sur l’hôte.](./windows-media/edge-inspect-connected.png)  

Déterminez le contenu que vous voulez déboguer, puis cliquez sur **inspecter**.  Le DevTools de Microsoft Edge s’ouvre dans un nouvel onglet, puis capturez le contenu de l’ordinateur hôte (débogueur) sur l’ordinateur client (débogueur).  Vous pouvez maintenant utiliser toute la puissance de Microsoft Edge DevTools sur le client pour le contenu exécuté sur l’hôte.  Apprenez-en davantage sur l’utilisation de Microsoft Edge DevTools [ici](../../devtools-guide-chromium.md).  

> ##### Figure8  
> Le client [Microsoft Edge devtools](../../devtools-guide-chromium.md) sur le client déboguant un onglet dans Microsoft Edge sur l’hôte  
> ![Le client Microsoft Edge DevTools sur le client déboguant un onglet dans Microsoft Edge sur l’hôte](./windows-media/devtools-client.png)  

### Inspecter les éléments  

Par exemple, essayez d’inspecter un élément.  Accédez au panneau **éléments** de votre instance devtools sur le client, puis pointez sur un élément pour le mettre en surbrillance dans la fenêtre d’affichage de l’appareil hôte.  

Vous pouvez également appuyer sur un élément de l’écran de votre appareil hôte pour le sélectionner dans le panneau **éléments** .  Cliquez sur **Sélectionner un élément** sur votre instance devtools sur le client, puis sur l’élément de l’écran de votre appareil hôte.  Notez que l' **élément sélectionner** est désactivé après la première interaction, donc vous devez le réactiver chaque fois que vous voulez utiliser cette fonctionnalité.  

> [!IMPORTANT]
> Le volet **détecteurs d’événements** du panneau **éléments** est vide dans la version 1903 de Windows 10.  Il s’agit d’un problème connu qui permettra d’ajuster le volet des **écouteurs d’événements** dans une mise à jour de maintenance de Windows 10 version 1903.  

## Étape 4: Capturez l’écran de votre hôte sur votre appareil client.  

Par défaut, l’option de capture d’écran est activée par défaut sur le client, ce qui vous permet d’afficher le contenu sur l’appareil hôte dans votre instance DevTools sur votre appareil client.  Cliquez sur **activer/désactiver** le mode vidéo pour désactiver ou activer cette fonction.  

> ##### Figure9  
> Bouton **activer/désactiver** l’enregistrement dans Microsoft Edge devtools sur le client  
> ![Bouton Activer/désactiver l’enregistrement dans Microsoft Edge DevTools sur le client](./windows-media/toggle-screencast.png)  

Vous pouvez interagir avec le screencast de plusieurs manières:  
*   Les clics sont convertis en pressions et déclenchent les événements d’effleurement appropriés sur l’appareil.  
*   Les séquences de touches de votre ordinateur sont envoyées à l’appareil.  
*   Pour simuler un mouvement de pincement, maintenez la touche enfoncée `Shift` pendant que vous faites glisser.  
*   Pour faire défiler, utilisez votre pavé tactile ou votre volant de souris, ou glissement rapide avec le pointeur de la souris.  

Quelques remarques sur les screencasts:  
*   Les screencasts affichent uniquement le contenu de la page.  Les parties transparentes de l’enregistrement vidéo représentent des interfaces de périphériques, comme la barre d’adresses Microsoft Edge, la barre des tâches Windows 10 ou le clavier Windows 10.  
*   Les screencasts ont un impact négatif sur les taux d’images.  Désactivez la capture d’images lors du mesurage des défilement ou des animations pour obtenir une image plus précise des performances de votre page.  
*   Si l’écran de votre appareil hôte est verrouillé, le contenu de votre screencast disparaît.  Déverrouillez l’écran de votre appareil hôte pour la reprise automatique.  

## Problèmes connus  

Le volet **détecteurs d’événements** du panneau **éléments** est vide dans la version 1903 de Windows 10.  Nous allons résoudre le problème du volet **écouteurs d’événements** dans une mise à jour de maintenance vers Windows 10 version 1903.  

Le volet **cookies** du panneau **application** est vide dans la version 1903 de Windows 10.  Nous allons résoudre le problème dans le volet **cookies** d’une mise à jour de maintenance de Windows 10 version 1903.  

Le volet **audits** , le panneau de **vue 3D** , la section **appareils émulés** dans les **paramètres**et le volet **arborescence d’accessibilité** dans le panneau **éléments** ne fonctionnent pas comme prévu.  Nous allons résoudre ces outils dans une prochaine mise à jour de Microsoft Edge.  

L’Explorateur de fichiers ne se lance pas à partir du DevTools dans le panneau **sources** ou du panneau de **sécurité** lors du débogage à distance.  Nous allons résoudre ces outils dans une prochaine mise à jour de Microsoft Edge.  
