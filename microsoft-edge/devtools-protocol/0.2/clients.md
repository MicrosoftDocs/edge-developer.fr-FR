---
description: La version 0,2 du protocole Microsoft Edge DevTools prend en charge les clients d’outils suivants.
title: Clients de la version 0,2 du protocole Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 657d594b85c47cc1d5c80b8f2ac3ecc4bd4e4502
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565481"
---
# Clients de protocole DevTools

> [!NOTE]
> La version 0,2 du protocole Microsoft Edge DevTools fonctionne uniquement avec la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) et les versions ultérieures de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .  

**Devtools protocole 0,2** prend en charge les clients d’outils suivants.

[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Visual Studio code Visual](../media/visual-studio-code.png)](#visual-studio-code) Studio [ ![ 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)

## Microsoft Edge DevTools preview

Vous pouvez utiliser l’application Windows 10 [**devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) autonome à partir du Microsoft Store pour déboguer à distance un appareil hôte exécutant Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) ou version ultérieure).

La version 0,2 du protocole DevTools fournit de nouveaux domaines pour le débogage de style et de disposition, ainsi que les API de console, en plus de la fonctionnalité de débogage de script principal introduite dans la version 0,1. Dans l’interface utilisateur de DevTools Edge, cela se traduit par une fonctionnalité disponible dans les panneaux [**éléments**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) et [**débogueur**](../../devtools-guide/debugger.md) . Pour le moment, le débogage à distance Microsoft Edge est limité aux hôtes de bureau, avec la prise en charge d’autres appareils Windows 10 présents dans les versions ultérieures.

Voici comment configurer le débogage à distance à l’aide de l’application Microsoft Edge DevTools preview. La version 0,2 du protocole DevTools nécessite la [mise à jour de Windows 10 d’octobre 2018](/windows/uwp/whats-new/windows-10-build-17763) ou une version ultérieure de Windows Insider Preview sur l’ordinateur hôte (débogueur). L’application Edge DevTools Preview (utilisée sur la machine de débogueur) s’exécute sur Windows 10 version 16299 (Windows 10 automne Creators Update, 10/2017) ou version ultérieure.

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

## VisualStudioCode

Avec le [débogueur pour](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) l’extension de code Edge vs, vous pouvez déboguer l’exécution du script directement dans Microsoft Edge dans le code Visual Studio. L’extension nécessite que vous utilisiez votre application Web à partir de localhost, que vous puissiez commencer à partir de la ligne de commande ou d’une [tâche](https://code.visualstudio.com/docs/editor/tasks).

Pour commencer:

1. Installez le [débogueur pour](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) l’extension de code Edge vs.

2. Redémarrez le code, ouvrez le dossier contenant le projet pour lequel vous souhaitez déboguer et définir des points d’arrêt dans votre code.

3. Configurer une [tâche de lancement](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) d’localhost pour ouvrir la page souhaitée de votre projet: **Déboguer**  >  **Ajouter une configuration...**. Par exemple:

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    [*L’utilisation du débogueur*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) est plus approfondie sur les paramètres de configuration de lancement. 

4. Démarrez votre serveur sur localhost, puis appuyez sur le bouton **Démarrer le débogage** (lecture) ou `F5` lancer Microsoft Edge. Lorsque le point d’arrêt est atteint, vous êtes interrompu dans le code VS et vous pouvez examiner et parcourir le code à partir de cet emplacement.

Pour plus d’informations, consultez le [code vs Debugger pour la documentation Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .

## Microsoft Visual Studio

À l’aide de la version la plus récente de [**Visual Studio**](https://www.visualstudio.com) (Visual Studio 15,8 ou version ultérieure) qui s’exécute sur [Windows 10 octobre 2018](/windows/uwp/whats-new/windows-10-build-17763), vous pouvez lancer et déboguer Microsoft Edge à partir de l’IDE sur n’importe quel projet ASP.net ou .net principal.

Voici comment configurer le débogage Microsoft Edge avec Visual Studio:

1.  Installez et lancez la dernière version de [**Visual Studio**](https://www.visualstudio.com/) (visual studio 15,8 ou version ultérieure).

2. Ouvrez un projet ASP.NET ou .NET principal existant, ou **créez un nouveau projet...** à l’aide de l’un des modèles **Visual C#** .net.

3. Dans l' **Explorateur de solutions**du projet, ouvrez les fichiers JavaScript dont vous souhaitez déboguer et définir des points d’arrêt dans l’environnement de développement, comme vous le feriez avec du code côté serveur.

4. Appuyez sur `F5` pour lancer Microsoft Edge exécutant le serveur devtools. Lorsque le point d’arrêt est atteint, vous êtes interrompu dans Visual Studio, vous pouvez le consulter et parcourir le code à partir de cet emplacement.
