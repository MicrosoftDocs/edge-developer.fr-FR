---
description: Cette page fournit une documentation sur la chaîne de l’agent utilisateur Microsoft Edge
title: Chaîne de l’agent utilisateur Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web, chaîne d’agent utilisateur, chaîne UA, substitutions UA
ms.openlocfilehash: 73401219b7708a739292a46b6131fe40765e9c8c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566666"
---
# Chaîne de l’agent utilisateur Microsoft Edge (bureau)  

Une chaîne d’agent utilisateur \ (UA \) peut être utilisée pour détecter la version d’un navigateur spécifique utilisée sur un certain système d’exploitation.  À l’instar des autres navigateurs, Microsoft Edge inclut ces informations dans l' `User-Agent` en-tête http dès qu’il envoie une demande à un site.  Il est également possible d’y accéder en utilisant JavaScript en interrogeant la valeur de `navigator.userAgent` .  

Microsoft recommande aux développeurs Web de se servir de la [fonctionnalité de détection de fonctionnalités](https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection) chaque fois que cela peut améliorer la facilité de maintenance du code, de réduire le Fragility de code et d’éliminer le risque de rupture du code lors des mises à jour ultérieures des chaînes UA.  

Dans le cas où la détection des fonctionnalités n’est pas applicable et que la détection UA doit être utilisée, le format de la version de bureau de Microsoft Edge UA sur le bureau est le suivant:

L' `User-Agent` en-tête de requête est au format suivant:

```http
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43
``` 

La valeur de retour de `navigator.userAgent` a le format suivant:

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43"
```  

Les identificateurs de plateforme changent en fonction du système d’exploitation utilisé, et les numéros de version sont incrémentés en même temps.  Ce format est identique à celui de l’UA du chrome et à l’ajout d’un nouveau `Edg` jeton à la fin.  Microsoft a sélectionné le `Edg` jeton pour éviter les problèmes de compatibilité liés à l’utilisation de la chaîne `Edge` , qui est utilisée par la version de Microsoft Edge basée sur EdgeHTML.  Le `Edg` jeton est également cohérent avec les [jetons existants](https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer/) utilisés sur iOS et Android.

## Mappage de la chaîne UA au nom du navigateur
Le mappage des jetons de chaîne UA vers un nom de navigateur plus lisible en personne à utiliser dans le code est un modèle commun sur le Web dès aujourd’hui. Lorsque vous mappez le nouveau `Edg` jeton à un nom de navigateur, Microsoft recommande d’utiliser un autre nom que celui utilisé par les développeurs pour la version héritée de Microsoft Edge pour éviter d’appliquer accidentellement des solutions de contournement héritées qui ne sont pas applicables aux navigateurs en chrome.

## Remplacements de l’agent utilisateur  

Parfois, un site Web ne reconnaît pas la version mise à jour du Microsoft Edge UA.  Par conséquent, il est possible que l’ensemble des fonctionnalités de ce site Web ne fonctionne pas correctement.  Lorsque Microsoft est prévenu de ces types de problèmes, les propriétaires de sites Web sont contactés et informés de la mise à jour des UA.  

Les sites nécessitent souvent du temps pour mettre à jour et tester la logique de détection des UA pour résoudre les problèmes liés à Microsoft pour les propriétaires de sites.  Dans ces cas, Microsoft utilise une liste de remplacements UA dans nos canaux bêta et stables pour optimiser la compatibilité des utilisateurs qui accèdent à ces sites.  Les substitutions spécifient de nouvelles valeurs UA qui doivent être envoyées par Microsoft Edge au lieu du paramètre UA par défaut pour des sites spécifiques.  Vous pouvez consulter la liste des remplacements UA actuellement appliqués en accédant à `edge://compat/useragent` la version bêta et aux canaux de Microsoft Edge. 

Pour le moment, nos Canaries et nos canaux de développement n’ont pas de remplacement UA de sorte que les développeurs Web disposent d’un environnement permettant de reproduire facilement les problèmes rencontrés par la fonction UA par défaut de Microsoft Edge.  Si, pour une raison quelconque, vous avez besoin de désactiver les remplacements UA dans les canaux bêta ou stables de Microsoft Edge, vous pouvez exécuter le fichier exécutable Microsoft Edge en utilisant l’argument de ligne de commande suivant:  

```shell
--disable-domain-action-user-agent-override
```  
