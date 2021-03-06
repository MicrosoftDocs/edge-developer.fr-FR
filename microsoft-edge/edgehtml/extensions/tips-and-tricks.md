---
description: Découvrez quelques conseils pratiques et astuces concernant les extensions Microsoft Edge
title: Conseils et astuces | Extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, développement web, html, css, javascript, développeur, extensions
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a5ea19152f5524d86d17d6f978c677c45f8f3a8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399350"
---
# <a name="tips-and-tricks"></a>Conseils et astuces  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Que vous travailliez actuellement sur une extension Microsoft Edge ou que vous en avez déjà publié une, les conseils et astuces suivants peuvent vous être utiles.  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a>Obtenir un lien direct vers votre extension dans le Microsoft Store  

Dans le tableau de bord du Centre de dév. Windows, vous trouverez un lien direct vers votre extension dans le Microsoft Store.  Ce lien peut être utile pour la publicité et le partage de votre extension.  

Une fois la connexion au Centre de dév. Windows et la navigation vers votre extension via le tableau de bord, sur la page Identité de l’application, vous trouverez le lien dans la ligne de lien de protocole du **Windows Store** :  

![lien de protocole store](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a>Assurez-vous que vous êtes en train de suivre la stratégie du Microsoft Store  

Lorsque vous créez votre extension, veillez à garder à l’esprit les instructions d’envoi au Microsoft Store mises en évidence dans la stratégie [du Microsoft Store.](/windows/uwp/publish/store-policies)  
 
Les extensions Microsoft Edge ont également un ensemble supplémentaire de stratégies à [suivre.](/windows/uwp/publish/store-policies#pol_10_12)  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a>Améliorer la découverte de votre extension dans le Microsoft Store  

Vous pouvez ajouter des mots clés à votre envoi d’extension pour améliorer sa découverte par le biais de recherches.  Par exemple, `Microsoft Edge Extensions` et `name of my extension` .  

Vous pouvez le faire dans le Centre de dév. Windows sous la section description de votre extension.  Ces mots clés doivent être ajoutés pour chaque langue que votre extension prend en charge.  

![Utiliser des mots clés pour envoyer une réponse à un avis](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a>Automatiser votre soumission au Microsoft Store  

Vous pouvez automatiser et rationaliser vos soumissions au Microsoft Store à l’aide de la nouvelle API de soumission au Microsoft Store, qui vous permet de mettre à jour les applications/jeux, les modules supplémentaires \(achats dans l’application\) et les version d’essai de package via une API REST.  Consultez la [documentation et les exemples ou](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) utilisez l’extension [VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) de l’API de soumission open source pour commencer.  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a>Utiliser le Hub de commentaires Windows pour recueillir des commentaires/avis/demandes de fonctionnalités  

Vous pouvez diriger les utilisateurs vers la sous-catégorie du Hub de commentaires Windows pour votre extension en insérez un lien qui pointe vers celle-ci.  Ce lien doit être créé au format suivant :  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Vous devrez remplacer votre extension par le nom de `<PFN>` la famille de packages.  Vous pouvez le trouver dans la section **Identité de** l’application pour votre extension dans le Centre de dév. Windows.  

## <a name="check-out-your-ratings-and-reviews"></a>Consulter vos évaluations et avis  

Connectez-vous régulièrement pour vérifier les avis et évaluations de vos utilisateurs.  Bien que l’application UWP ne présente que des informations sur le marché des utilisateurs actuel, la connexion au Centre de dév. Windows affiche l’évaluation moyenne sur tous les marchés.  

## <a name="respond-to-user-reviews"></a>Répondre aux avis des utilisateurs  

Vous pouvez répondre aux avis des utilisateurs dans le Microsoft Store via le tableau de bord du Centre de dév. Windows.  Accédez à votre extension et sous Analyse, sélectionnez **Avis.**  Un lien s’affiche sous chaque avis pour vous permettre de répondre directement au client.  Ce canal de communication vous permet de nous faire part de vos commentaires, de vos résolutions ou d’envoyer un message de merci pour l’avis.  

![Répondre à l’avis de l’utilisateur](./media/reviews.png)  
