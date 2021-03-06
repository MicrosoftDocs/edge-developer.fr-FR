---
description: Liste des API pris en charge à utiliser lors de la création d’extensions Microsoft Edge.
title: API prise en charge pour les extensions Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, extensions, api d’extension, développeur, développement web
ms.openlocfilehash: 20e924b5c973b9ecd433feeb3a772c6d17746369
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398104"
---
# <a name="supported-apis-for-microsoft-edge-extensions"></a>API prise en charge pour les extensions Microsoft Edge

Le tableau suivant fournit une liste des API que vous pouvez utiliser lors de la création d’extensions pour le navigateur Microsoft Edge \(Chromium\).

| API                                   | Description                                            
|---------------------------------------|----------------------------------------------------------|
| [alarmes](https://developer.chrome.com/extensions/alarms) | Planifier l’exécuter régulièrement ou à une heure spécifiée à l’avenir. |
| [favoris](https://developer.chrome.com/extensions/bookmarks) | Créer, organiser et manipuler des signets. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Utilisez les actions du navigateur pour placer des icônes dans la barre d’outils dans Microsoft Edge. Vous pouvez également utiliser des actions de navigateur pour ajouter une boîte à outils, un badge ou une fenêtre popup. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Supprimez les données de navigation du profil local d’un utilisateur. |
| [commandes](https://developer.chrome.com/extensions/commands) | Ajoutez des raccourcis clavier qui déclenchent des actions dans votre extension. Par exemple, une action pour ouvrir le navigateur ou envoyer une commande à l’extension. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | En règle générale, les paramètres de contenu vous permettent de personnaliser le comportement de Microsoft Edge sur chaque site, et non globalement. Modifier les paramètres qui contrôlent si les sites web peuvent utiliser des fonctionnalités telles que les cookies, JavaScript et les plug-ins. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Ajoutez des éléments au menu contexto dans Microsoft Edge. Les éléments de menu peuvent s’appliquer à différents objets, tels que des images, des liens hypertexte et des pages. |
| [cookies](https://developer.chrome.com/extensions/cookies) | Interroger et modifier les cookies, et recevoir des notifications lorsqu’ils changent. |
| [débogger](https://developer.chrome.com/extensions/debugger) | Attachez un ou plusieurs onglets pour instrumenter l’interaction réseau, déboguer JavaScript, modifier le DOM, modifier CSS, etc. Utilisez l’onglet Dubugger pour cibler les onglets avec sendCommand et routez les événements par tabId à partir des rappels onEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Prenez des mesures en fonction du contenu d’une page, sans avoir besoin d’autorisation pour lire le contenu de la page. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Fournit plus de confidentialité en bloquant ou en modifiant les demandes réseau en spécifiant des règles déclaratives. Autoriser les extensions à modifier les demandes réseau sans intercepter la demande et afficher le contenu. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Capturez le contenu d’un écran, de fenêtres individuelles ou d’onglets. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interagir avec la fenêtre inspectée.  Par exemple, obtenez l’ID d’onglet des pages, évaluez le code, actualisez les pages ou obtenez des ressources sur une page. |
| [devtools.network](https://developer.chrome.com/extensions/devtools_network) | Récupérez des informations sur les demandes réseau affichées par les outils de développement dans le panneau Réseau. |
| [devtools.panels](https://developer.chrome.com/extensions/devtools.panels) | Intégrez votre extension dans l’interface utilisateur de la fenêtre Outils de développement en créant vos propres panneaux, en accédant à des panneaux existants ou en ajoutant des barres latérales. |
| [téléchargements](https://developer.chrome.com/extensions/downloads) | Démarrez, surveillez, manipulez et recherchez des téléchargements par programme. |
| [enterprise.hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Obtenez le fabricant et le modèle de la plateforme matérielle sur laquelle le navigateur s’exécute. Cette API est disponible uniquement pour les extensions installées par la stratégie d’entreprise. |
| [événements](https://developer.chrome.com/extensions/events) | Types courants utilisés par les API qui lèvent des événements pour vous avertir lorsqu’un événement intéressant se produit. |
| [extension](https://developer.chrome.com/extensions/extension) | N’importe quelle page d’extension peut utiliser les utilitaires de cette API. Il inclut la prise en charge de l’échange de messages entre les extensions et les scripts de contenu, qui est décrit dans Message Passing. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Contient des déclarations de type pour les extensions Microsoft Edge. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Gérer les paramètres de police dans Microsoft Edge. |
| [historique](https://developer.chrome.com/extensions/history) | Interagir avec l’enregistrement des pages visitées du navigateur. Vous pouvez ajouter, supprimer ou interroger des URL dans l’historique du navigateur. Pour remplacer la page d’historique par votre propre version, accédez à Remplacer les pages. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implémentez l’internationalisation dans l’ensemble de votre application ou extension. |
| [idle](https://developer.chrome.com/extensions/idle) | Détecter les changements d’état d’inactivité de l’ordinateur. |
| [gestion](https://developer.chrome.com/extensions/management) | Gérer la liste des extensions installées ou en cours d’exécution. Il est utile pour les extensions qui remplacent la page Nouvel onglet intégrée. |
| [notifications](https://developer.chrome.com/extensions/notifications) | Créez des notifications enrichies à l’aide de modèles et affichez-les dans la bac système. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Enregistrez des mots clés dans la barre d’adresses Microsoft Edge, également appelée omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Ajoutez des icônes à la barre d’outils Microsoft Edge, à droite de la barre d’adresses. Les actions de page sont des actions qui peuvent être entreprises sur la page actuelle et qui ne sont pas applicables à toutes les pages. Les actions de page apparaissent grisées lorsqu’elles sont inactives. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Enregistrez les onglets en tant que fichiers MHTML.|
| [autorisations](https://developer.chrome.com/extensions/permissions) | Récupérer les autorisations déclarées et facultatives au moment de l’utilisation, plutôt qu’au moment de l’installation. Vous pouvez utiliser cette API pour afficher les autorisations nécessaires et approuvées pour vos utilisateurs. |
| [alimentation](https://developer.chrome.com/extensions/power) | Remplacez les fonctionnalités de gestion de l’alimentation du système. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Utilisez les événements pour interroger les imprimantes, leurs fonctionnalités et soumettre des tâches d’impression. |
| [confidentialité](https://developer.chrome.com/extensions/privacy) | Contrôlez les fonctionnalités de Microsoft Edge qui affectent la confidentialité d’un utilisateur. Cette API dépend du `EdgeSetting` prototype `types` d’obtenir et de définir la configuration de Microsoft Edge. |
| [proxy](https://developer.chrome.com/extensions/proxy) | Gérer les paramètres de proxy pour Microsoft Edge. Cette API dépend du prototype de l’API pour obtenir et définir `EdgeSetting` la configuration proxy de Microsoft `types` Edge. |
| [runtime](https://developer.chrome.com/extensions/runtime) | Récupérez la page d’arrière-plan, renvoyez des détails sur le manifeste, et écoutez et répondez aux événements dans le cycle de vie de l’application ou de l’extension. Vous pouvez également convertir le chemin d’accès relatif des URL en URL complètes. |
| [sessions](https://developer.chrome.com/extensions/sessions) | Interroger et restaurer des onglets et des fenêtres à partir d’une session de navigation. |
| [stockage](https://developer.chrome.com/extensions/storage) | Stockez, récupérez et suivez les modifications apportées aux données utilisateur. |
| [system.memory](https://developer.chrome.com/extensions/system_memory) | The `system.memory` API. |
| [system.storage](https://developer.chrome.com/extensions/system_storage) | Interrogez les informations sur les périphériques de stockage. Vous pouvez également recevoir des notifications lorsque des périphériques de stockage sont attachés ou détachés. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interagir avec les flux multimédias d’onglets. |
| [onglets](https://developer.chrome.com/extensions/tabs) | Interagir avec le système d’onglets du navigateur pour créer, modifier et réorganiser des onglets. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Accédez aux principaux sites, également appelés sites les plus visités, qui sont affichés sur la page nouvel onglet. Ces sites n’incluent pas de raccourcis personnalisés par l’utilisateur. |
| [tts](https://developer.chrome.com/extensions/tts) | Lire un texte synthétisé par synthèse vocale (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implémentez un moteur de reconnaissance vocale (TTS) à l’aide d’une extension. Les extensions qui s’inscrivent pour utiliser cette API reçoivent des événements qui contiennent des énoncés à prononcer et d’autres paramètres. Les extensions peuvent ensuite utiliser n’importe quelle technologie web disponible pour synthétiser et sortie vocale, et renvoyer des événements à la fonction d’appel pour signaler l’état. |
| [types](https://developer.chrome.com/extensions/types) | Déclarations de type pour Microsoft Edge. |
| [webNavigation](https://developer.chrome.com/extensions/webNavigation) | Recevoir des notifications sur l’état des demandes de navigation. |
| [webRequest](https://developer.chrome.com/extensions/webRequest) | Observez et analysez le trafic. Intercepter, bloquer ou modifier des demandes. |
| [windows](https://developer.chrome.com/extensions/windows) | Interagir avec les fenêtres du navigateur pour créer, modifier et réorganiser des fenêtres dans le navigateur. |



## <a name="unsupported-extension-apis"></a>API d’extension non pris en

Microsoft Edge ne prend pas en charge les API d’extension suivantes :

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` - En tant qu’alternative, vous pouvez utiliser pour récupérer un `launchWebAuthFlow` jeton OAuth2 pour authentifier les utilisateurs.
* `chrome.instanceID`.


## <a name="additional-considerations-for-supported-apis"></a>Considérations supplémentaires pour les API pris en charge

* L’utilisateur doit être inscrit à Microsoft Edge à l’aide d’un compte MSA ou Azure Active Directory à `chrome.identity.getProfileUserInfo` utiliser. Si l’utilisateur est connexion à Microsoft Edge à l’aide d’un compte Active Directory local, l’API renvoie les valeurs de courrier électronique et `null` d’ID.

* Microsoft Edge ne prend pas en charge les extensions qui utilisent les paiements du Chrome Web Store, car il utilise cette fonctionnalité pour demander des jetons pour les `identity.getAuthtoken` utilisateurs. Ces jetons sont envoyés à l’API de licence basée sur REST. 


<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/apps/external_extensions)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
