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
# <a name="tips-and-tricks"></a><span data-ttu-id="95b13-104">Conseils et astuces</span><span class="sxs-lookup"><span data-stu-id="95b13-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="95b13-105">Que vous travailliez actuellement sur une extension Microsoft Edge ou que vous en avez déjà publié une, les conseils et astuces suivants peuvent vous être utiles.</span><span class="sxs-lookup"><span data-stu-id="95b13-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a><span data-ttu-id="95b13-106">Obtenir un lien direct vers votre extension dans le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="95b13-106">Get a direct link to your extension in the Microsoft Store</span></span>  

<span data-ttu-id="95b13-107">Dans le tableau de bord du Centre de dév. Windows, vous trouverez un lien direct vers votre extension dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="95b13-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span>  <span data-ttu-id="95b13-108">Ce lien peut être utile pour la publicité et le partage de votre extension.</span><span class="sxs-lookup"><span data-stu-id="95b13-108">This link can be useful for advertising and sharing out your extension.</span></span>  

<span data-ttu-id="95b13-109">Une fois la connexion au Centre de dév. Windows et la navigation vers votre extension via le tableau de bord, sur la page Identité de l’application, vous trouverez le lien dans la ligne de lien de protocole du **Windows Store** :</span><span class="sxs-lookup"><span data-stu-id="95b13-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>  

![lien de protocole store](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a><span data-ttu-id="95b13-111">Assurez-vous que vous êtes en train de suivre la stratégie du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="95b13-111">Make sure you’re following the Microsoft Store Policy</span></span>  

<span data-ttu-id="95b13-112">Lorsque vous créez votre extension, veillez à garder à l’esprit les instructions d’envoi au Microsoft Store mises en évidence dans la stratégie [du Microsoft Store.](/windows/uwp/publish/store-policies)</span><span class="sxs-lookup"><span data-stu-id="95b13-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](/windows/uwp/publish/store-policies).</span></span>  
 
<span data-ttu-id="95b13-113">Les extensions Microsoft Edge ont également un ensemble supplémentaire de stratégies à [suivre.](/windows/uwp/publish/store-policies#pol_10_12)</span><span class="sxs-lookup"><span data-stu-id="95b13-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](/windows/uwp/publish/store-policies#pol_10_12).</span></span>  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a><span data-ttu-id="95b13-114">Améliorer la découverte de votre extension dans le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="95b13-114">Improve your extension’s discoverability in the Microsoft Store</span></span>  

<span data-ttu-id="95b13-115">Vous pouvez ajouter des mots clés à votre envoi d’extension pour améliorer sa découverte par le biais de recherches.</span><span class="sxs-lookup"><span data-stu-id="95b13-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span>  <span data-ttu-id="95b13-116">Par exemple, `Microsoft Edge Extensions` et `name of my extension` .</span><span class="sxs-lookup"><span data-stu-id="95b13-116">For example, `Microsoft Edge Extensions` and `name of my extension`.</span></span>  

<span data-ttu-id="95b13-117">Vous pouvez le faire dans le Centre de dév. Windows sous la section description de votre extension.</span><span class="sxs-lookup"><span data-stu-id="95b13-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span>  <span data-ttu-id="95b13-118">Ces mots clés doivent être ajoutés pour chaque langue que votre extension prend en charge.</span><span class="sxs-lookup"><span data-stu-id="95b13-118">These keywords will need to be added for every language your extension supports.</span></span>  

![Utiliser des mots clés pour envoyer une réponse à un avis](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a><span data-ttu-id="95b13-120">Automatiser votre soumission au Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="95b13-120">Automate your submission to the Microsoft Store</span></span>  

<span data-ttu-id="95b13-121">Vous pouvez automatiser et rationaliser vos soumissions au Microsoft Store à l’aide de la nouvelle API de soumission au Microsoft Store, qui vous permet de mettre à jour les applications/jeux, les modules supplémentaires \(achats dans l’application\) et les version d’essai de package via une API REST.</span><span class="sxs-lookup"><span data-stu-id="95b13-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons \(in-app purchases\), and package flights through a REST API.</span></span>  <span data-ttu-id="95b13-122">Consultez la [documentation et les exemples ou](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) utilisez l’extension [VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) de l’API de soumission open source pour commencer.</span><span class="sxs-lookup"><span data-stu-id="95b13-122">Check out the [documentation and samples](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a><span data-ttu-id="95b13-123">Utiliser le Hub de commentaires Windows pour recueillir des commentaires/avis/demandes de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="95b13-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>  

<span data-ttu-id="95b13-124">Vous pouvez diriger les utilisateurs vers la sous-catégorie du Hub de commentaires Windows pour votre extension en insérez un lien qui pointe vers celle-ci.</span><span class="sxs-lookup"><span data-stu-id="95b13-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span>  <span data-ttu-id="95b13-125">Ce lien doit être créé au format suivant :</span><span class="sxs-lookup"><span data-stu-id="95b13-125">This link will need to be created using the following format:</span></span>  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="95b13-126">Vous devrez remplacer votre extension par le nom de `<PFN>` la famille de packages.</span><span class="sxs-lookup"><span data-stu-id="95b13-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span>  <span data-ttu-id="95b13-127">Vous pouvez le trouver dans la section **Identité de** l’application pour votre extension dans le Centre de dév. Windows.</span><span class="sxs-lookup"><span data-stu-id="95b13-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>  

## <a name="check-out-your-ratings-and-reviews"></a><span data-ttu-id="95b13-128">Consulter vos évaluations et avis</span><span class="sxs-lookup"><span data-stu-id="95b13-128">Check out your ratings and reviews</span></span>  

<span data-ttu-id="95b13-129">Connectez-vous régulièrement pour vérifier les avis et évaluations de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="95b13-129">Log in regularly to check your user reviews and ratings.</span></span>  <span data-ttu-id="95b13-130">Bien que l’application UWP ne présente que des informations sur le marché des utilisateurs actuel, la connexion au Centre de dév. Windows affiche l’évaluation moyenne sur tous les marchés.</span><span class="sxs-lookup"><span data-stu-id="95b13-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>  

## <a name="respond-to-user-reviews"></a><span data-ttu-id="95b13-131">Répondre aux avis des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="95b13-131">Respond to user reviews</span></span>  

<span data-ttu-id="95b13-132">Vous pouvez répondre aux avis des utilisateurs dans le Microsoft Store via le tableau de bord du Centre de dév. Windows.</span><span class="sxs-lookup"><span data-stu-id="95b13-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span>  <span data-ttu-id="95b13-133">Accédez à votre extension et sous Analyse, sélectionnez **Avis.**</span><span class="sxs-lookup"><span data-stu-id="95b13-133">Navigate to your extension and under Analytics select **Reviews**.</span></span>  <span data-ttu-id="95b13-134">Un lien s’affiche sous chaque avis pour vous permettre de répondre directement au client.</span><span class="sxs-lookup"><span data-stu-id="95b13-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span>  <span data-ttu-id="95b13-135">Ce canal de communication vous permet de nous faire part de vos commentaires, de vos résolutions ou d’envoyer un message de merci pour l’avis.</span><span class="sxs-lookup"><span data-stu-id="95b13-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>  

![Répondre à l’avis de l’utilisateur](./media/reviews.png)  
