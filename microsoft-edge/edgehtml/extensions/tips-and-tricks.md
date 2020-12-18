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
# <span data-ttu-id="4c872-104">Conseils et astuces</span><span class="sxs-lookup"><span data-stu-id="4c872-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="4c872-105">Si vous travaillez actuellement sur une extension Microsoft Edge ou si vous avez déjà publié une extension, les conseils et astuces suivants peuvent être utiles.</span><span class="sxs-lookup"><span data-stu-id="4c872-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>

## <span data-ttu-id="4c872-106">Obtenir un lien direct vers votre extension dans le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="4c872-106">Get a direct link to your extension in the Microsoft Store</span></span>

<span data-ttu-id="4c872-107">Le tableau de bord du centre de développement Windows vous permet de trouver un lien direct vers votre extension dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="4c872-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span> <span data-ttu-id="4c872-108">Ce lien peut être utile pour publier et partager votre extension.</span><span class="sxs-lookup"><span data-stu-id="4c872-108">This link can be useful for advertising and sharing out your extension.</span></span>

<span data-ttu-id="4c872-109">Après vous être connecté au centre de développement Windows et avoir navigué vers votre extension via le tableau de bord, dans la page identité de l’application, vous trouverez le lien dans la ligne **lier le protocole Store** :</span><span class="sxs-lookup"><span data-stu-id="4c872-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>

![lien vers le protocole Store](./media/store-link.png)
 
## <span data-ttu-id="4c872-111">Vérifiez que vous suivez la politique du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="4c872-111">Make sure you’re following the Microsoft Store Policy</span></span>

<span data-ttu-id="4c872-112">Lorsque vous créez votre extension, veillez à garder à l’esprit les recommandations en matière de soumission à la boutique Microsoft en surbrillance dans la [politique Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c872-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span></span> 
 
<span data-ttu-id="4c872-113">Les extensions Microsoft Edge disposent également d’un ensemble supplémentaire de stratégies à [suivre.](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)</span><span class="sxs-lookup"><span data-stu-id="4c872-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span>

## <span data-ttu-id="4c872-114">Améliorer la détectabilité de votre extension dans la boutique Microsoft</span><span class="sxs-lookup"><span data-stu-id="4c872-114">Improve your extension’s discoverability in the Microsoft Store</span></span>

<span data-ttu-id="4c872-115">Vous pouvez ajouter des mots clés à votre soumission d’extension pour améliorer sa détectabilité par le biais de recherches.</span><span class="sxs-lookup"><span data-stu-id="4c872-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span> <span data-ttu-id="4c872-116">Par exemple, «Microsoft Edge extensions» et «nom de mon extension».</span><span class="sxs-lookup"><span data-stu-id="4c872-116">For example, "Microsoft Edge Extensions" and "name of my extension".</span></span> 

<span data-ttu-id="4c872-117">Pour cela, vous pouvez effectuer cette opération dans le centre de développement Windows, sous la section Description de votre extension.</span><span class="sxs-lookup"><span data-stu-id="4c872-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span> <span data-ttu-id="4c872-118">Vous devrez ajouter ces mots clés pour chaque langue prise en charge par votre extension.</span><span class="sxs-lookup"><span data-stu-id="4c872-118">These keywords will need to be added for every language your extension supports.</span></span>

![Envoyer une réponse à un avis-Keywords](./media/keywords.png)

## <span data-ttu-id="4c872-120">Automatiser votre soumission sur le Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="4c872-120">Automate your submission to the Microsoft Store</span></span>

<span data-ttu-id="4c872-121">Vous pouvez automatiser et rationaliser vos soumissions du Microsoft Store à l’aide de la nouvelle API de soumission du Windows Store, qui vous permet de mettre à jour les applications/jeux, les modules complémentaires (achats dans l’application) et les versions d’évaluation de package via une API REST.</span><span class="sxs-lookup"><span data-stu-id="4c872-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons (in-app purchases), and package flights through a REST API.</span></span> <span data-ttu-id="4c872-122">Consultez la [documentation et les exemples,](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) ou utilisez l' [extension VSTS d’API de soumission](https://github.com/Microsoft/windows-dev-center-vsts-extension) Open source pour commencer.</span><span class="sxs-lookup"><span data-stu-id="4c872-122">Check out the [documentation and samples](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>

## <span data-ttu-id="4c872-123">Utiliser le hub de commentaires Windows pour recueillir les commentaires/avis/demandes de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="4c872-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>

<span data-ttu-id="4c872-124">Vous pouvez rediriger les utilisateurs vers la sous-catégorie du Hub de commentaires Windows pour votre extension en incorporant un lien vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4c872-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span> <span data-ttu-id="4c872-125">Ce lien doit être créé en utilisant le format suivant:</span><span class="sxs-lookup"><span data-stu-id="4c872-125">This link will need to be created using the following format:</span></span> 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="4c872-126">Vous devez remplacer `<PFN>` par le nom de la famille de packages de votre extension.</span><span class="sxs-lookup"><span data-stu-id="4c872-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span> <span data-ttu-id="4c872-127">Pour plus d’informations, consultez la section identité de l' **application** pour votre extension dans le centre de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="4c872-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>

## <span data-ttu-id="4c872-128">Consulter vos évaluations et avis</span><span class="sxs-lookup"><span data-stu-id="4c872-128">Check out your ratings and reviews</span></span>

<span data-ttu-id="4c872-129">Connectez-vous régulièrement pour vérifier les évaluations de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4c872-129">Log in regularly to check your user reviews and ratings.</span></span> <span data-ttu-id="4c872-130">Même si l’application UWP n’aura de renseignements sur le marché de l’utilisateur actuel, la connexion au centre de développement Windows affichera le classement moyenne sur tous les marchés.</span><span class="sxs-lookup"><span data-stu-id="4c872-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>

## <span data-ttu-id="4c872-131">Répondre aux avis des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4c872-131">Respond to user reviews</span></span>

<span data-ttu-id="4c872-132">Dans le tableau de bord du centre de développement Windows, vous pouvez répondre aux avis des utilisateurs dans Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="4c872-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span> <span data-ttu-id="4c872-133">Accédez à votre extension, puis sous analyse, sélectionnez **avis**.</span><span class="sxs-lookup"><span data-stu-id="4c872-133">Navigate to your extension and under Analytics select **Reviews**.</span></span> <span data-ttu-id="4c872-134">Un lien s’affiche sous chaque avis qui vous permettra de répondre directement au client.</span><span class="sxs-lookup"><span data-stu-id="4c872-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span> <span data-ttu-id="4c872-135">Ce canal de communication vous permet d’envoyer des commentaires, des résolutions ou de vous envoyer des remerciements pour votre avis.</span><span class="sxs-lookup"><span data-stu-id="4c872-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>

![Envoi d’une réponse à un avis](./media/reviews.png)
