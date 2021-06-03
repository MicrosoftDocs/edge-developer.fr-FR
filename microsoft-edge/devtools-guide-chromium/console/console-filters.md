---
description: Découvrez comment filtrer les messages de la console
title: Commencer à filtrer des messages dans la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b493bb790b48bc1c4dca0e6802d2f638099b7644
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483429"
---
# <a name="filter-console-messages"></a><span data-ttu-id="6a2d9-104">Filtrer les messages de la console</span><span class="sxs-lookup"><span data-stu-id="6a2d9-104">Filter Console messages</span></span>  

<span data-ttu-id="6a2d9-105">Lorsque vous naviguez sur le web, il se peut que vous trouviez que la **console** est submergée de toutes sortes d’informations.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-105">When you surf the web, you may find the **Console** is flooded with all kinds of information.</span></span>  <span data-ttu-id="6a2d9-106">Souvent, les informations ne sont pas pertinentes pour vous.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-106">Often the information isn't relevant to you.</span></span>  <span data-ttu-id="6a2d9-107">Telles que des informations sur le projet en direct qu’un autre développeur a journalisé pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-107">Such as information about the live project that another developer logged while you debug.</span></span>  <span data-ttu-id="6a2d9-108">Ou plus d’informations sur les violations et avertissements concernant les performances du site actuel que vous ne pouvez pas modifier.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-108">Or more information about violations and warnings about the performance of the current site that you aren't able to change.</span></span>  <span data-ttu-id="6a2d9-109">Il est logique d’utiliser les options de filtre de **console** pour réduire le bruit.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-109">It makes sense to use the filter options of **Console** to reduce the noise.</span></span>  

## <a name="filter-by-log-level"></a><span data-ttu-id="6a2d9-110">Filtrer par niveau de journal</span><span class="sxs-lookup"><span data-stu-id="6a2d9-110">Filter by log level</span></span>  

<span data-ttu-id="6a2d9-111">Chaque méthode de l’objet est attachée à un niveau `console` de gravité.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-111">Each method of the `console` object has a severity level attached to it.</span></span>  <span data-ttu-id="6a2d9-112">Les niveaux de gravité `Verbose` sont `Info` , ou `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="6a2d9-112">The severity levels are `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="6a2d9-113">Affichez les niveaux de gravité dans la [documentation de l’API.][DevtoolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="6a2d9-113">Display the severity levels in the [API documentation][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="6a2d9-114">Par exemple, `console.log()` il s’agit `Info` d’un message de niveau -level, mais `console.error()` `Error` d’un message de niveau -.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-114">For example, `console.log()` is an `Info`-level message, but `console.error()` is an `Error`-level message.</span></span>  

<span data-ttu-id="6a2d9-115">Pour filtrer des messages dans **la console,** utilisez **le** menu déroulant Niveau journal.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-115">To filter messages in the **Console**, use the **Log Level** dropdown menu.</span></span>  <span data-ttu-id="6a2d9-116">Vous pouvez faire bascule l’état de chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-116">You may toggle the state of each level.</span></span>  <span data-ttu-id="6a2d9-117">Pour désactiver chaque niveau, supprimez la coche en regard de chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-117">To turn off each level, remove the checkmark next to each.</span></span>  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="Le menu déroulant filtre les messages de la console à l’aide du niveau de journal" lightbox="../media/console-filter-dropdown.msft.png":::
    <span data-ttu-id="6a2d9-119">Le menu déroulant filtre les messages **de la console** à l’aide du niveau de journal</span><span class="sxs-lookup"><span data-stu-id="6a2d9-119">The dropdown menu filters **Console** messages using the log level</span></span>  
:::image-end:::  

<span data-ttu-id="6a2d9-120">Étant donné qu’aucun filtre n’est appliqué, la figure suivante affiche des dizaines de messages.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-120">Since no filter is applied, the following figure displays dozens of messages.</span></span>  <span data-ttu-id="6a2d9-121">Ensuite, réduisez et gérez le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-121">Next, reduce and manage the number of messages.</span></span>  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Aucun ensemble de filtres signifie que vous pouvez afficher de nombreux messages de console" lightbox="../media/console-filter-displays-all.msft.png":::
    <span data-ttu-id="6a2d9-123">Aucun ensemble de filtres signifie que vous pouvez afficher de nombreux messages de console</span><span class="sxs-lookup"><span data-stu-id="6a2d9-123">No filter set means you may display many console messages</span></span>  
:::image-end:::  

<span data-ttu-id="6a2d9-124">Choisissez de masquer tous les messages de niveau Avertissement pour réduire le bruit.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-124">Choose to hide all the Warning-level messages to cut down on the noise.</span></span>  <span data-ttu-id="6a2d9-125">Accédez à la dropdown **Log Levels** et décochez le `Warnings` niveau.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-125">Navigate to the **Log Levels** dropdown and uncheck the `Warnings` level.</span></span>  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Masquer tous les messages de niveau d’avertissement dans la console pour filtrer une grande partie du bruit" lightbox="../media/console-filter-hide-warning.msft.png":::
    <span data-ttu-id="6a2d9-127">Masquer tous les messages de niveau d’avertissement dans la **console** pour filtrer une grande partie du bruit</span><span class="sxs-lookup"><span data-stu-id="6a2d9-127">Hide all the warning level messages in the **Console** to filter much of the noise</span></span>  
:::image-end:::  

## <a name="filter-by-text"></a><span data-ttu-id="6a2d9-128">Filtrer par texte</span><span class="sxs-lookup"><span data-stu-id="6a2d9-128">Filter by text</span></span>  

<span data-ttu-id="6a2d9-129">Si vous souhaitez examiner plus en détail, pour filtrer les messages à l’aide de texte, tapez une chaîne dans la **boîte de** texte Filtrer.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-129">If you want to review more detail, to filter messages using text, type a string into the **Filter** textbox.</span></span>  <span data-ttu-id="6a2d9-130">Par exemple, tapez dans la zone pour afficher uniquement les messages concernant le chargement des ressources de blocage `block` du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-130">For example, type `block` into the box to only display your messages about the browser blocking resources from loading.</span></span>

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Affiche les messages qui contiennent le bloc de mots" lightbox="../media/console-filter-text.msft.png":::
    <span data-ttu-id="6a2d9-132">Affiche les messages qui contiennent le mot</span><span class="sxs-lookup"><span data-stu-id="6a2d9-132">Displays the messages that contain the word</span></span> `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a><span data-ttu-id="6a2d9-133">Filtrer par expression régulière</span><span class="sxs-lookup"><span data-stu-id="6a2d9-133">Filter by regular expression</span></span>

<span data-ttu-id="6a2d9-134">[Les expressions régulières][MdnDocsWebJavascriptGuideRegularExpressions] sont un moyen puissant de filtrer des messages.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-134">[Regular expressions][MdnDocsWebJavascriptGuideRegularExpressions] are a powerful way to filter messages.</span></span>  <span data-ttu-id="6a2d9-135">Par exemple, tapez `/^Tracking/` dans la boîte de texte **Filtrer** pour afficher uniquement les messages qui commencent par le terme `Tracking` .</span><span class="sxs-lookup"><span data-stu-id="6a2d9-135">For example, type `/^Tracking/` into the **Filter** textbox to only displays messages that start with the term `Tracking`.</span></span>  <span data-ttu-id="6a2d9-136">Si vous ne connaissez pas les expressions régulières, [RegExr][|::ref1::|Main] est une excellente ressource pour en savoir plus sur l’utilisation des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-136">If you're unfamiliar with regular expressions, [RegExr][|::ref1::|Main] is a great resource to learn about using regular expressions.</span></span>

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Affiche les messages qui commencent par le filtre word à l’aide d’une expression régulière dans la boîte de texte Filtre" lightbox="../media/console-filter-regex.msft.png":::
    <span data-ttu-id="6a2d9-138">Affiche les messages qui commencent par le mot à `filter` l’aide d’une expression régulière dans la boîte **de** texte Filtrer</span><span class="sxs-lookup"><span data-stu-id="6a2d9-138">Displays the messages that start with the word `filter` using a regular expression in the **Filter** textbox</span></span>  
:::image-end:::  

## <a name="filter-by-message-source"></a><span data-ttu-id="6a2d9-139">Filtrer par source de message</span><span class="sxs-lookup"><span data-stu-id="6a2d9-139">Filter by message source</span></span>  

<span data-ttu-id="6a2d9-140">Vous pouvez également définir le type de message à afficher et l’origine de chacun d’eux à l’aide de la barre latérale **de** la **console.**</span><span class="sxs-lookup"><span data-stu-id="6a2d9-140">You may also define what kind of messages you want to display and where each originated using the **Sidebar** of the **Console**.</span></span>  <span data-ttu-id="6a2d9-141">Pour ce faire, sélectionnez le bouton Afficher la **barre latérale de la console.**</span><span class="sxs-lookup"><span data-stu-id="6a2d9-141">To do it, choose the **Show console sidebar** button.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Pour ouvrir la barre latérale, sélectionnez l’icône Barre latérale" lightbox="../media/console-filter-sidebar-icon.msft.png":::
    <span data-ttu-id="6a2d9-143">Pour ouvrir la barre **latérale,** choisissez le bouton Afficher la **barre latérale de la console**</span><span class="sxs-lookup"><span data-stu-id="6a2d9-143">To open the **Sidebar**, choose the **Show console sidebar** button</span></span>  
:::image-end:::  

<span data-ttu-id="6a2d9-144">Lorsque la **barre latérale est** ouverte, vous pouvez afficher le nombre global de messages et l’origine de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-144">When the **Sidebar** is open, you may display the overall number of messages and where each originated.</span></span>  <span data-ttu-id="6a2d9-145">Les options sont `All messages` , , , et `User Messages` `Errors` `Warnings` `Info` `Verbose` .</span><span class="sxs-lookup"><span data-stu-id="6a2d9-145">The options are `All messages`, `User Messages`, `Errors`, `Warnings`, `Info`, and `Verbose`.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="La barre latérale de la console affiche les différentes sources d’origine des messages" lightbox="../media/console-filter-sidebar-open.msft.png":::
    <span data-ttu-id="6a2d9-147">La **barre latérale de la console** affiche les différentes sources d’origine des messages</span><span class="sxs-lookup"><span data-stu-id="6a2d9-147">The **Console Sidebar** displays the different sources messages originated from</span></span>  
:::image-end:::  

<span data-ttu-id="6a2d9-148">Choisissez l’une des options pour afficher uniquement les messages de ce type.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-148">Choose any of the options to display only the messages of that type.</span></span>  <span data-ttu-id="6a2d9-149">Par exemple, pour afficher les messages des utilisateurs, choisissez l’option de messages de l’utilisateur pour afficher moins de bruit.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-149">For example, to display user messages, choose the user messages option to display less noise.</span></span>

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Choisir d’afficher uniquement les messages utilisateur dans la console à l’aide du filtre dans la barre latérale" lightbox="../media/console-filter-select-user-messages.msft.png":::
    <span data-ttu-id="6a2d9-151">Choisir d’afficher uniquement les messages utilisateur dans la **console** à l’aide du filtre dans la **barre latérale**</span><span class="sxs-lookup"><span data-stu-id="6a2d9-151">Choose to display only user messages in the **Console** using the filter in the **Sidebar**</span></span>  
:::image-end:::  

<span data-ttu-id="6a2d9-152">Pour filtrer davantage et développer le choix, choisissez l’icône de triangle en de côté.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-152">To filter more and expand the choice, choose the triangle icon next to it.</span></span>  <span data-ttu-id="6a2d9-153">Ainsi, vous obtenez plus de choix pour afficher uniquement les messages provenant d’une source spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a2d9-153">That way you get more choices to display only messages that originate from a specific source.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Choisir l’icône de flèche développe chacune des sections" lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    <span data-ttu-id="6a2d9-155">Choisir l’icône de flèche développe chacune des sections</span><span class="sxs-lookup"><span data-stu-id="6a2d9-155">Choose the arrow icon expands each of the sections</span></span>  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Choisir l’une des nouvelles options de filtrage à l’aide du type et de la source" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    <span data-ttu-id="6a2d9-157">Choisir l’une des nouvelles options de filtrage à l’aide du type et de la source</span><span class="sxs-lookup"><span data-stu-id="6a2d9-157">Choose any of the new options to filter using type and source</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6a2d9-158">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="6a2d9-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Référence de l’API de console | Documents Microsoft"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressions régulières | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
