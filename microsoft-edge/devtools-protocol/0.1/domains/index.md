---
description: Liste de références pour les domaines pris en charge dans la version 0,1 du protocole Microsoft Edge DevTools.
title: DevTools protocole Domains-DevTools Protocol version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: de816e2b07838ba1b6151967ff7b8751789c60ea
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882946"
---
# DevTools protocole Domains-DevTools Protocol version 0,1 (EdgeHTML)  

## [Débogueur](debugger.md)  

Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.
## [Page](page.md)
Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
## [Runtime](runtime.md)
Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
## [Schéma](schema.md)
Fournit des informations sur le schéma de protocole.