---
description: Rendez votre extension accessible pour différentes langues et testez vos chaînes de langue grâce au Guide d’internationalisation.
title: Extensions-internationalisation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbbc847ebd2103cba2eca8a791009b4e72f93a6f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233404"
---
# Internationalisation  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Pour rendre votre extension accessible à un large éventail de personnes, il est important de développer en même tant que d’autres pays. Les extensions Microsoft Edge vous permettent d’ajouter différentes chaînes de langue à vos extensions de sorte que leur langue puisse être facilement modifiée.

Pour en savoir plus sur la mise en international de votre poste, consultez le [Guide international](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)MDN.


## Langues de test

Pour tester vos chaînes de langue, vous devez d’abord définir la langue d’affichage de Windows sur celle que vous souhaitez tester.

Pour modifier la langue d’affichage de Windows, procédez comme suit:

1. Ouvrez l’application paramètres.

   ![application paramètres](./../media/loc-settings.png)
2. Sélectionnez «heure & langue».
3. Sélectionnez «région & langue».
4. Sélectionnez "+ ajouter une langue" pour ajouter la langue à la liste de langues possibles.
5. Dans la liste «langues», choisissez la langue que vous souhaitez tester.
6. Sélectionnez le bouton «définir par défaut» (il est possible que vous deviez redémarrer votre PC).
7. Ouvrez Microsoft Edge et vérifiez que les chaînes définies pour les paramètres régionaux apparaissent comme prévu.

À l’aide de la propriété [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) , vous pouvez vérifier que la langue Microsoft Edge est déterminée comme étant correcte.

Cliquez sur le bouton dans le CodePen ci-dessous pour afficher la langue d’affichage de votre navigateur.

<iframe height='300' scrolling='no' title='Obtention des paramètres régionaux' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> </a> Pour plus d’MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='http://codepen.io'> CodePen </a> , voir Pen Get.
</iframe>
