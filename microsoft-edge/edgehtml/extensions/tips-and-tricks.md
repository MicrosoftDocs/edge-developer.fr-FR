---
description: En savoir plus sur les conseils et astuces utiles concernant les extensions Microsoft Edge
title: Trucs et astuces | Variable
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur, extensions
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd512085f13b76c5a8e474301ef296612eeb0414
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233020"
---
# Conseils et astuces  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Si vous travaillez actuellement sur une extension Microsoft Edge ou si vous avez déjà publié une extension, les conseils et astuces suivants peuvent être utiles.

## Obtenir un lien direct vers votre extension dans le Microsoft Store

Le tableau de bord du centre de développement Windows vous permet de trouver un lien direct vers votre extension dans le Microsoft Store. Ce lien peut être utile pour publier et partager votre extension.

Après vous être connecté au centre de développement Windows et avoir navigué vers votre extension via le tableau de bord, dans la page identité de l’application, vous trouverez le lien dans la ligne **lier le protocole Store** :

![lien vers le protocole Store](./media/store-link.png)
 
## Vérifiez que vous suivez la politique du Microsoft Store.

Lorsque vous créez votre extension, veillez à garder à l’esprit les recommandations en matière de soumission à la boutique Microsoft en surbrillance dans la [politique Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx). 
 
Les extensions Microsoft Edge disposent également d’un ensemble supplémentaire de stratégies à [suivre.](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)

## Améliorer la détectabilité de votre extension dans la boutique Microsoft

Vous pouvez ajouter des mots clés à votre soumission d’extension pour améliorer sa détectabilité par le biais de recherches. Par exemple, «Microsoft Edge extensions» et «nom de mon extension». 

Pour cela, vous pouvez effectuer cette opération dans le centre de développement Windows, sous la section Description de votre extension. Vous devrez ajouter ces mots clés pour chaque langue prise en charge par votre extension.

![Envoyer une réponse à un avis-Keywords](./media/keywords.png)

## Automatiser votre soumission sur le Microsoft Store

Vous pouvez automatiser et rationaliser vos soumissions du Microsoft Store à l’aide de la nouvelle API de soumission du Windows Store, qui vous permet de mettre à jour les applications/jeux, les modules complémentaires (achats dans l’application) et les versions d’évaluation de package via une API REST. Consultez la [documentation et les exemples,](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) ou utilisez l' [extension VSTS d’API de soumission](https://github.com/Microsoft/windows-dev-center-vsts-extension) Open source pour commencer.

## Utiliser le hub de commentaires Windows pour recueillir les commentaires/avis/demandes de fonctionnalité

Vous pouvez rediriger les utilisateurs vers la sous-catégorie du Hub de commentaires Windows pour votre extension en incorporant un lien vers celui-ci. Ce lien doit être créé en utilisant le format suivant: 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Vous devez remplacer `<PFN>` par le nom de la famille de packages de votre extension. Pour plus d’informations, consultez la section identité de l' **application** pour votre extension dans le centre de développement Windows.

## Consulter vos évaluations et avis

Connectez-vous régulièrement pour vérifier les évaluations de vos utilisateurs. Même si l’application UWP n’aura de renseignements sur le marché de l’utilisateur actuel, la connexion au centre de développement Windows affichera le classement moyenne sur tous les marchés.

## Répondre aux avis des utilisateurs

Dans le tableau de bord du centre de développement Windows, vous pouvez répondre aux avis des utilisateurs dans Microsoft Store. Accédez à votre extension, puis sous analyse, sélectionnez **avis**. Un lien s’affiche sous chaque avis qui vous permettra de répondre directement au client. Ce canal de communication vous permet d’envoyer des commentaires, des résolutions ou de vous envoyer des remerciements pour votre avis.

![Envoi d’une réponse à un avis](./media/reviews.png)
