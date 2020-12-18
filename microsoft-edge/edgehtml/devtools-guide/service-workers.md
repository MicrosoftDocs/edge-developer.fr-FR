---
description: Utiliser le panneau des travailleurs de services pour gérer et déboguer vos travailleurs de service
title: DevTools-débogueur-travailleurs de service
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, débogueur, débogage, PWA, travailleur de service, API de cache
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 99592f787da8bcf89d2e16231aa3f39047b4fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233260"
---
# Worker du service

Le panneau **travailleurs de service** dispose d’outils permettant de gérer et de déboguer les travailleurs de service de votre site pour vous aider:

 - Obtenez une vue d’ensemble de tous les travailleurs de service associés à votre site et des détails de leur étendue et de leur état.
 - **Mettre à jour** et gérer (**désinscrire**) l’inscription du travailleur de service pour l’étendue donnée
 - **Diffuser** une notification de test
 - **Arrêt** / **Lancer** des travailleurs de service individuels et
 - **Inspecter** le travailleur de service sélectionné dans une fenêtre de débogueur séparée

![Volet vue d’ensemble des travailleurs de services](./media/service_worker.png)

Notez les points suivants concernant le débogage des travailleurs de services dans Edge DevTools:

 - Le débogage d’un ouvrier de service lancera une nouvelle instance du DevTools séparée des outils de la page, car les travailleurs de services peuvent être partagés entre plusieurs onglets.
 - Les [**éléments**](./elements.md) et les panneaux d' [**émulation**](./emulation.md) ne sont pas pris en tant que débogueur de service, car ils s’exécutent en arrière-plan et ne contrôlent pas directement le serveur principal de votre application.
 - Pour le moment, le trafic réseau d’un ouvrier de service est uniquement signalé à partir de l’instance de débogage de DevTools pour ce travailleur et non à partir de l’instance de débogueur de la page elle-même.
 - Pour simuler une **Poussée** à partir du devtools, vous devez ajouter un écouteur d’événements de *type pousser* à votre travailleur de service afin d’observer son effet. L’exemple suivant imprime «message envoyé par test de DevTools» dans la **console**de votre travailleur de service.

   ```JavaScript
   self.addEventListener('push', function(event){
       console.log(event.data.text());
   });
   ```

Voici quelques éléments généraux à garder à l’esprit lorsque vous utilisez des travailleurs de service:

- **HTTPs uniquement.** Les travailleurs de service ne fonctionnent pas dans HTTP; vous devrez utiliser HTTPs. Toutefois, vous pouvez enregistrer des travailleurs de service à des `localhost` fins de test.

- **Aucun accès au DOM n’est autorisé.** Comme pour les travailleurs Web, vous n’obtenez pas l’accès au modèle d’objet de la page. Cela signifie que si vous avez besoin de modifier des informations sur la page, vous devez l’utiliser à [`postMessage`](https://developer.mozilla.org/docs/Web/API/Worker/postMessage) partir du travailleur du service sur la page pour pouvoir gérer les modifications du DOM à partir de la page.

- **S’exécute séparément de la page.** Étant donné que ces scripts ne sont pas liés à la durée de vie d’une page, il est important de comprendre qu’ils ne partagent pas le même contexte que la page. Outre l’accès au DOM sans avoir accès au DOM (comme indiqué plus haut), il n’aura pas accès aux mêmes variables disponibles sur la page.

- **Remplace le cache de l' *application*.** Le cache d’application sera ignoré lorsque des travailleurs de service sont en cours d’utilisation. L’API Worker worker est conçue pour supplanter entièrement le cache d’application en fournissant un contrôle plus précis au développeur Web.

  - **Le script ne peut pas être sur le CDN.** Le fichier JavaScript pour le travailleur de service ne peut pas être hébergé sur un réseau de distribution de contenu (CDN), il doit figurer dans le même domaine que la page. Néanmoins, si vous le souhaitez, vous pouvez importer des scripts à partir de votre réseau de distribution de contenu (CDN).

- **Peut être arrêté à tout moment.** Les travailleurs de service sont censés être courts et leur durée de vie est liée à des événements. En particulier, les travailleurs de service ont un délai dans lequel ils doivent terminer d’exécuter leurs gestionnaires d’événements. Dans d’autres cas, le navigateur ou le système d’exploitation est susceptible de mettre fin à un travailleur de service ayant un impact sur la batterie, le processeur ou la consommation de mémoire. Dans les deux cas, évitez de dépendre des variables globales du script de travailleur de service au cas où une instance de travailleur de service différente est utilisée sur un événement ultérieur géré.

- **Uniquement les requêtes asynchrones autorisées.** Le XHR synchrone n’est pas autorisé ici. Aucun d’entre eux n’est localStorage, il est donc préférable d’utiliser IndexedDB et la nouvelle API caches décrite plus haut.

- **Le travailleur de service est 1:1.** Vous ne pourrez avoir qu’un seul travailleur par étendue. Cela signifie que si vous tentez d’inscrire un autre travailleur de service pour une étendue qui possède déjà un travailleur de service, ce travailleur de service sera mis à jour.
