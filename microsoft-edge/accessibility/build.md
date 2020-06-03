---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Découvrez comment les meilleures pratiques et les applications Internet enrichies accessibles peuvent être utilisées pour créer un site Web accessible.
title: Accessibilité-version
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibilité, accessibilité pour les développeurs, sites Web accessibles, Edge, développement Web, ARIA, développeur, UIA, UI Automation
ms.custom: seodec18
ms.openlocfilehash: 4412fef6bb78b5a393ccafd5a2cfa79aba223141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564678"
---
# <span data-ttu-id="17795-104">Créer des sites Web accessibles</span><span class="sxs-lookup"><span data-stu-id="17795-104">Building Accessible Websites</span></span>
<span data-ttu-id="17795-105">Le Web est rempli par des sites Web, des applications et des interfaces utilisateur dynamiques et complexes, développés à l’aide d’une combinaison de HTML, CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17795-105">The web is filled with dynamic and complex websites, applications, and user interfaces built using a combination of HTML, CSS, and JavaScript.</span></span>  <span data-ttu-id="17795-106">Néanmoins, lors d’une conception et d’une conception sans l’accessibilité, ces sites Web complexes sont difficiles à utiliser par les personnes qui utilisent des [technologies d’assistance](https://webaim.org/articles/motor/assistive) pour naviguer sur le Web.</span><span class="sxs-lookup"><span data-stu-id="17795-106">However, when designed and built without accessibility in mind, these complex websites are difficult to use by people who rely on [assistive technologies](https://webaim.org/articles/motor/assistive) to browse the web.</span></span> <span data-ttu-id="17795-107">La création de sites Web accessibles aux personnes atteintes de handicaps nécessite des informations sémantiques sur l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17795-107">Building websites that are accessible to people with disabilities requires semantic information about the user interface.</span></span> <span data-ttu-id="17795-108">Cela permet aux technologies d’assistance (par exemple, les lecteurs d’écran) de transmettre les informations nécessaires à des personnes atteintes de capacités d’utilisation du site Web.</span><span class="sxs-lookup"><span data-stu-id="17795-108">This allows for assistive technologies, like screen readers, to convey the necessary information to help people with a range of abilities use the website.</span></span>

<span data-ttu-id="17795-109">Consultez [HTML5Accessibility](https://html5accessibility.com) pour en savoir plus sur les nouvelles fonctionnalités HTML5 prises en charge par Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="17795-109">Visit [HTML5Accessibility](https://html5accessibility.com) for information on which new HTML5 features are accessibly supported by Microsoft Edge.</span></span>

## <span data-ttu-id="17795-110">Fonctionnement de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="17795-110">How Accessibility Works</span></span>

<span data-ttu-id="17795-111">Les technologies d’assistance permettent d’ajouter des fonctionnalités qui ne sont généralement pas disponibles sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="17795-111">Assistive technologies add capabilities that computers don't usually have.</span></span> <span data-ttu-id="17795-112">Par exemple, un utilisateur souffrant d’une déficience visuelle peut utiliser son clavier en association avec la technologie d’assistance telle qu’un lecteur d’écran, plutôt que d’utiliser directement le navigateur avec la souris et l’écran.</span><span class="sxs-lookup"><span data-stu-id="17795-112">For example, a visually impaired user might use their keyboard in combination with assistive technology such as a screen reader, rather than directly using the browser with the mouse and screen.</span></span> <span data-ttu-id="17795-113">Pour les applications sur les plates-formes Microsoft et sur le Web, la technologie d’assistance interagit avec Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), un modèle d’objet spécifique à l’application tel que le DOM (Document Object Model) dans Microsoft Edge, ou une combinaison de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="17795-113">For applications on Microsoft platforms and on the web, the assistive technology interacts with Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), an application-specific object model such as the Document Object Model (DOM) in Microsoft Edge, or a combination of these.</span></span>

<span data-ttu-id="17795-114">Pour les développeurs Web, certains éléments HTML sont mappés aux objets UI Automation, de sorte que la sélection de ces éléments HTML par le développeur peut utiliser les propriétés d’accessibilité et les événements intégrés à ces éléments.</span><span class="sxs-lookup"><span data-stu-id="17795-114">For web developers, certain HTML elements are mapped to UI Automation objects, so in selecting those HTML elements, the developer can use the accessibility properties and events built in to those elements.</span></span> <span data-ttu-id="17795-115">Lors du développement de votre site Web, il n’est généralement pas nécessaire de veiller à ce que l’API soit correctement écrite (ou que l’élément approprié soit spécifié), afin que l’application soit accessible.</span><span class="sxs-lookup"><span data-stu-id="17795-115">While developing your website, you usually only need to be concerned with ensuring that the API is correctly written to (or that the appropriate element is specified), in order for the application to be accessible.</span></span> <span data-ttu-id="17795-116">Pour plus d’informations, voir [Aria et UI Automation dans Microsoft Edge](./build/ARIA-and-UI-Automation.md) .</span><span class="sxs-lookup"><span data-stu-id="17795-116">Check out [ARIA and UI Automation in Microsoft Edge](./build/ARIA-and-UI-Automation.md) for more information.</span></span>  <span data-ttu-id="17795-117">Pour plus d’informations sur les applications de plateforme Windows universelle (UWP) accessibles, voir la rubrique [accessibilité](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) dans le centre de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="17795-117">For information on accessible Universal Windows Platform (UWP) apps, see the [Accessibility](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) topic in the Windows Dev Center.</span></span>

<span data-ttu-id="17795-118">De nombreux problèmes d’accessibilité courants liés au contenu dynamique peuvent être corrigés par de bonnes pratiques de programmation, et la documentation de [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) comporte de nombreuses techniques et meilleures pratiques pour vous aider à créer des applications Web dynamiques plus accessibles.</span><span class="sxs-lookup"><span data-stu-id="17795-118">Many common accessibility issues with dynamic content can be addressed by good coding practice, and the [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) documentation includes many techniques and best practices to help you create more accessible dynamic web applications.</span></span> <span data-ttu-id="17795-119">Même s’il est correctement codé, le contenu dynamique n’est pas nécessairement accessible.</span><span class="sxs-lookup"><span data-stu-id="17795-119">Even when coded properly, however, dynamic content is not necessarily accessible.</span></span> <span data-ttu-id="17795-120">Les [applications Internet enrichies accessibles](#aria) peuvent résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="17795-120">[Accessible Rich Internet Applications (ARIA)](#aria) helps overcome this issue.</span></span>  

<span data-ttu-id="17795-121">Pour plus d’informations sur l’accessibilité Web, consultez l’article [Présentation de](https://www.w3.org/WAI/intro/accessibility.php) l’accessibilité Web par l' [initiative de Web Accessibility](https://www.w3.org/WAI/) (WAI).</span><span class="sxs-lookup"><span data-stu-id="17795-121">For more information on web accessibility, check out the [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative](https://www.w3.org/WAI/) (WAI).</span></span>

## <span data-ttu-id="17795-122">ENRICHI</span><span class="sxs-lookup"><span data-stu-id="17795-122">ARIA</span></span>
<span data-ttu-id="17795-123">La spécification Aria ( [Rich Internet applications) accessible](https://www.w3.org/TR/wai-aria/) par l' [initiative W3C’s Web Accessibility](https://www.w3.org/WAI/) définit en tant que syntaxe pour rendre le contenu Web dynamique et les interfaces utilisateur personnalisés accessibles à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="17795-123">The [Accessible Rich Internet Applications](https://www.w3.org/TR/wai-aria/) (ARIA) specification by the W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) defines as a syntax for making dynamic web content and custom user interfaces accessible to all people.</span></span> <span data-ttu-id="17795-124">ARIA étend le code HTML à l’aide d’attributs supplémentaires (rôles, propriétés et États) conçus pour transmettre des sémantiques personnalisées.</span><span class="sxs-lookup"><span data-stu-id="17795-124">ARIA extends HTML by using additional attributes (roles, properties, and states) that are designed to convey custom semantics.</span></span> <span data-ttu-id="17795-125">Ces attributs sont utilisés par les navigateurs pour passer de l’État et du rôle de contrôles à l’API d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-125">These attributes are used by browsers to pass along the controls' state and role to the accessibility API.</span></span>

### <span data-ttu-id="17795-126">Rôles, propriétés et États</span><span class="sxs-lookup"><span data-stu-id="17795-126">Roles, Properties, and States</span></span>
<span data-ttu-id="17795-127">Les rôles ARIA sont définis sur des éléments à l’aide de l' [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribut pour fournir des informations sur les technologies d’assistance et sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="17795-127">ARIA roles are set on elements using the [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribute to give assistive technologies and accessibility APIs information about the element.</span></span> <span data-ttu-id="17795-128">Par exemple, l' `<li>` élément suivant est assigné `role="menuitem"` pour indiquer qu’il s’agit d’un élément d’un menu.</span><span class="sxs-lookup"><span data-stu-id="17795-128">For example, the below `<li>` element is assigned `role="menuitem"` to signify it's an item in a menu.</span></span>

``` html
<li role="menuitem">Home</li>
```

<span data-ttu-id="17795-129">Les États et propriétés ARIA sont des attributs prédéfinis de Aria qui fournissent des informations spécifiques sur un objet pour faciliter la définition de la nature des rôles.</span><span class="sxs-lookup"><span data-stu-id="17795-129">ARIA states and properties are aria-prefixed attributes that provide specific information about an object to help form the definition of the nature of roles.</span></span> <span data-ttu-id="17795-130">Les propriétés sont des attributs essentiels pour la nature d’un objet, par exemple [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) et [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="17795-130">Properties are attributes that are essential to the nature of an object, like [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) and [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx).</span></span> <span data-ttu-id="17795-131">Le changement de propriété affecte la signification de l’objet.</span><span class="sxs-lookup"><span data-stu-id="17795-131">Changing a property affects the meaning of the object.</span></span> <span data-ttu-id="17795-132">Dans l’exemple ci-dessous, la propriété `aria-haspopup="true"` est définie sur un `<li>` élément de menu pour signifier qu’il s’agit d’une fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="17795-132">In the example below, the property `aria-haspopup="true"` is set on a `<li>` menu item to signify it has a popup.</span></span>

``` html
<li role="menuitem" aria-haspopup="true">Open</li>
```

<span data-ttu-id="17795-133">Les États ne changent pas la nature de l’objet, mais représentent des informations associées à l’interaction de l’objet ou de l’utilisateur avec l’objet, par exemple [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) ou [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="17795-133">States do not change the nature of the object, but represent information associated with the object or user interaction with the object, like [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) or [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx).</span></span> <span data-ttu-id="17795-134">Par exemple, l’état `aria-checked="false"` dans l’exemple ci-dessous correspond à la case à cocher non activée.</span><span class="sxs-lookup"><span data-stu-id="17795-134">For example, the state `aria-checked="false"` in the example below represents that the checkbox is not checked.</span></span>

``` html
<div role="checkbox" aria-checked="false">Accept</div>
```

<span data-ttu-id="17795-135">Accédez au [modèle de rôles](https://www.w3.org/TR/wai-aria-1.1/#roles) par le W3C pour afficher une liste complète des rôles, propriétés et États.</span><span class="sxs-lookup"><span data-stu-id="17795-135">Go to [The Roles Model](https://www.w3.org/TR/wai-aria-1.1/#roles) by the W3C to see a full list of roles, properties, and states.</span></span>

<span data-ttu-id="17795-136">Pour plus d’informations sur ARIA, voir la section «ARIA» dans la section « [ressources](#resources) ».</span><span class="sxs-lookup"><span data-stu-id="17795-136">For more information on ARIA, see the ARIA in the [Resources](#resources) section.</span></span>

## <span data-ttu-id="17795-137">Ressources</span><span class="sxs-lookup"><span data-stu-id="17795-137">Resources</span></span>

### <span data-ttu-id="17795-138">Notions de base sur l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="17795-138">Accessibility Basics</span></span>
#### [<span data-ttu-id="17795-139">Le projet A11Y</span><span class="sxs-lookup"><span data-stu-id="17795-139">The A11Y Project</span></span>](http://a11yproject.com/)
<span data-ttu-id="17795-140">Le projet A11Y est un effort axé sur la communauté pour faciliter l’accessibilité Web.</span><span class="sxs-lookup"><span data-stu-id="17795-140">The A11Y Project is a community-driven effort to make web accessibility easier.</span></span> <span data-ttu-id="17795-141">Consultez le site de [projet A11Y](https://a11yproject.com/) pour en savoir plus sur les principes d’accessibilité de base, la [bibliothèque](https://a11yproject.com/patterns)de modèles et de gadgets accessibles et leurs [ressources](http://a11yproject.com/resources.html) sur les logiciels d’accessibilité, les blogs, les livres et les outils.</span><span class="sxs-lookup"><span data-stu-id="17795-141">Check out [The A11Y Project](https://a11yproject.com/) site to learn about basic accessibility principles, their accessible pattern and widget [library](https://a11yproject.com/patterns), and their [resources](http://a11yproject.com/resources.html) on accessibility software, blogs, books, and tools.</span></span>

#### [<span data-ttu-id="17795-142">Initiative Web Accessibility (WAI)</span><span class="sxs-lookup"><span data-stu-id="17795-142">Web Accessibility Initiative (WAI)</span></span>](https://w3.org/WAI/)
<span data-ttu-id="17795-143">L’initiative Web Accessibility W3C’s (WAI) vous permet d’améliorer l’accessibilité du Web.</span><span class="sxs-lookup"><span data-stu-id="17795-143">The W3C's Web Accessibility Initiative (WAI) is an effort to help improve the accessibility of the web.</span></span> <span data-ttu-id="17795-144">Son site fournit diverses ressources pour la [prise en main de l’accessibilité Web](https://www.w3.org/WAI/gettingstarted/Overview.html), la [création d’une inclusion, des](https://www.w3.org/WAI/users/Overview.html) [didacticiels et des présentations](https://www.w3.org/WAI/train.html), et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="17795-144">Their site provides a variety of resources for [Getting Started with Web Accessibility](https://www.w3.org/WAI/gettingstarted/Overview.html), [Designing for Inclusion](https://www.w3.org/WAI/users/Overview.html), [tutorials and presentations](https://www.w3.org/WAI/train.html), and more.</span></span>

### <span data-ttu-id="17795-145">Blogs sur l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="17795-145">Accessibility Blogs</span></span>
#### [<span data-ttu-id="17795-146">Le groupe Paciello</span><span class="sxs-lookup"><span data-stu-id="17795-146">The Paciello Group</span></span>](https://www.paciellogroup.com/blog/)
<span data-ttu-id="17795-147">Le groupe Paciello fournit des solutions de Conseil et de technologie aux organisations du monde entier pour s’assurer que leurs clients accèdent efficacement à tous les audiences, tout en remplissant les normes gouvernementales et internationales.</span><span class="sxs-lookup"><span data-stu-id="17795-147">The Paciello Group provides consulting and technology solutions to organizations around the world to ensure their clients reach all audiences effectively and efficiently, while meeting governmental and international standards.</span></span> <span data-ttu-id="17795-148">Leur blog englobe des sujets tels que les meilleures pratiques en matière d’accessibilité Web, les outils d’accessibilité et les tendances en matière d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-148">Their blog covers topics like web accessibility best practices, accessibility tools, and accessibility trends.</span></span>

#### [<span data-ttu-id="17795-149">Accès simple</span><span class="sxs-lookup"><span data-stu-id="17795-149">Simply Accessible</span></span>](http://simplyaccessible.com/articles/)
<span data-ttu-id="17795-150">Le simple accès est une équipe de spécialistes de l’accessibilité qui fournissent une formation sur l’accessibilité, des conseils et plus encore pour modifier la perception de l’accessibilité sur le Web.</span><span class="sxs-lookup"><span data-stu-id="17795-150">Simply Accessible is a team of accessibility specialists providing accessibility training, consulting and more to change the perception of accessibility on the web.</span></span> <span data-ttu-id="17795-151">La section relative à cette rubrique [décrit les meilleures](http://simplyaccessible.com/articles/) pratiques en matière d’accessibilité Web, de conception accessible et plus encore.</span><span class="sxs-lookup"><span data-stu-id="17795-151">Their [Articles](http://simplyaccessible.com/articles/) section discusses best practices for web accessibility, accessible design, and more.</span></span>

#### [<span data-ttu-id="17795-152">Groupe SSB Christian (SSB)</span><span class="sxs-lookup"><span data-stu-id="17795-152">SSB BART Group (SSB)</span></span>](http://www.ssbbartgroup.com/blog/)
<span data-ttu-id="17795-153">Le groupe SSB Christian est une entreprise d’accessibilité numérique qui soutient ses clients lors du développement et du déploiement de produits et services accessibles.</span><span class="sxs-lookup"><span data-stu-id="17795-153">SSB BART Group is a digital accessibility firm supporting their clients in developing and deploying accessible products and services.</span></span> <span data-ttu-id="17795-154">Son blog adresse des rubriques telles que les meilleures pratiques ARIA, les tendances d’accessibilité, les webinaires, etc.</span><span class="sxs-lookup"><span data-stu-id="17795-154">Their blog addresses topics like ARIA best practices, accessibility trends, webinars, and more.</span></span>

### <span data-ttu-id="17795-155">Exemples accessibles</span><span class="sxs-lookup"><span data-stu-id="17795-155">Accessible Examples</span></span>
#### [<span data-ttu-id="17795-156">allié. js-didacticiels</span><span class="sxs-lookup"><span data-stu-id="17795-156">ally.js - Tutorials</span></span>](http://allyjs.io/tutorials/)
<span data-ttu-id="17795-157">Bibliothèque JavaScript pour aider les applications Web modernes en matière d’accessibilité, rendre l’accessibilité plus simple.</span><span class="sxs-lookup"><span data-stu-id="17795-157">JavaScript library to help modern web applications with accessibility concerns by making accessibility simpler.</span></span>

#### [<span data-ttu-id="17795-158">Heydonworks-exemples de ARIA</span><span class="sxs-lookup"><span data-stu-id="17795-158">Heydonworks - ARIA Examples</span></span>](http://heydonworks.com/practical_aria_examples/)
<span data-ttu-id="17795-159">Exemples pratiques ARIA pour améliorer l’accessibilité de votre application</span><span class="sxs-lookup"><span data-stu-id="17795-159">Practical ARIA examples to enhance your application accessibility</span></span>

#### [<span data-ttu-id="17795-160">Exemples de OpenAjax</span><span class="sxs-lookup"><span data-stu-id="17795-160">OpenAjax Examples</span></span>](http://oaa-accessibility.org/)
<span data-ttu-id="17795-161">Le site Web de OpenAjax Alliance est une excellente ressource de vérification des règles pour le WAI-ARIA et fournit plusieurs exemples d’implémentations WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="17795-161">The OpenAjax Alliance website is an excellent resource for verifying the rules for WAI-ARIA and provides a number of examples of WAI-ARIA implementations.</span></span>

#### [<span data-ttu-id="17795-162">Masques</span><span class="sxs-lookup"><span data-stu-id="17795-162">Patterns</span></span>](http://a11yproject.com/patterns.html)
<span data-ttu-id="17795-163">[Le projet A11Y](http://a11yproject.com/) propose une bibliothèque de gadgets et de modèles accessibles tels que des menus, des boutons, des info-bulles, etc.</span><span class="sxs-lookup"><span data-stu-id="17795-163">[The A11Y Project](http://a11yproject.com/) offers a library of accessible widgets and patterns like menus, buttons, tooltips, and more.</span></span>

### <span data-ttu-id="17795-164">Techniques d’accessibilité & outils</span><span class="sxs-lookup"><span data-stu-id="17795-164">Accessibility Techniques & Tools</span></span>
#### [<span data-ttu-id="17795-165">Accessibilité: création d’icônes d’extension accessibles pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="17795-165">Accessibility: Creating accessible extension icons for Microsoft Edge</span></span>](../extensions/guides/accessibility.md)
<span data-ttu-id="17795-166">Obtenez des conseils sur la création d’icônes d’extensions accessibles pour Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="17795-166">Get guidance on creating accessible extensions icons for Microsoft Edge.</span></span>

#### [<span data-ttu-id="17795-167">Nom et description accessibles: calculs et mappages 1,1</span><span class="sxs-lookup"><span data-stu-id="17795-167">Accessible Name and Description: Computation and Mappings 1.1</span></span>](https://www.w3.org/TR/accname-1.1/)
<span data-ttu-id="17795-168">Ce document de mappage W3C décrit la façon dont les navigateurs déterminent les noms et descriptions des objets accessibles dans les langages de contenu Web, et les exposent dans les API d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-168">This W3C mapping document explains how browsers determine name and descriptions of accessible objects from web content languages and expose them in accessibility APIs.</span></span>

#### [<span data-ttu-id="17795-169">Ressources d’évaluation de l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="17795-169">Accessibility Evaluation Resources</span></span>](https://www.w3.org/WAI/eval/Overview.html)
<span data-ttu-id="17795-170">Les ressources d’évaluation de l’accessibilité sont une ressource de plusieurs pages par le W3C qui souligne les différentes approches d’évaluation des sites Web pour l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-170">Accessibility Evaluation Resources is a multi-page resource by the W3C that outlines different approaches for evaluating websites for accessibility.</span></span>

#### [<span data-ttu-id="17795-171">Tests de compatibilité de technologie d’assistance</span><span class="sxs-lookup"><span data-stu-id="17795-171">Assistive technology compatibility tests</span></span>](http://www.powermapper.com/tests/)
<span data-ttu-id="17795-172">Résultats de test montrant le comportement des différents types de contenu et normes dans les technologies d’assistance comme les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="17795-172">Test results showing how different content types and standards behave in assistive technologies (AT) like screen readers.</span></span>

#### [<span data-ttu-id="17795-173">La création de sites Web accessibles est encore plus facile</span><span class="sxs-lookup"><span data-stu-id="17795-173">Building accessible websites just got a lot easier</span></span>](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)
<span data-ttu-id="17795-174">Ce billet de blog .NET Web Development et Tools décrit le [vérificateur d’accessibilité](https://go.microsoft.com/fwlink/p/?linkid=841539)sur le Web de Visual Studio extensions.</span><span class="sxs-lookup"><span data-stu-id="17795-174">This .NET Web Development and Tools blog post describes the Visual Studio extension [Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).</span></span>

#### [<span data-ttu-id="17795-175">Mappages des API d’accessibilité principales 1,1</span><span class="sxs-lookup"><span data-stu-id="17795-175">Core Accessibility API Mappings 1.1</span></span>](https://www.w3.org/TR/core-aam-1.1/)
<span data-ttu-id="17795-176">Ce document de mappage W3C explique comment les sémantiques des langages de contenu Web sont exposées aux API d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-176">This W3C mapping document explains how the semantics of web content languages are exposed to accessibility APIs.</span></span>  

#### [<span data-ttu-id="17795-177">Vérifications simplifiées: un premier examen de l’accessibilité sur le Web</span><span class="sxs-lookup"><span data-stu-id="17795-177">Easy Checks – A First Review of Web Accessibility</span></span>](https://www.w3.org/WAI/eval/preliminary.html)
<span data-ttu-id="17795-178">Séries de contrôles rapide par le WAI qui vous permettent d’identifier l’accessibilité d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="17795-178">A series of quick checks by the WAI that help you asses the accessibility of a web page.</span></span>

#### [<span data-ttu-id="17795-179">Comment respecter les 2,0 de WCAG</span><span class="sxs-lookup"><span data-stu-id="17795-179">How to Meet WCAG 2.0</span></span>](https://www.w3.org/WAI/WCAG20/quickref/)
<span data-ttu-id="17795-180">Référence rapide aux instructions d’accessibilité pour le contenu Web (WCAG) 2,0 (critères de réussite) et aux techniques.</span><span class="sxs-lookup"><span data-stu-id="17795-180">A quick reference to Web Content Accessibility Guidelines (WCAG) 2.0 requirements (success criteria) and techniques.</span></span>

#### [<span data-ttu-id="17795-181">Mappages des API d’accessibilité HTML 1,0</span><span class="sxs-lookup"><span data-stu-id="17795-181">HTML Accessibility API Mappings 1.0</span></span>](https://www.w3.org/TR/html-aam-1.0/)
<span data-ttu-id="17795-182">Ce document relatif aux mappages W3C décrit le mappage des éléments et attributs HTML 5.1 aux API d’accessibilité de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="17795-182">This W3C mappings document explains how HTML5.1 element and attributes map to platform accessibility APIs.</span></span>


#### [<span data-ttu-id="17795-183">Conseils rapides</span><span class="sxs-lookup"><span data-stu-id="17795-183">Quick Tips</span></span>](http://a11yproject.com/#Quick-tips)
<span data-ttu-id="17795-184">Liste de conseils de développement Web rapide pour l’accessibilité par [le projet A11Y](http://a11yproject.com/).</span><span class="sxs-lookup"><span data-stu-id="17795-184">A list of quick web development tips for accessibility by [The A11Y Project](http://a11yproject.com/).</span></span>

#### [<span data-ttu-id="17795-185">Analyse du site</span><span class="sxs-lookup"><span data-stu-id="17795-185">Site Scan</span></span>](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)
<span data-ttu-id="17795-186">L’outil d’analyse de site dans le centre de développement Microsoft Edge recherche les bibliothèques obsolètes, les problèmes de disposition et les problèmes d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-186">The Site Scan tool on Microsoft Edge Dev Center checks for out-of-date libraries, layout issues, and accessibility issues.</span></span>

#### [<span data-ttu-id="17795-187">Techniques pour WCAG 2,0</span><span class="sxs-lookup"><span data-stu-id="17795-187">Techniques for WCAG 2.0</span></span>](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)
<span data-ttu-id="17795-188">Techniques du W3C qui fournissent des recommandations pour les développeurs Web en matière d’indications sur l' [accessibilité du contenu Web de réunion (WCAG) 2,0](https://w3.org/TR/WCAG20/) critères de réussite.</span><span class="sxs-lookup"><span data-stu-id="17795-188">Techniques from the W3C that provide guidance for web developers on meeting [Web Content Accessibility Guidelines (WCAG) 2.0](https://w3.org/TR/WCAG20/) success criteria.</span></span>

#### [<span data-ttu-id="17795-189">Conseils en matière de développement pour l’accessibilité sur le Web</span><span class="sxs-lookup"><span data-stu-id="17795-189">Tips on Developing for Web Accessibility</span></span>](https://w3.org/WAI/gettingstarted/tips/developing.html)
<span data-ttu-id="17795-190">Conseils du W3C sur le développement de contenus Web plus accessibles aux personnes atteintes de handicaps.</span><span class="sxs-lookup"><span data-stu-id="17795-190">Tips from the W3C on developing web content that is more accessible to people with disabilities.</span></span>

#### [<span data-ttu-id="17795-191">WAI-ARIA, pratiques de création 1,1</span><span class="sxs-lookup"><span data-stu-id="17795-191">WAI-ARIA Authoring Practices 1.1</span></span>](http://w3c.github.io/aria-practices/)
<span data-ttu-id="17795-192">Document par le W3C qui fournit aux lecteurs des informations de savoir comment utiliser WAI-ARIA 1,1 et recommande des approches pour rendre les widgets, la navigation et les comportements accessibles à l’aide des rôles et des propriétés WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="17795-192">A document by the W3C that provides readers with an understanding of how to use WAI-ARIA 1.1 and recommends approaches to make widgets, navigation, and behaviors accessible using WAI-ARIA roles, states, and properties.</span></span>

#### [<span data-ttu-id="17795-193">Recommandations et techniques pour le WAI</span><span class="sxs-lookup"><span data-stu-id="17795-193">WAI Guidelines and Techniques</span></span>](https://w3.org/WAI/guid-tech.html)
<span data-ttu-id="17795-194">Série de recommandations et de normes en matière d’accessibilité Web développées par le WAI.</span><span class="sxs-lookup"><span data-stu-id="17795-194">A series of web accessibility guidelines and standards developed by the WAI.</span></span>  

#### [<span data-ttu-id="17795-195">Liste des outils d’évaluation de l’accessibilité Web</span><span class="sxs-lookup"><span data-stu-id="17795-195">Web Accessibility Evaluation Tools List</span></span>](https://www.w3.org/WAI/ER/tools/index.html)
<span data-ttu-id="17795-196">Liste des outils d’évaluation de l’accessibilité du Web permettant de déterminer si les sites Web respectent les recommandations en matière d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="17795-196">A list of web accessibility evaluation tools to help determine if websites meet accessibility guidelines.</span></span>

#### [<span data-ttu-id="17795-197">Perspectives d’accessibilité sur le Web: découvrir les avantages et les avantages de tout le monde</span><span class="sxs-lookup"><span data-stu-id="17795-197">Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone</span></span>](https://w3.org/WAI/perspectives/)
<span data-ttu-id="17795-198">Une série de vidéos de courte durée par le W3C sur l’impact de l’accessibilité et les avantages de tout le monde.</span><span class="sxs-lookup"><span data-stu-id="17795-198">A series of short situational videos by the W3C about the impact of accessibility and the benefits for everyone.</span></span>