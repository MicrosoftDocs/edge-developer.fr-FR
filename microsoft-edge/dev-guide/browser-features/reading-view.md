---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Découvrez comment Microsoft Edge fournit un mode lecture pour les pages Web pour permettre la lecture de la version sans ajouter.
title: Mode de lecture-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: 0d2076a63f97ecf2b4699795b0036736d0f95c9c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941999"
---
# <span data-ttu-id="59910-104">Mode Lecture</span><span class="sxs-lookup"><span data-stu-id="59910-104">Reading view</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="59910-105">Microsoft Edge fournit un mode lecture pour une connaissance plus rationalisée et plus agréable de la lecture de pages Web, sans la distraction de contenus non liés ou secondaires sur la page.</span><span class="sxs-lookup"><span data-stu-id="59910-105">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="59910-106">Le mode lecture peut être activé ou désactivé à partir du bouton **lecture** \ (icône du livre \) sur la barre d’adresse ou avec `Ctrl` + `Shift` + `R` .</span><span class="sxs-lookup"><span data-stu-id="59910-106">Reading view can be toggled on or off from the **Reading view** \(book icon\) button on the address bar or with `Ctrl`+`Shift`+`R`.</span></span>  <span data-ttu-id="59910-107">Le mode lecture extrait les métadonnées suivantes d’une page:</span><span class="sxs-lookup"><span data-stu-id="59910-107">Reading view extracts the following metadata from a page:</span></span>  

*   <span data-ttu-id="59910-108">Title</span><span class="sxs-lookup"><span data-stu-id="59910-108">Title</span></span>
*   <span data-ttu-id="59910-109">Auteur</span><span class="sxs-lookup"><span data-stu-id="59910-109">Author</span></span>
*   <span data-ttu-id="59910-110">Date</span><span class="sxs-lookup"><span data-stu-id="59910-110">Date</span></span>
*   <span data-ttu-id="59910-111">Éditeur</span><span class="sxs-lookup"><span data-stu-id="59910-111">Publisher</span></span>
*   <span data-ttu-id="59910-112">Image dominante (s \)</span><span class="sxs-lookup"><span data-stu-id="59910-112">Dominant image\(s\)</span></span>
*   <span data-ttu-id="59910-113">Légendes de l’image dominante (s \)</span><span class="sxs-lookup"><span data-stu-id="59910-113">Captions of dominant image\(s\)</span></span>
*   <span data-ttu-id="59910-114">Images secondaires</span><span class="sxs-lookup"><span data-stu-id="59910-114">Secondary images</span></span>
*   <span data-ttu-id="59910-115">Contenu du texte principal de la page</span><span class="sxs-lookup"><span data-stu-id="59910-115">Main text content of the page</span></span>
*   <span data-ttu-id="59910-116">Copyright</span><span class="sxs-lookup"><span data-stu-id="59910-116">Copyright</span></span>

<span data-ttu-id="59910-117">Les utilisateurs peuvent ensuite ajuster le contraste de la page et la taille de police à partir du panneau **paramètres** de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="59910-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>  

## <span data-ttu-id="59910-118">Extraction de métadonnées</span><span class="sxs-lookup"><span data-stu-id="59910-118">Metadata extraction</span></span>  

<span data-ttu-id="59910-119">Voici les détails des métadonnées de page rendues en mode lecture.</span><span class="sxs-lookup"><span data-stu-id="59910-119">Here are details of the page metadata rendered by reading view.</span></span>  

### <span data-ttu-id="59910-120">Title</span><span class="sxs-lookup"><span data-stu-id="59910-120">Title</span></span>  

<span data-ttu-id="59910-121">Pour vous assurer que le mode lecture restitue le titre de votre article, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="59910-121">To ensure Reading view renders your article's title:</span></span>  

*   <span data-ttu-id="59910-122">Inclure un `title` élément dans votre en-tête</span><span class="sxs-lookup"><span data-stu-id="59910-122">Include a `title` element in your header</span></span>  
*   <span data-ttu-id="59910-123">Ajoutez une balise Meta avec</span><span class="sxs-lookup"><span data-stu-id="59910-123">Include a meta tag with</span></span> `name="title"`  
*   <span data-ttu-id="59910-124">Faites correspondre le texte du titre dans votre corps d’article à la chaîne de contenu de votre balise meta.</span><span class="sxs-lookup"><span data-stu-id="59910-124">Match the title text in your article body with the content string of your meta tag.</span></span>  <span data-ttu-id="59910-125">Les canaux \ ( `|` \) dans votre chaîne de contenu empêchent l’affichage du lecteur de lire le contenu, essayez d’utiliser des tirets \ ( `-` \) à la place.</span><span class="sxs-lookup"><span data-stu-id="59910-125">Pipes \(`|`\) in your content string prevent the reader view from becoming active, try using hyphens \(`-`\) instead.</span></span>  

### <span data-ttu-id="59910-126">Auteur</span><span class="sxs-lookup"><span data-stu-id="59910-126">Author</span></span>  

<span data-ttu-id="59910-127">Le mode lecture va chercher un élément avec `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="59910-127">Reading View will look for an element with `class = "byline-name"`.</span></span>  <span data-ttu-id="59910-128">Meilleure pratique consiste à placer le nom de l’auteur après le titre et le corps de l’article.</span><span class="sxs-lookup"><span data-stu-id="59910-128">Best practice is to place the author name after the title and before the article body.</span></span>  

```html
<div class="byline-name">Author name</div>
```  

### <span data-ttu-id="59910-129">Date</span><span class="sxs-lookup"><span data-stu-id="59910-129">Date</span></span>  

<span data-ttu-id="59910-130">Le mode lecture permet d’afficher les informations relatives à l’éditeur et la date sur la même ligne, grâce à un autre style de mise en surbrillance des informations.</span><span class="sxs-lookup"><span data-stu-id="59910-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span>  <span data-ttu-id="59910-131">La date de publication de l’article s’affiche exactement telle qu’elle apparaît dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="59910-131">The article's publishing date will render exactly as it appears in the string.</span></span>  <span data-ttu-id="59910-132">Le mode lecture n’est pas converti dans un format de date spécifique.</span><span class="sxs-lookup"><span data-stu-id="59910-132">Reading view does not convert to a specific date format.</span></span>  

<span data-ttu-id="59910-133">Si vous avez une date dans votre corps d’article et que vous voulez que le mode lecture le rende, assignez l’élément contenant la date au sein de la classe `'dateline'` :</span><span class="sxs-lookup"><span data-stu-id="59910-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

<span data-ttu-id="59910-134">Si vous n’avez pas de date dans le corps de l’article mais souhaitez que le mode lecture effectue le rendu de la date, utilisez la balise meta `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="59910-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### <span data-ttu-id="59910-135">Éditeur</span><span class="sxs-lookup"><span data-stu-id="59910-135">Publisher</span></span>  

<span data-ttu-id="59910-136">Le mode lecture va chercher le protocole Open Graph `"og:site_name"` pour afficher les informations de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="59910-136">Reading view will look for the Open Graph protocol `"og:site_name"` to render the publisher information.</span></span>  <span data-ttu-id="59910-137">Il recherche également les `source_organization` `publisher` attributs et dans n’importe quelle balise HTML en tant qu’indicateur secondaire des informations de l’éditeur dans la page.</span><span class="sxs-lookup"><span data-stu-id="59910-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span>  <span data-ttu-id="59910-138">Le texte de l’éditeur est lié à l’URL de la page à l’aide du style de lien hypertexte de la page du mode lecture.</span><span class="sxs-lookup"><span data-stu-id="59910-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### <span data-ttu-id="59910-139">Images</span><span class="sxs-lookup"><span data-stu-id="59910-139">Images</span></span>  

<span data-ttu-id="59910-140">Le mode lecture capture la plupart des images brutes avec la largeur >= 400px et les proportions >= 1/3 et =< 3,0.</span><span class="sxs-lookup"><span data-stu-id="59910-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span>  <span data-ttu-id="59910-141">Les images qui ne satisfont pas ces dimensions peuvent toujours être extraites, telles que les images dont la taille est inférieure à 400px, mais qui comportent des sous-titres.</span><span class="sxs-lookup"><span data-stu-id="59910-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span>  <span data-ttu-id="59910-142">La première image éligible devient l’image dominante de l’article.</span><span class="sxs-lookup"><span data-stu-id="59910-142">The first eligible image becomes the dominant image of the article.</span></span>  <span data-ttu-id="59910-143">L’image dominante est restituée en tant que première partie du contenu et en fonction de la largeur de colonne complète.</span><span class="sxs-lookup"><span data-stu-id="59910-143">The dominant image is rendered as the first piece of content and given full column width.</span></span>  <span data-ttu-id="59910-144">Toutes les images suivantes sont rendues en tant qu’images incorporées dans l’article.</span><span class="sxs-lookup"><span data-stu-id="59910-144">All following images are rendered as inline images within the article.</span></span>  

### <span data-ttu-id="59910-145">Légendes</span><span class="sxs-lookup"><span data-stu-id="59910-145">Captions</span></span>  

<span data-ttu-id="59910-146">Il est recommandé de placer les images dans les balises de [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) avec au moins deux balises [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) imbriquées.</span><span class="sxs-lookup"><span data-stu-id="59910-146">Best practice is to place images in [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) tags with no more than two nested [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) tags.</span></span>  

### <span data-ttu-id="59910-147">Body</span><span class="sxs-lookup"><span data-stu-id="59910-147">Body</span></span>  

<span data-ttu-id="59910-148">Pour vous assurer que tout le texte de la page est capturé par le mode lecture, il est recommandé de conserver la même taille de la police et la même profondeur DOM.</span><span class="sxs-lookup"><span data-stu-id="59910-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span>  <span data-ttu-id="59910-149">L’algorithme du mode lecture permet d’obtenir un certain écart par rapport à cette règle, de sorte que les éditeurs puissent être libres de mettre l’accent sur des lignes ou des mots.</span><span class="sxs-lookup"><span data-stu-id="59910-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>  

### <span data-ttu-id="59910-150">Copyright</span><span class="sxs-lookup"><span data-stu-id="59910-150">Copyright</span></span>  

<span data-ttu-id="59910-151">Le mode lecture extrait et affiche les informations de Copyright signalées par des balises meta avec `name = "copyright"` , ou s’il n’existe aucune information de méta-indicateur, un nœud de texte contenant le symbole Copyright \ ( `©` \).</span><span class="sxs-lookup"><span data-stu-id="59910-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright \(`©`\) symbol.</span></span>  <span data-ttu-id="59910-152">Le mode lecture affiche les informations de Copyright à la fin de l’article principal de l’article, dont le style est inférieur à celui du corps de texte principal.</span><span class="sxs-lookup"><span data-stu-id="59910-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>  

```html
<meta name="copyright" content="Your copyright information">
```  

## <span data-ttu-id="59910-153">Désactivation du mode lecture</span><span class="sxs-lookup"><span data-stu-id="59910-153">Opting out of Reading View</span></span>  

<span data-ttu-id="59910-154">Si vous pensez que votre contenu n’est pas adapté au mode lecture, vous pouvez utiliser la balise Meta suivante pour désactiver cette fonctionnalité:</span><span class="sxs-lookup"><span data-stu-id="59910-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>  

```html
<meta name="IE_RM_OFF" content="true">
```  

<span data-ttu-id="59910-155">Avec cette balise, le bouton **mode lecture** ne s’affiche pas dans la barre d’adresses lorsque les utilisateurs affichent votre page.</span><span class="sxs-lookup"><span data-stu-id="59910-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>  
