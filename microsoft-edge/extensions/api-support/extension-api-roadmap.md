---
description: Trouvez des informations sur la progression actuelle vers la fin de l’API d’extension Microsoft Edge.
title: Introduction à l’API d’extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, API, extensions, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: ce40dd2d37b7ef446516a743286c5285ad3187a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565401"
---
# Introduction à l’API d’extension Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Outre les API Web, l’API d’extension permet d’utiliser des extensions pour assurer une intégration plus approfondie avec l’hôte de navigateur. Cette API permet aux développeurs d’accéder aux fonctionnalités du navigateur Microsoft Edge, telles que la manipulation des onglets et des fenêtres. Le tableau suivant décrit en détail les API prises en charge/en développement pour les builds publiées par Windows 10 de Microsoft Edge.


|     Cours     |                                                              Description                                                              |                État — numéro de build                 |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
|   favoris   |                                          Utilisé pour créer, organiser et manipuler des signets.                                          | Pris en charge: Microsoft Edge (40)/Windows 10 (15063) |
| browserAction |                                 Autorise les extensions à ajouter un bouton persistant dans Microsoft Edge.                                  | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
| commandes      |                                                      Définit des raccourcis clavier.                                                      | En considération
| contextMenus  |                           Ajoute un élément de menu contextuel sur une URL spécifique, dans un contexte spécifié d’une page Web.                            | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|    les    |                                 Permet de rechercher et de modifier des cookies, ainsi que de notifier leur changement.                                 | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|   téléchargements   |                           Utilisé pour lancer, surveiller, manipuler et Rechercher des téléchargements par programmation.                           |                 En considération                  |
|   long   |                                      Contient des utilitaires qui peuvent être utilisés par n’importe quelle page d’extension.                                       | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|    historique    |                                         Interagit avec l’enregistrement de pages visitées du navigateur.                                         |                 En considération                  |
|     i18n      |                                         Implémente l’internationalisation sur une extension.                                          | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|   identité    |                                       Utilisé pour obtenir un code d’autorisation OAuth2 ou un jeton d’accès.                                       |                 En considération                  |
|     inactif      |                                       Permet de détecter la modification de l’état inactif de l’ordinateur.                                        | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|  gestion des   |                                              Obtient des informations sur les modules complémentaires installés.                                                |                 En considération                  |
| notifications |                      Autorise la création de notifications à l’aide de modèles qui s’affichent dans la barre d’état système de l’utilisateur.                      | Pris en charge-Microsoft Edge (42)/Windows 10 (17134) |
|  pageAction   |                                      Active les extensions pour ajouter un bouton dans la barre d’adresses.                                       | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|  attribué  |                   Permet aux utilisateurs de sélectionner les autorisations facultatives auxquelles ils souhaitent accorder un accès par extension.                   |                 En considération                  |
|    Runtime    | Extrait la page d’arrière-plan, renvoie des détails sur le manifeste, et écoute et répond aux événements dans le cycle de vie de l’extension. | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|    stockage    |                                      Utilisé par l’extension pour lire/écrire des données et pour synchroniser les données.                                       | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|     eux      |                Interagit avec le système de tabulations de Microsoft Edge en créant, modifiant et réorganisant les onglets dans le navigateur.                | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
| Navigation Webnavigation |                           Utilisé pour recevoir des notifications concernant l’état des demandes de navigation en cours de vol.                            | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|  Instances   |        Autorise l’utilisation de l’API WebRequest pour observer et analyser le trafic et pour intercepter, bloquer ou modifier les demandes en transit.        | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |
|    windows    |                              Interagit avec le navigateur en créant, modifiant et réorganisant les fenêtres.                              | Pris en charge: Microsoft Edge (38)/Windows 10 (14393) |

