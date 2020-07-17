---
description: La version 0,1 du protocole Microsoft Edge DevTools prend en charge les clients d’outils suivants.
title: Clients de la version 0,1 du protocole DevTools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 5fdf375634bb63c944b3fe09d1c0cbd5a935dcd7
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882764"
---
# Clients de la version 0,1 du protocole DevTools (EdgeHTML)  

> [!NOTE]
> Le protocole Microsoft Edge DevTools fonctionne uniquement sur les [mises à jour de Windows 10 d’avril 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

**Devtools protocole 0,1** prend en charge les clients d’outils suivants.

[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Microsoft Visual Studio 15,7 Preview 2](../media/visual-studio-2017.png)](#microsoft-visual-studio-preview)

## Aperçu de DevTools Microsoft Edge

Vous pouvez utiliser l’application Windows 10 [**devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome à partir du Microsoft Store pour déboguer à distance un appareil hôte exécutant Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) ou version ultérieure).

La version 0,1 de la version préliminaire du protocole DevTools fournit une fonctionnalité de débogage de base, comme la définition de points d’arrêt, l’exécution du code et l’exploration de traces de pile. Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans le volet [**débogueur**](../../devtools-guide/debugger.md) , l’inspection du cache (pour le stockage Web, le travailleur de service, l’API de cache et IndexedDB). Pour le moment, le débogage à distance Microsoft Edge est limité aux hôtes de bureau, avec la prise en charge d’autres appareils Windows 10 présents dans les versions ultérieures.

Voici comment configurer le débogage à distance à l’aide de l’application Microsoft Edge DevTools preview. Le protocole DevTools est dans Preview et nécessite [Windows 10 avril 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou une version ultérieure de Windows Insider Preview sur l’ordinateur hôte (débogueur). L’application Edge DevTools Preview (utilisée sur la machine de débogueur) sera exécutée sur les versions de l’automne Creators Update (version 1709) et de Windows Insider preview.

**Sur l’ordinateur hôte (débogueur)...**

1. Si vous utilisez un réseau WiFi, assurez-vous que le réseau est marqué comme **domaine** ou **privé**. Pour ce faire, ouvrez l’application [**Centre de sécurité Windows Defender**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , cliquez sur **pare-feu & protection du réseau** et vérifiez si votre réseau figure en tant que réseau de *domaine* ou *réseau privé*. 

    S’il est répertorié comme étant *public*, accédez à **réglages**  >  **Network & Internet**  >  **Wi-Fi**, cliquez sur votre réseau et activez le bouton *Network Network (réseau* **privé**).

2. Ouvrez le panneau **de configuration pour les développeurs** dans les *paramètres* Windows (recherchez *développeur* et cliquez sur utiliser les *fonctionnalités de développement*) et: 

    a. Activez le **mode développeur**. Le package *mode développeur* s’installe, ce qui permet d’activer les outils de contrôle à distance pour le bureau.

    b. Activez [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*activez les diagnostics à distance sur connexions au réseau local*) et la **découverte d’appareils** (*rendez votre appareil visible pour les connexions USB et votre réseau local*).

    c. Activez **l’authentification** et attribuez un nom d’utilisateur/mot de passe.

    d. Notez l’adresse IP et le port de connexion de l’ordinateur (50443) affichés.

3. Ouvrez les onglets dans Microsoft Edge que vous souhaitez déboguer de l’ordinateur client.

**Sur l’ordinateur client (débogueur)...**

1.  Installez et lancez l’application [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome à partir du Microsoft Store.

2. Ouvrez le panneau **distant** et entrez l’emplacement réseau (URL et port) de l’ordinateur hôte, puis cliquez sur **se connecter**.

3. **Installez** le certificat de l’ordinateur hôte à partir de la boîte de dialogue *certificat non approuvé* qui s’affiche.

4. Fournissez le nom d’utilisateur/mot de passe que vous avez désigné pour l’authentification Device Portal.

5. Le panneau *distant* charge une liste de cibles de pages débogageées sur l’ordinateur hôte. Sélectionnez-en un pour démarrer le débogage.

6. Utilisez le bouton **Actualiser** pour mettre à jour et rechargez la liste des cibles de pages distantes sur l’ordinateur hôte. Cliquez sur le bouton **déconnecter** pour revenir à l’écran *se connecter à un appareil distant* et le joindre à un autre hôte.

## Microsoft Visual Studio preview

À l’aide de la version la plus récente de [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual studio 15,7 Preview 1 ou version ultérieure), vous pouvez lancer et déboguer Microsoft Edge à partir de l’environnement de développement intégré (IDE) sur n’importe quel projet ASP.net ou .net principal. Le protocole DevTools est actuellement en version préliminaire et nécessite l’exécution d’une build [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

Voici comment configurer le débogage Microsoft Edge avec Visual Studio:

1.  Installez et lancez la dernière version de [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual studio 15,7 Preview 1 ou version ultérieure).

2. Ouvrez un projet ASP.NET ou .NET principal existant, ou **créez un nouveau projet...** à l’aide de l’un des modèles **Visual C#** .net.

3. Dans l' **Explorateur de solutions**du projet, ouvrez les fichiers JavaScript dont vous souhaitez déboguer et définir des points d’arrêt dans l’environnement de développement, comme vous le feriez avec du code côté serveur.

4. Appuyez sur `F5` pour lancer Microsoft Edge exécutant le serveur devtools. Lorsque le point d’arrêt est atteint, vous êtes interrompu dans Visual Studio, vous pouvez le consulter et parcourir le code à partir de cet emplacement.
