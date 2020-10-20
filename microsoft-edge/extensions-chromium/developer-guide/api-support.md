---
description: Liste des API prises en charge à utiliser lors de la création d’extensions Microsoft Edge.
title: API prises en charge pour les extensions Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, extensions, API d’extension, développeur, développement Web
ms.openlocfilehash: 868473393da6cefbf146fb7acd6c9816903bd253
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120390"
---
# API prises en charge pour les extensions Microsoft Edge

Le tableau suivant répertorie les API que vous pouvez utiliser lors de la création d’extensions pour le navigateur Microsoft Edge.

| API                                   | Description                                            
|---------------------------------------|----------------------------------------------------------|
| [alarmes](https://developer.chrome.com/extensions/alarms) | Planifiez le code pour qu’il s’exécute régulièrement ou à une heure précise. |
| [favoris](https://developer.chrome.com/extensions/bookmarks) | Créer, organiser et manipuler des signets. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Utilisez les actions du navigateur pour placer des icônes dans la barre d’outils dans Microsoft Edge. Vous pouvez également utiliser les actions du navigateur pour ajouter une info-bulle, un badge ou une fenêtre contextuelle. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Supprimer les données de navigation du profil local d’un utilisateur. |
| [commandes](https://developer.chrome.com/extensions/commands) | Ajoutez des raccourcis clavier déclenchant des actions dans votre extension. Par exemple, une action permettant d’ouvrir le navigateur ou d’envoyer une commande à l’extension. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | En général, les paramètres de contenu vous permettent de personnaliser le comportement de Microsoft Edge sur chaque site plutôt que globalement. Modifiez les paramètres qui contrôlent l’utilisation des fonctionnalités telles que les cookies, JavaScript et les plug-ins. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Ajouter des éléments au menu contextuel dans Microsoft Edge. Les éléments de menu s’appliquent à différents objets, tels que des images, des liens hypertexte et des pages. |
| [les](https://developer.chrome.com/extensions/cookies) | Recherchez et modifiez des cookies, et recevez des notifications lorsqu’ils changent. |
| [débogueur](https://developer.chrome.com/extensions/debugger) | Joindre à un ou plusieurs onglets pour instrumenter l’interaction réseau, déboguer JavaScript, modifier le DOM, modifier la CSS, etc. Le débogueur est utilisé pour cibler les onglets à l’aide de sendCommand et de l’itinéraire des événements par le biais des rappels onEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Effectuer des actions en fonction du contenu d’une page, sans nécessiter l’autorisation de lecture du contenu de la page. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Fournit plus de confidentialité en bloquant ou en modifiant des requêtes réseau en spécifiant des règles déclaratives. Autorisez les extensions à modifier les requêtes réseau sans intercepter la demande et afficher le contenu. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Capturez le contenu d’un écran, des fenêtres individuelles ou des onglets. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interagir avec la fenêtre inspectée. Par exemple, obtenez l’ID de onglet des pages, évaluez le code, rechargez des pages ou obtenez des ressources sur une page. |
| [devtools. Network](https://developer.chrome.com/extensions/devtools_network) | Récupérez les informations sur les requêtes réseau affichées par les outils de développement dans le volet réseau. |
| [devtools. panneaux](https://developer.chrome.com/extensions/devtools.panels) | Intégrez votre extension dans l’interface utilisateur de la fenêtre outils de développement en créant vos propres panneaux, en accédant aux panneaux existants ou en ajoutant des volets. |
| [téléchargements](https://developer.chrome.com/extensions/downloads) | Démarrer, surveiller, manipuler et Rechercher des téléchargements par programmation; |
| [Enterprise. hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Obtenez le fabricant et le modèle de la plateforme matérielle sur laquelle s’exécute le navigateur. Cette API n’est disponible que pour les extensions installées par une stratégie d’entreprise. |
| [venu](https://developer.chrome.com/extensions/events) | Types communs utilisés par des API qui déclenchent des événements pour vous avertir lorsqu’un événement intéressant se produit. |
| [long](https://developer.chrome.com/extensions/extension) | Toutes les pages de l’extension peuvent utiliser les utilitaires de cette API. Il inclut la prise en charge de l’échange de messages entre les extensions et les scripts de contenu, décrits dans le passage de messages. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Contient des déclarations de type pour les extensions Microsoft Edge. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Gérer les paramètres de police dans Microsoft Edge. |
| [historique](https://developer.chrome.com/extensions/history) | Interagissez avec l’enregistrement de pages visitées du navigateur. Vous pouvez ajouter, supprimer ou Rechercher des URL dans l’historique du navigateur. Pour remplacer la page d’historique par votre propre version, voir remplacer des pages. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implémenter l’internationalisation sur l’ensemble de votre application ou extension. |
| [inactif](https://developer.chrome.com/extensions/idle) | Détecter les changements d’état inactif de l’ordinateur. |
| [gestion des](https://developer.chrome.com/extensions/management) | Gérer la liste des extensions installées ou en cours d’exécution. Il est utile pour les extensions qui remplacent la nouvelle page d’onglets. |
| [notifications](https://developer.chrome.com/extensions/notifications) | Créez des notifications complètes à l’aide de modèles et affichez-les dans la barre d’état système. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Enregistrez des mots clés dans la barre d’adresses Microsoft Edge, également appelé omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Ajoutez des icônes dans la barre d’outils Microsoft Edge, à droite de la barre d’adresses. Les actions de page sont des actions qui peuvent être effectuées sur la page active et ne sont pas applicables à toutes les pages. Les actions de page apparaissent grisées lorsqu’elles sont inactives. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Enregistrez les onglets en tant que fichiers. MHTML.|
| [attribué](https://developer.chrome.com/extensions/permissions) | Récupérez les autorisations déclarées, facultatives lors de l’exécution, au lieu du moment de l’installation. Vous pouvez utiliser cette API pour afficher les autorisations nécessaires et approuvées pour vos utilisateurs. |
| [alimentation](https://developer.chrome.com/extensions/power) | Remplacez les fonctionnalités de gestion de l’alimentation du système. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Vous pouvez utiliser des événements pour interroger des imprimantes, leurs fonctionnalités et pour effectuer des travaux d’impression. |
| [confidentialité](https://developer.chrome.com/extensions/privacy) | Fonctionnalités de contrôle dans Microsoft Edge qui affectent la confidentialité d’un utilisateur. Cette API dépend du `EdgeSetting` prototype de `types` pour obtenir et définir la configuration de Microsoft Edge. |
| [doublure](https://developer.chrome.com/extensions/proxy) | Gérer les paramètres du proxy pour Microsoft Edge. Cette API dépend du `EdgeSetting` prototype de l' `types` API permettant d’obtenir et de définir la configuration de proxy de Microsoft Edge. |
| [Runtime](https://developer.chrome.com/extensions/runtime) | Récupérez la page d’arrière-plan, renvoyez des détails sur le manifeste, puis écoutez et répondez aux événements dans le cycle de vie de l’application ou de l’extension. Vous pouvez également convertir le chemin d’URL relatif d’URL en URL complètes. |
| [sessions](https://developer.chrome.com/extensions/sessions) | Recherchez et restaurez des onglets et des fenêtres à partir d’une session de navigation. |
| [stockage](https://developer.chrome.com/extensions/storage) | Stocker, récupérer et effectuer le suivi des modifications apportées aux données utilisateur. |
| [System. Memory](https://developer.chrome.com/extensions/system_memory) | `system.memory`API. |
| [System. Storage](https://developer.chrome.com/extensions/system_storage) | Recherchez des informations sur les périphériques de stockage. Vous pouvez également recevoir des notifications lorsque les périphériques de stockage sont attachés ou déconnectés. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interagir avec des flux de média par tabulation. |
| [eux](https://developer.chrome.com/extensions/tabs) | Interagissez avec le système de tabulations du navigateur pour créer, modifier et réorganiser les onglets. |
| [Sites](https://developer.chrome.com/extensions/topSites) | Accédez aux sites récurrents, également appelés sites visités, qui s’affichent sous l’onglet nouveau. Ces sites n’incluent pas de raccourcis personnalisés par l’utilisateur. |
| [synthèse](https://developer.chrome.com/extensions/tts) | Lire du texte synthèse vocale (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implémentez un moteur de conversion de texte par synthèse vocale à l’aide d’une extension. Les extensions qui s’inscrivent pour utiliser cette API reçoivent des événements qui contiennent des énoncés pour être prononcés et d’autres paramètres. Les extensions peuvent alors utiliser n’importe quelle technologie Web disponible pour synthétiser et générer des rapports vocaux, et renvoyer des événements à la fonction d’appel pour signaler l’État. |
| [types](https://developer.chrome.com/extensions/types) | Déclarations de type pour Microsoft Edge. |
| [Navigation Webnavigation](https://developer.chrome.com/extensions/webNavigation) | Recevoir des notifications concernant l’état des demandes de navigation. |
| [Instances](https://developer.chrome.com/extensions/webRequest) | Observez et analysez le trafic. Interordonnez, bloquez ou modifiez des requêtes. |
| [windows](https://developer.chrome.com/extensions/windows) | Interagissez avec les fenêtres du navigateur pour créer, modifier et réorganiser des fenêtres dans le navigateur. |



## API d’extension non prises en charge

Microsoft Edge ne prend pas en charge les API d’extension suivantes:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` -En guise d’alternative, vous pouvez utiliser `launchWebAuthFlow` pour récupérer un jeton OAuth2 pour authentifier les utilisateurs.
* `chrome.instanceID`.


## Autres considérations relatives aux API prises en charge

* L’utilisateur doit être connecté à Microsoft Edge en utilisant un compte MSA ou Azure Active Directory pour pouvoir l’utiliser `chrome.identity.getProfileUserInfo` . Si l’utilisateur est connecté à Microsoft Edge à l’aide d’un compte Active Directory local, l’API renvoie les `null` valeurs de messagerie et d’ID.

* Microsoft Edge ne prend pas en charge les extensions qui utilisent des paiements de chrome Web Store, car il utilise `identity.getAuthtoken` pour demander des jetons aux utilisateurs connectés. Ces jetons sont envoyés à l’API de gestion de licences basée sur le REST. 


<!-- links -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/apps/external_extensions).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
