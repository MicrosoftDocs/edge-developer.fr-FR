---
description: Rendez votre extension accessible pour différentes langues et testez vos chaînes de langue grâce au Guide d’internationalisation.
title: Extensions-internationalisation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565333"
---
# <span data-ttu-id="cb166-104">Internationalisation</span><span class="sxs-lookup"><span data-stu-id="cb166-104">Internationalization</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="cb166-105">Pour rendre votre extension accessible à un large éventail de personnes, il est important de développer en même tant que d’autres pays.</span><span class="sxs-lookup"><span data-stu-id="cb166-105">In order to make your extension accessible to a variety of different people, it is important to develop with other countries in mind.</span></span> <span data-ttu-id="cb166-106">Les extensions Microsoft Edge vous permettent d’ajouter différentes chaînes de langue à vos extensions de sorte que leur langue puisse être facilement modifiée.</span><span class="sxs-lookup"><span data-stu-id="cb166-106">Microsoft Edge extensions allows you to add different language strings to your extensions so that their language can easily be changed.</span></span>

<span data-ttu-id="cb166-107">Pour en savoir plus sur la mise en international de votre poste, consultez le [Guide international](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)MDN.</span><span class="sxs-lookup"><span data-stu-id="cb166-107">For more information on internationalizing your extension, check out MDN's [Internationalization guide](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization).</span></span>


## <span data-ttu-id="cb166-108">Langues de test</span><span class="sxs-lookup"><span data-stu-id="cb166-108">Testing languages</span></span>

<span data-ttu-id="cb166-109">Pour tester vos chaînes de langue, vous devez d’abord définir la langue d’affichage de Windows sur celle que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="cb166-109">To test your language strings, you first need to set the Windows display language to the language that you want to test for.</span></span>

<span data-ttu-id="cb166-110">Pour modifier la langue d’affichage de Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="cb166-110">Follow the steps below to change the Windows display language:</span></span>

1. <span data-ttu-id="cb166-111">Ouvrez l’application paramètres.</span><span class="sxs-lookup"><span data-stu-id="cb166-111">Open the Settings app.</span></span>

   ![application paramètres](./../media/loc-settings.png)
2. <span data-ttu-id="cb166-113">Sélectionnez «heure & langue».</span><span class="sxs-lookup"><span data-stu-id="cb166-113">Select "Time & language".</span></span>
3. <span data-ttu-id="cb166-114">Sélectionnez «région & langue».</span><span class="sxs-lookup"><span data-stu-id="cb166-114">Select "Region & language".</span></span>
4. <span data-ttu-id="cb166-115">Sélectionnez "+ ajouter une langue" pour ajouter la langue à la liste de langues possibles.</span><span class="sxs-lookup"><span data-stu-id="cb166-115">Select "+ Add a language" to add the language to the list of possible languages.</span></span>
5. <span data-ttu-id="cb166-116">Dans la liste «langues», choisissez la langue que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="cb166-116">Choose the language from the "Languages" list that you want to test.</span></span>
6. <span data-ttu-id="cb166-117">Sélectionnez le bouton «définir par défaut» (il est possible que vous deviez redémarrer votre PC).</span><span class="sxs-lookup"><span data-stu-id="cb166-117">Select the "Set as default" button (you may need to restart your PC).</span></span>
7. <span data-ttu-id="cb166-118">Ouvrez Microsoft Edge et vérifiez que les chaînes définies pour les paramètres régionaux apparaissent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="cb166-118">Open Microsoft Edge and verify that the strings defined for the locale appear as expected.</span></span>

<span data-ttu-id="cb166-119">À l’aide de la propriété [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) , vous pouvez vérifier que la langue Microsoft Edge est déterminée comme étant correcte.</span><span class="sxs-lookup"><span data-stu-id="cb166-119">By using the [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) property, you can verify that the language Microsoft Edge has determined to be the Windows display language is correct.</span></span>

<span data-ttu-id="cb166-120">Cliquez sur le bouton dans le CodePen ci-dessous pour afficher la langue d’affichage de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cb166-120">Click the button in the CodePen below to see the display language of your browser.</span></span>

<iframe height='300' scrolling='no' title='<span data-ttu-id="cb166-121">Obtention des paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="cb166-121">Get locale</span></span>' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="cb166-122"><a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> </a> Pour plus d’MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='http://codepen.io'> CodePen </a> , voir Pen Get.</span><span class="sxs-lookup"><span data-stu-id="cb166-122">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'>Get locale</a>by MSEdgeDev (<a href='http://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span>
</iframe>
