---
ms.assetid: e56172c0-b635-4c02-8e0c-56bf8cb4c164
description: Découvrez comment prendre en main le contrôle de réseau Web, qui permet aux programmes et aux scripts de contrôler le comportement du navigateur Web.
title: WebDriver (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, Web Driver, sélénium, test
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab26931c09ecbae41ae88734b25038d21c93c0f6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233155"
---
# WebDriver (EdgeHTML)

L’API [WebDriver](https://www.w3.org/TR/webdriver/) W3C est une plate-forme et un protocole filaire qui autorisent des programmes ou des scripts à contrôler le comportement d’un navigateur Web.

Le WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction de l’utilisateur. Cette fonction est différente de celle des tests unitaires JavaScript, car le WebDriver a accès aux fonctionnalités et aux informations que JavaScript en cours d’exécution dans le navigateur ne permet pas de simuler plus précisément les événements utilisateur ou au niveau du système d’exploitation. Le Web Driver peut également gérer des tests sur plusieurs fenêtres, des onglets et des pages Web au sein d’une seule et même session de test.

Voici comment prendre en main le WebDriver pour Microsoft Edge (EdgeHTML).

Dans le cadre de la compatibilité descendante avec les tests existants, l’implémentation de Microsoft Edge (EdgeHTML) de WebDriver prend en charge les spécifications du World [Driver](https://www.w3.org/TR/webdriver/) W3C et du [protocole JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol) .

## Commencer à utiliser le WebDriver pour Microsoft Edge (EdgeHTML)
* Installation de Windows 10.
* Téléchargez le serveur [Microsoft WebDriver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/) approprié pour votre version de Windows et Microsoft Edge (EdgeHTML).
* Téléchargez la liaison de langue de votre choix. [Toutes les liaisons de langue de sélénium prennent en charge Microsoft Edge (EdgeHTML)](https://docs.seleniumhq.org/download/).

> [!NOTE]
> Vous pouvez trouver de l’aide, signaler des problèmes et formuler des demandes de fonctionnalité de fichier à l’aide des [& commentaires Microsoft Edge (EdgeHTML)](https://developer.microsoft.com/microsoft-edge/support/).


## Utilisation du WebDriver
Pour commencer à utiliser le Web à l’aide de Microsoft Edge (EdgeHTML), consultez les exemples suivants:

* [Exemple de code C \ #](https://gist.github.com/InstyleVII/baf25274c55e891076d5#file-webdriver-cs) pour ouvrir une fenêtre de navigateur, en accédant à Bing.com et en effectuant une recherche sur’WebDriver' (GitHub).

## Balises de la ligne de commande du serveur WebDriver
Liste des indicateurs de ligne de commande pour le serveur WebDriver.

| Nom    | Description                                                                                                      | Version disponible |
|:--------|:-----------------------------------------------------------------------------------------------------------------|:------------------|
| Metahost    | Adresse IP de l’hôte à utiliser pour le serveur WebDriver (par défaut: localhost)                                                     | 14393             |
| port    | Port à utiliser pour le serveur WebDriver (par défaut: 17556)                                                            | 14393             |
| package | ApplicationUserModelId (AUMID) pour que l’application soit lancée par le serveur WebDriver                        | 14393             |
| détaillée | Génère les demandes reçues et les réponses envoyées par le serveur WebDriver                                             | 14393             |
| silent  | Ne génère aucune valeur                                                                                                  | 15063             |
| version | Génère la version de MicrosoftWebDriver.exe                                                                    | 17763             |
| W3C     | Utiliser le protocole W3C Web Driver (option par défaut)                                                                      | 17763             |
| jwp     | Utiliser le protocole filaire JSON                                                                                           | 17763             |
| nettoyage | Nettoyage de données temporaires et de clés de Registre définies par le serveur WebDriver pour le package. Les autres paramètres ne sont pas pris en compte | 17763             |

## W3C WebDriver
La prise en charge sur une base par commande pour la [spécification du World Driver W3C](https://www.w3.org/TR/webdriver/).

### Fonctionnalités
| Fonctionnalité                       | Clé                       | Statut                   | Version disponible |
|:---------------------------------|:--------------------------|:-------------------------|:------------------|
| Nom du navigateur                     | "browserName"             | Pris en charge                | 17763             |
| Version du navigateur                  | "browserVersion"          | Pris en charge                | 17763             |
| Nom de la plateforme                    | "platformName"            | Pris en charge                | 17763             |
| Accepter les certificats TLS non sécurisés | "acceptInsecureCerts"     | Non &nbsp; pris en charge       | Non applicable               |
| Stratégie de chargement de page               | "pageLoadStrategy"        | Pris en charge                | 17763             |
| Configuration du proxy              | doublure                   | Non &nbsp; pris en charge       | Non applicable               |
| Dimensionnement/positionnement de fenêtre  | SetWindowRect           | Pris en charge                | 17763             |
| Configuration du délai d’expiration de session   | délais d’expiration                | Pris en charge                | 17763             |
| Comportement d’invite non géré        | "unhandledPromptBehavior" | Partiellement &nbsp; pris en charge | 17763             |
| InPrivate                        | "ms: InPrivate"            | Pris en charge                | 17763             |
| Chemins d’extension                  | "ms: extensionPaths"       | Pris en charge                | 17763             |
| Page de démarrage                       | "ms: startPage"            | Pris en charge                | 17763             |

### Stratégies de localisateur
| Stratégie de localisateur                                                        | Statut    | Version disponible |
|:------------------------------------------------------------------------|:----------|:------------------|
| [Sélecteurs de CSS](https://www.w3.org/TR/webdriver/#css-selectors)         | Pris en charge | 17763             |
| [Texte du lien](https://www.w3.org/TR/webdriver/#link-text)                 | Pris en charge | 17763             |
| [Texte d’une liaison partielle](https://www.w3.org/TR/webdriver/#partial-link-text) | Pris en charge | 17763             |
| [Nom de la balise](https://www.w3.org/TR/webdriver/#tag-name)                   | Pris en charge | 17763             |
| [Suivante](https://www.w3.org/TR/webdriver/#xpath)                         | Pris en charge | 17763             |

### Commandes
| Méthode HTTP | Modèle d’URI                                                   | Commande                                                                                   | Statut             | Version disponible |
|:------------|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------|:-------------------|:----------------  |
| POST        | /session                                                       | [Nouvelle session](https://www.w3.org/TR/webdriver/#new-session)                               | Pris en charge          | 17763             |
| DELETE      | ID/session/{session                                          | [Supprimer une session](https://www.w3.org/TR/webdriver/#delete-session)                         | Pris en charge          | 17763             |
| GET         | /Status                                                        | [Statut](https://www.w3.org/TR/webdriver/#status)                                         | Pris en charge          | 17763             |
| GET         | ID/session/{session/timeouts                                 | [Obtenir des délais d’expiration](https://www.w3.org/TR/webdriver/#get-timeouts)                             | Pris en charge          | 17763             |
| POST        | ID/session/{session/timeouts                                 | [Définir des délais d’expiration](https://www.w3.org/TR/webdriver/#set-timeouts)                             | Pris en charge          | 17763             |
| POST        | ID/session/{session/URL                                      | [Accédez à](https://www.w3.org/TR/webdriver/#navigate-to)                               | Pris en charge          | 17763             |
| GET         | ID/session/{session/URL                                      | [Obtenir l’URL actuelle](https://www.w3.org/TR/webdriver/#get-current-url)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Back                                     | [Back](https://www.w3.org/TR/webdriver/#back)                                             | Pris en charge          | 17763             |
| POST        | ID/session/{session/Forward                                  | [Forward](https://www.w3.org/TR/webdriver/#forward)                                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Refresh                                  | [Actualiser](https://www.w3.org/TR/webdriver/#refresh)                                       | Pris en charge          | 17763             |
| GET         | /session/{session ID}/title                                    | [Obtenir le titre](https://www.w3.org/TR/webdriver/#get-title)                                   | Pris en charge          | 17763             |
| GET         | ID/session/{session/Window                                   | [Handle de fenêtre Get](https://www.w3.org/TR/webdriver/#get-window-handle)                   | Pris en charge          | 17763             |
| DELETE      | ID/session/{session/Window                                   | [Fermer la fenêtre](https://www.w3.org/TR/webdriver/#close-window)                             | Pris en charge          | 17763             |
| POST        | ID/session/{session/Window                                   | [Basculer vers la fenêtre](https://www.w3.org/TR/webdriver/#switch-to-window)                     | Pris en charge          | 17763             |
| GET         | ID/session/{session/Window/Handles                           | [Obtenir des poignées de fenêtre](https://www.w3.org/TR/webdriver/#get-window-handles)                 | Pris en charge          | 17763             |
| POST        | ID/session/{session/Frame                                    | [Basculer vers le cadre](https://www.w3.org/TR/webdriver/#switch-to-frame)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Frame/parent                             | [Basculer vers le cadre parent](https://www.w3.org/TR/webdriver/#switch-to-parent-frame)         | Pris en charge          | 17763             |
| GET         | ID/session/{session/Window/Rect                              | [Obtenir la fenêtre Rect](https://www.w3.org/TR/webdriver/#get-window-rect)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Window/Rect                              | [Définir la fenêtre Rect](https://www.w3.org/TR/webdriver/#set-window-rect)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Window/Maximize                          | [Agrandir la fenêtre](https://www.w3.org/TR/webdriver/#maximize-window)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Window/Minimize                          | [Réduire la fenêtre](https://www.w3.org/TR/webdriver/#minimize-window)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Window/fullscreen                        | [Fenêtre plein écran](https://www.w3.org/TR/webdriver/#fullscreen-window)                   | Non &nbsp; pris en charge | Non applicable               |
| GET         | ID/session/{session/Element/active                           | [Get actif, élément](https://www.w3.org/TR/webdriver/#get-active-element)                 | Pris en charge          | 17763             |
| POST        | ID/session/{session/Element                                  | [Élément Find](https://www.w3.org/TR/webdriver/#find-element)                             | Pris en charge          | 17763             |
| POST        | ID/session/{session/Elements                                 | [Rechercher des éléments](https://www.w3.org/TR/webdriver/#find-elements)                           | Pris en charge          | 17763             |
| POST        | ID de/session/{session/element/{element/element             | [Rechercher l’élément à partir de l’élément](https://www.w3.org/TR/webdriver/#find-element-from-element)   | Pris en charge          | 17763             |
| POST        | ID de/session/{session/element/{element/Elements            | [Rechercher des éléments à partir de l’élément](https://www.w3.org/TR/webdriver/#find-elements-from-element) | Pris en charge          | 17763             |
| GET         | ID de/session/{session/element/{element/Selected            | [Élément sélectionné](https://www.w3.org/TR/webdriver/#is-element-selected)               | Pris en charge          | 17763             |
| GET         | ID de/session/{session/element/{element/attribute/{name}    | [Get, attribut d’élément](https://www.w3.org/TR/webdriver/#get-element-attribute)           | Pris en charge          | 17763             |
| GET         | ID de/session/{session/element/{element/Property/{Name}     | [Propriété Get, élément](https://www.w3.org/TR/webdriver/#get-element-property)             | Pris en charge          | 17763             |
| GET         | /session/{session ID =/element/{element ID}/CSS/{Property Name} | [Obtenir la valeur CSS de l’élément](https://www.w3.org/TR/webdriver/#get-element-css-value)           | Pris en charge          | 17763             |
| GET         | ID de/session/{session/element/{element/Text                | [Obtenir le texte de l’élément](https://www.w3.org/TR/webdriver/#get-element-text)                     | Pris en charge          | 17763             |
| GET         | ID de/session/{session                | [Obtenir le nom de la balise d’élément](https://www.w3.org/TR/webdriver/#get-element-tag-name)             | Pris en charge          | 17763             |
| GET         | ID de/session/{session/element/{element/Rect                | [Obtenir l’élément Rect](https://www.w3.org/TR/webdriver/#get-element-rect)                     | Pris en charge          | 17763             |
| GET         | ID de/session/{session/element/{element/Enabled             | [L’élément est-il activé](https://www.w3.org/TR/webdriver/#is-element-enabled)                 | Pris en charge          | 17763             |
| POST        | ID de/session/{session/element/{element/Click               | [Cliquez sur l’élément](https://www.w3.org/TR/webdriver/#element-click)                           | Pris en charge          | 17763             |
| POST        | /session/{session ID}/element/{element ID}/Clear               | [Élément Clear](https://www.w3.org/TR/webdriver/#element-clear)                           | Pris en charge          | 17763             |
| POST        | ID de/session/{session/element/{element/sendKeys            | [Touches d’envoi d’élément](https://www.w3.org/TR/webdriver/#element-send-keys)                   | Pris en charge          | 17763             |
| GET         | ID/session/{session                                   | [Obtenir la source de la page](https://www.w3.org/TR/webdriver/#get-page-source)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Execute/Sync                             | [Exécuter le script](https://www.w3.org/TR/webdriver/#execute-script)                         | Pris en charge          | 17763             |
| POST        | ID/session/{session/Execute/Async                            | [Exécuter le script Async](https://www.w3.org/TR/webdriver/#execute-async-script)             | Pris en charge          | 17763             |
| GET         | ID/session/{session/cookie                                   | [Obtenir tous les cookies](https://www.w3.org/TR/webdriver/#get-all-cookies)                       | Pris en charge          | 17763             |
| GET         | ID/session/{session/cookie/{Name}                            | [Obtenir le cookie nommé](https://www.w3.org/TR/webdriver/#get-named-cookie)                     | Pris en charge          | 17763             |
| POST        | ID/session/{session/cookie                                   | [Ajouter un cookie](https://www.w3.org/TR/webdriver/#add-cookie)                                 | Pris en charge          | 17763             |
| DELETE      | ID/session/{session/cookie/{Name}                            | [Supprimer le cookie](https://www.w3.org/TR/webdriver/#delete-cookie)                           | Pris en charge          | 17763             |
| DELETE      | ID/session/{session/cookie                                   | [Supprimer tous les cookies](https://www.w3.org/TR/webdriver/#delete-all-cookies)                 | Pris en charge          | 17763             |
| POST        | ID/session/{session/actions                                  | [Effectuer des actions](https://www.w3.org/TR/webdriver/#perform-actions)                       | Pris en charge          | 17763             |
| DELETE      | ID/session/{session/actions                                  | [Actions de publication](https://www.w3.org/TR/webdriver/#release-actions)                       | Pris en charge          | 17763             |
| POST        | ID/session/{session/Alert/dismiss                            | [Ignorer l’alerte](https://www.w3.org/TR/webdriver/#dismiss-alert)                           | Pris en charge          | 17763             |
| POST        | ID/session/{session/Alert/Accept                             | [Accepter l’alerte](https://www.w3.org/TR/webdriver/#accept-alert)                             | Pris en charge          | 17763             |
| GET         | ID/session/{session/Alert/Text                               | [Obtenir le texte d’une alerte](https://www.w3.org/TR/webdriver/#get-alert-text)                         | Pris en charge          | 17763             |
| POST        | ID/session/{session/Alert/Text                               | [Envoyer un message d’alerte](https://www.w3.org/TR/webdriver/#send-alert-text)                       | Pris en charge          | 17763             |
| GET         | ID/session/{session/screenshot                               | [Prendre une capture d’écran](https://www.w3.org/TR/webdriver/#take-screenshot)                       | Pris en charge          | 17763             |
| GET         | ID/session/{session/screenshot/{Element}                  | [Capture d’écran de l’élément](https://www.w3.org/TR/webdriver/#take-element-screenshot)       | Pris en charge          | 17763             |

## Protocole filaire JSON
La prise en charge sur une base par commande pour le [protocole filaire JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol).

### Commandes
| Méthode HTTP | Chemin d'accès                                                                                                                                                         | Statut             | Version disponible |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------|
| GET         | [/Status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)                                                                               | Pris en charge          | 10240             |
| POST        | [/session](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#session-1)                                                                           | Pris en charge          | 10240             |
| GET         | [/sessions](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessions)                                                                           | Pris en charge          | 10240             |
| GET         | [/session/: sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Pris en charge          | 10240             |
| DELETE      | [/session/: sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/temporisation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeouts)                                        | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/temporisation/async_script](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsasync_script)               | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/temporisation/implicit_wait](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsimplicit_wait)             | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/window_handle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handle)                              | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/window_handles](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handles)                            | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/Forward](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidforward)                                          | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/précédent](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidback)                                                | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/actualiser](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidrefresh)                                          | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/exécuter](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute)                                          | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/execute_async](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute_async)                              | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/capture d’écran](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidscreenshot)                                    | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/IME/available_engines](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeavailable_engines)               | Non &nbsp; pris en charge | Non applicable               |
| GET         | [/session/: sessionId/IME/active_engine](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactive_engine)                       | Non &nbsp; pris en charge | Non applicable               |
| GET         | [/session/: sessionId/IME/activé](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivated)                               | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/IME/désactivé](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimedeactivate)                             | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/IME/activation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivate)                                 | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/Frame](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframe)                                              | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/Frame/parent](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframeparent)                                 | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Pris en charge          | 10586             |
| DELETE      | [/session/: sessionId/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/Window/: windowHandle/Size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/Window/: windowHandle/Size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/Window/: windowHandle/position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/Window/: windowHandle/position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/Window/: windowHandle/Maximize](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlemaximize) | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Pris en charge          | 10240             |
| DELETE      | [/session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Pris en charge          | 10586             |
| DELETE      | [/session/: sessionId/cookie/: nom](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookiename)                                  | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/source](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsource)                                            | Pris en charge          | 10586             |
| GET         | [/session/: sessionId}/title](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtitle)                                             | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/élément](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelement)                                          | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/éléments](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelements)                                        | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/élément/actif](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementactive)                             | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/élément/: ID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementid)                                    | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/élément/: ID/élément](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelement)                     | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/élément/: ID/éléments](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelements)                   | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/Element/: ID/Click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclick)                         | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/élément/: ID/envoi](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsubmit)                       | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/élément/: ID/texte](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidtext)                           | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/élément/: ID/valeur](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidvalue)                         | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/clés](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidkeys)                                                | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/Element/: ID/Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidname)                           | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/élément/: ID/Clear](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclear)                         | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/élément/: ID/sélectionné](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidselected)                   | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/élément/: ID/activé](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidenabled)                     | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/élément/: ID/attribut/: nom](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidattribute/:name)     | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/élément/: ID/égal/: Other](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidequals/:other)         | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/élément/: ID/affiché](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementiddisplayed)                 | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/élément/: ID/emplacement](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation)                   | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/élément/: ID/location_in_view](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation_in_view)   | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/élément/: ID/taille](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsize)                           | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/élément/: ID/CSS/:p ropertyName](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidcss/:propertyName) | Pris en charge          | 10240             |
| GET         | [/session/: sessionId/orientation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/orientation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Non &nbsp; pris en charge | Non applicable               |
| GET         | [/session/: sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/accept_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidaccept_alert)                                | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/dismiss_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddismiss_alert)                              | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/MoveTo](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidmoveto)                                            | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/Click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidclick)                                              | Pris en charge          | 10240             |
| POST        | [/session/: sessionId/ButtonDown](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttondown)                                    | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/BUTTONUP](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttonup)                                        | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddoubleclick)                                  | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/TouchWare/Click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchclick)                                   | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/effleurement](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdown)                                     | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/TouchWare/up](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchup)                                         | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/effleurement/déplacer](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchmove)                                     | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/effleurement/défilement](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll)                                 | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/effleurement/défilement](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll-1)                               | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/TouchWare/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdoubleclick)                       | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/TouchWare/longclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchlongclick)                           | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/tactile/raccourci](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick)                                   | Non &nbsp; pris en charge | Non applicable               |
| POST        | [/session/: sessionId/tactile/raccourci](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick-1)                                 | Non &nbsp; pris en charge | Non applicable               |
| GET         | [/session/: sessionId/emplacement](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/emplacement](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Pris en charge          | 10586             |
| DELETE      | [/session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Pris en charge          | 10586             |
| DELETE      | [/session/: sessionId/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/local_storage/Size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagesize)                     | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Pris en charge          | 10586             |
| POST        | [/session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Pris en charge          | 10586             |
| DELETE      | [/session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Pris en charge          | 10586             |
| DELETE      | [/session/: sessionId/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/session_storage/Size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagesize)                 | Pris en charge          | 10586             |
| GET         | [/session/: sessionId/log](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlog)                                                  | Non &nbsp; pris en charge | Non applicable               |
| GET         | [/session/: sessionId/log/types](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlogtypes)                                       | Non &nbsp; pris en charge | Non applicable               |
| GET         | [/session/: sessionId/application_cache/Status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidapplication_cachestatus)         | Pris en charge          | 10586             |  
