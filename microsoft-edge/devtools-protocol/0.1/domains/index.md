---
description: Liste de références pour les domaines pris en charge dans la version 0,1 du protocole Microsoft Edge DevTools.
title: Domains-protocole DevTools version 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: b3cf3411a8402b7407012eb789f8bf267b4997a8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565487"
---
# Domaines de protocole DevTools
## [Débogueur](debugger.md)
Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.
## [Page](page.md)
Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
## [Runtime](runtime.md)
Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
## [Schéma](schema.md)
Fournit des informations sur le schéma de protocole.