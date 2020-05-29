---
description: Référence pour le domaine CSS. Ce domaine présente les opérations en lecture/écriture CSS. Tous les objets CSS (feuilles de style, règles et styles) sont associés à des `id` opérations ultérieures sur l’objet associé. Chaque type d’objet possède une `id` structure spécifique et celles-ci ne sont pas interchangeables entre les objets de différents genres. Les objets CSS peuvent être chargés en utilisant les `get*ForNode()` appels (qui acceptent un ID de nœud DOM). Un client peut également suivre les feuilles de style par le biais des `styleSheetAdded` / `styleSheetRemoved` événements, puis charger le contenu de la feuille de style requis au moyen des `getStyleSheet[Text]()` méthodes.
title: Version 0,2 du protocole CSS Domain-DevTools
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 939eda0ae2f5228657d35899ab75b39493eff917
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565478"
---
# <span data-ttu-id="16045-108">CSS</span><span class="sxs-lookup"><span data-stu-id="16045-108">CSS</span></span>
<span data-ttu-id="16045-109">Ce domaine présente les opérations en lecture/écriture CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="16045-110">Tous les objets CSS (feuilles de style, règles et styles) sont associés à des `id` opérations ultérieures sur l’objet associé.</span><span class="sxs-lookup"><span data-stu-id="16045-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="16045-111">Chaque type d’objet possède une `id` structure spécifique et celles-ci ne sont pas interchangeables entre les objets de différents genres.</span><span class="sxs-lookup"><span data-stu-id="16045-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="16045-112">Les objets CSS peuvent être chargés en utilisant les `get*ForNode()` appels (qui acceptent un ID de nœud DOM).</span><span class="sxs-lookup"><span data-stu-id="16045-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="16045-113">Un client peut également suivre les feuilles de style par le biais des `styleSheetAdded` / `styleSheetRemoved` événements, puis charger le contenu de la feuille de style requis au moyen des `getStyleSheet[Text]()` méthodes.</span><span class="sxs-lookup"><span data-stu-id="16045-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="16045-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16045-114">Methods</span></span>**](#methods) | <span data-ttu-id="16045-115">[activer](#enable), [Désactiver](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="16045-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="16045-116">Événements</span><span class="sxs-lookup"><span data-stu-id="16045-116">Events</span></span>**](#events) | <span data-ttu-id="16045-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="16045-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="16045-118">Types</span><span class="sxs-lookup"><span data-stu-id="16045-118">Types</span></span>**](#types) | <span data-ttu-id="16045-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span><span class="sxs-lookup"><span data-stu-id="16045-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="16045-120">Dépendances</span><span class="sxs-lookup"><span data-stu-id="16045-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="16045-121">DOM</span><span class="sxs-lookup"><span data-stu-id="16045-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="16045-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16045-122">Methods</span></span>

### <span data-ttu-id="16045-123">activer</span><span class="sxs-lookup"><span data-stu-id="16045-123">enable</span></span>
<span data-ttu-id="16045-124">Active l’agent CSS pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="16045-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="16045-125">Les clients ne doivent pas supposer que l’agent CSS a été activé tant que le résultat de la commande n’a pas été reçu.</span><span class="sxs-lookup"><span data-stu-id="16045-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="16045-126">désactiver </span><span class="sxs-lookup"><span data-stu-id="16045-126">disable</span></span>
<span data-ttu-id="16045-127">Désactive l’agent CSS pour la page donnée.</span><span class="sxs-lookup"><span data-stu-id="16045-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="16045-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="16045-128">getInlineStylesForNode</span></span>
<span data-ttu-id="16045-129">Retourne les styles définis inline (explicitement dans l’attribut «style» et implicitement à l’aide d’attributs DOM) pour un nœud DOM identifié par `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="16045-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-130">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-131">ID</span><span class="sxs-lookup"><span data-stu-id="16045-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-132">Renvoie</span><span class="sxs-lookup"><span data-stu-id="16045-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-133">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="16045-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="16045-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-135">Style intraligne du nœud DOM spécifié.</span><span class="sxs-lookup"><span data-stu-id="16045-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-136">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="16045-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="16045-137">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-138">Style d’élément défini par l’attribut (par exemple, «Width = 20 Height = 100%»).</span><span class="sxs-lookup"><span data-stu-id="16045-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="16045-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="16045-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="16045-140">Renvoie les styles requis pour un nœud DOM identifié par `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="16045-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-141">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-142">ID</span><span class="sxs-lookup"><span data-stu-id="16045-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-143">Renvoie</span><span class="sxs-lookup"><span data-stu-id="16045-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-144">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="16045-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="16045-145">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-146">Style intraligne du nœud DOM spécifié.</span><span class="sxs-lookup"><span data-stu-id="16045-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-147">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="16045-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="16045-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-149">Style d’élément défini par l’attribut (par exemple, «Width = 20 Height = 100%»).</span><span class="sxs-lookup"><span data-stu-id="16045-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="16045-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="16045-151">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="16045-152">Règles CSS correspondant à ce nœud, de toutes les feuilles de style en vigueur.</span><span class="sxs-lookup"><span data-stu-id="16045-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="16045-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="16045-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="16045-155">Correspondances de Pseudo-styles pour ce nœud.</span><span class="sxs-lookup"><span data-stu-id="16045-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-156">héritées</span><span class="sxs-lookup"><span data-stu-id="16045-156">inherited</span></span> <br /> <i><span data-ttu-id="16045-157">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="16045-158">Chaîne de styles hérités (du nœud immédiat parent jusqu’à la racine de l’arborescence DOM).</span><span class="sxs-lookup"><span data-stu-id="16045-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="16045-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="16045-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="16045-161">Liste des animations par images clés CSS correspondant à ce nœud.</span><span class="sxs-lookup"><span data-stu-id="16045-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="16045-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="16045-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="16045-163">Demande des informations sur les polices de plateforme que nous avons utilisées pour afficher les TextNodes enfants dans le nœud donné.</span><span class="sxs-lookup"><span data-stu-id="16045-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-164">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-165">ID</span><span class="sxs-lookup"><span data-stu-id="16045-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-166">Renvoie</span><span class="sxs-lookup"><span data-stu-id="16045-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-167">polices</span><span class="sxs-lookup"><span data-stu-id="16045-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="16045-168">Statistiques d’utilisation pour chaque police de plateforme utilisée.</span><span class="sxs-lookup"><span data-stu-id="16045-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="16045-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="16045-169">getComputedStyleForNode</span></span>
<span data-ttu-id="16045-170">Renvoie le style calculé pour un nœud DOM identifié par `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="16045-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-171">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-172">ID</span><span class="sxs-lookup"><span data-stu-id="16045-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-173">Renvoie</span><span class="sxs-lookup"><span data-stu-id="16045-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-174">computedStyle</span><span class="sxs-lookup"><span data-stu-id="16045-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="16045-175">Style calculé pour le nœud DOM spécifié.</span><span class="sxs-lookup"><span data-stu-id="16045-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="16045-176">Événements</span><span class="sxs-lookup"><span data-stu-id="16045-176">Events</span></span>

### <span data-ttu-id="16045-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="16045-177">styleSheetAdded</span></span>
<span data-ttu-id="16045-178">Déclenché lors de l’ajout d’une feuille de style de document active.</span><span class="sxs-lookup"><span data-stu-id="16045-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-179">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-180">header</span><span class="sxs-lookup"><span data-stu-id="16045-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="16045-181">A ajouté des méta-informations.</span><span class="sxs-lookup"><span data-stu-id="16045-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="16045-182">styleSheetChanged</span><span class="sxs-lookup"><span data-stu-id="16045-182">styleSheetChanged</span></span>
<span data-ttu-id="16045-183">Déclenché dès que le résultat de l’opération du client est modifié.</span><span class="sxs-lookup"><span data-stu-id="16045-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-184">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-185">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="16045-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="16045-186">styleSheetRemoved</span></span>
<span data-ttu-id="16045-187">Déclenché lors de la suppression d’une feuille de style de document active.</span><span class="sxs-lookup"><span data-stu-id="16045-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-188">Parameters</span><span class="sxs-lookup"><span data-stu-id="16045-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-189">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="16045-190">Identificateur de la feuille de style supprimée.</span><span class="sxs-lookup"><span data-stu-id="16045-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="16045-191">Types</span><span class="sxs-lookup"><span data-stu-id="16045-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="16045-192">StyleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="16045-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="16045-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="16045-194">Collection de règles CSS pour un Pseudo-style unique.</span><span class="sxs-lookup"><span data-stu-id="16045-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-195">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-196">pseudoType</span><span class="sxs-lookup"><span data-stu-id="16045-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="16045-197">Type de pseudo-élément.</span><span class="sxs-lookup"><span data-stu-id="16045-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-198">matches</span><span class="sxs-lookup"><span data-stu-id="16045-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="16045-199">Correspondances de règles CSS applicables au Pseudo-style.</span><span class="sxs-lookup"><span data-stu-id="16045-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="16045-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="16045-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="16045-201">Collection de règles CSS héritée du nœud ancêtre.</span><span class="sxs-lookup"><span data-stu-id="16045-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-202">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-203">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="16045-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="16045-204">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-205">Le style intraligne du nœud ancêtre, le cas échéant, dans la chaîne d’héritage de style.</span><span class="sxs-lookup"><span data-stu-id="16045-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="16045-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="16045-207">Correspondances de règles CSS correspondant au nœud ancêtre dans la chaîne d’héritage de style.</span><span class="sxs-lookup"><span data-stu-id="16045-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="16045-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="16045-208">RuleMatch</span></span> `object`

<span data-ttu-id="16045-209">Correspondent aux données pour une règle CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-210">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-211">elle</span><span class="sxs-lookup"><span data-stu-id="16045-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="16045-212">Règle CSS dans la correspondance.</span><span class="sxs-lookup"><span data-stu-id="16045-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="16045-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="16045-213">Value</span></span> `object`

<span data-ttu-id="16045-214">Les données d’un sélecteur simple (délimitées par des virgules dans une liste de sélecteur).</span><span class="sxs-lookup"><span data-stu-id="16045-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-215">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-216">texte</span><span class="sxs-lookup"><span data-stu-id="16045-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-217">Texte de la valeur.</span><span class="sxs-lookup"><span data-stu-id="16045-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-218">portée</span><span class="sxs-lookup"><span data-stu-id="16045-218">range</span></span> <br /> <i><span data-ttu-id="16045-219">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="16045-220">Plage de valeurs de la ressource sous-jacente (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="16045-221">SelectorList</span><span class="sxs-lookup"><span data-stu-id="16045-221">SelectorList</span></span> `object`

<span data-ttu-id="16045-222">Afficher les données des listes.</span><span class="sxs-lookup"><span data-stu-id="16045-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-223">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-224">sélecteurs</span><span class="sxs-lookup"><span data-stu-id="16045-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="16045-225">Sélectionneurs de la liste.</span><span class="sxs-lookup"><span data-stu-id="16045-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-226">texte</span><span class="sxs-lookup"><span data-stu-id="16045-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-227">Texte du sélecteur de règles</span><span class="sxs-lookup"><span data-stu-id="16045-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="16045-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="16045-228">CSSRule</span></span> `object`

<span data-ttu-id="16045-229">Représentation de la règle CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-230">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-231">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="16045-232">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="16045-233">Identifiant de la feuille de style CSS (absent pour la feuille de style de l’agent utilisateur et règles de feuille de style spécifiées par l’utilisateur) dont provient cette règle.</span><span class="sxs-lookup"><span data-stu-id="16045-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-234">selectorList</span><span class="sxs-lookup"><span data-stu-id="16045-234">selectorList</span></span> <br /> <i><span data-ttu-id="16045-235">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="16045-236">Données du sélecteur de règles.</span><span class="sxs-lookup"><span data-stu-id="16045-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-237">prêts</span><span class="sxs-lookup"><span data-stu-id="16045-237">origin</span></span> <br /> <i><span data-ttu-id="16045-238">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="16045-239">Origine de la feuille de style parente.</span><span class="sxs-lookup"><span data-stu-id="16045-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-240">style</span><span class="sxs-lookup"><span data-stu-id="16045-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-241">Déclaration de style associée.</span><span class="sxs-lookup"><span data-stu-id="16045-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-242">médias</span><span class="sxs-lookup"><span data-stu-id="16045-242">media</span></span> <br /> <i><span data-ttu-id="16045-243">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="16045-244">Tableau de liste de médias (pour les règles impliquant des requêtes multimédias).</span><span class="sxs-lookup"><span data-stu-id="16045-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="16045-245">Le tableau recense les requêtes multimédias à partir de l’élément le plus interne, en partant du haut.</span><span class="sxs-lookup"><span data-stu-id="16045-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="16045-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="16045-246">SourceRange</span></span> `object`

<span data-ttu-id="16045-247">Plage de textes au sein d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="16045-247">Text range within a resource.</span></span> <span data-ttu-id="16045-248">Tous les nombres sont en fonction du zéro.</span><span class="sxs-lookup"><span data-stu-id="16045-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-249">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-250">startLine</span><span class="sxs-lookup"><span data-stu-id="16045-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="16045-251">Ligne de début de la plage.</span><span class="sxs-lookup"><span data-stu-id="16045-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-252">ColonneDébut</span><span class="sxs-lookup"><span data-stu-id="16045-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="16045-253">Colonne de début de plage (inclusive).</span><span class="sxs-lookup"><span data-stu-id="16045-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-254">lignefin</span><span class="sxs-lookup"><span data-stu-id="16045-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="16045-255">Ligne de fin de la plage</span><span class="sxs-lookup"><span data-stu-id="16045-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-256">ColonneFin</span><span class="sxs-lookup"><span data-stu-id="16045-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="16045-257">Colonne de plage de fin (exclusif).</span><span class="sxs-lookup"><span data-stu-id="16045-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="16045-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="16045-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-259">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-260">name</span><span class="sxs-lookup"><span data-stu-id="16045-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-261">Nom abrégé.</span><span class="sxs-lookup"><span data-stu-id="16045-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-262">value</span><span class="sxs-lookup"><span data-stu-id="16045-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-263">Valeur raccourci.</span><span class="sxs-lookup"><span data-stu-id="16045-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-264">essentielles</span><span class="sxs-lookup"><span data-stu-id="16045-264">important</span></span> <br /> <i><span data-ttu-id="16045-265">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-266">Si la propriété comporte une annotation «! important» (implique qu’il n’en soit pas `false` ).</span><span class="sxs-lookup"><span data-stu-id="16045-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="16045-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="16045-267">CSSStyle</span></span> `object`

<span data-ttu-id="16045-268">Représentation de style CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-269">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-270">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="16045-271">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="16045-272">Identifiant de la feuille de style CSS (absent pour la feuille de style de l’agent utilisateur et règles de feuille de style spécifiées par l’utilisateur) dont provient cette règle.</span><span class="sxs-lookup"><span data-stu-id="16045-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="16045-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="16045-274">Propriétés CSS du style.</span><span class="sxs-lookup"><span data-stu-id="16045-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="16045-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="16045-276">Valeurs calculées pour tous les raccourcis identifiés dans le style.</span><span class="sxs-lookup"><span data-stu-id="16045-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-277">cssText</span><span class="sxs-lookup"><span data-stu-id="16045-277">cssText</span></span> <br /> <i><span data-ttu-id="16045-278">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-279">Texte de la déclaration de style (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-280">portée</span><span class="sxs-lookup"><span data-stu-id="16045-280">range</span></span> <br /> <i><span data-ttu-id="16045-281">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="16045-282">Plage de déclaration de style dans la feuille de style englobante (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="16045-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="16045-283">CSSProperty</span></span> `object`

<span data-ttu-id="16045-284">Données de déclaration de propriété CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-285">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-286">name</span><span class="sxs-lookup"><span data-stu-id="16045-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-287">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="16045-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-288">value</span><span class="sxs-lookup"><span data-stu-id="16045-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-289">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="16045-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-290">essentielles</span><span class="sxs-lookup"><span data-stu-id="16045-290">important</span></span> <br /> <i><span data-ttu-id="16045-291">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-292">Si la propriété comporte une annotation «! important» (implique qu’il n’en soit pas `false` ).</span><span class="sxs-lookup"><span data-stu-id="16045-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-293">prennent</span><span class="sxs-lookup"><span data-stu-id="16045-293">implicit</span></span> <br /> <i><span data-ttu-id="16045-294">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-295">L’utilisation de la propriété implicite (implique `false` si absent).</span><span class="sxs-lookup"><span data-stu-id="16045-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-296">texte</span><span class="sxs-lookup"><span data-stu-id="16045-296">text</span></span> <br /> <i><span data-ttu-id="16045-297">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-298">Texte de la propriété complète, tel qu’indiqué dans le style.</span><span class="sxs-lookup"><span data-stu-id="16045-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="16045-299">parsedOk</span></span> <br /> <i><span data-ttu-id="16045-300">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-301">Si la propriété est comprise par le navigateur (c’est-à-dire si elle est `true` absente).</span><span class="sxs-lookup"><span data-stu-id="16045-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-302">désactivé</span><span class="sxs-lookup"><span data-stu-id="16045-302">disabled</span></span> <br /> <i><span data-ttu-id="16045-303">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-304">Si la propriété est désactivée par l’utilisateur (disponible uniquement pour les propriétés sources).</span><span class="sxs-lookup"><span data-stu-id="16045-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-305">portée</span><span class="sxs-lookup"><span data-stu-id="16045-305">range</span></span> <br /> <i><span data-ttu-id="16045-306">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="16045-307">Plage de propriétés entière de la déclaration de style englobante (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="16045-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="16045-308">CSSMedia</span></span> `object`

<span data-ttu-id="16045-309">Descripteur de règle multimédia CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-310">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-311">texte</span><span class="sxs-lookup"><span data-stu-id="16045-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-312">Texte de la requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-313">origine</span><span class="sxs-lookup"><span data-stu-id="16045-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="16045-314">Valeurs autorisées: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="16045-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="16045-315">Source de la requête multimédia: «mediaRule» s’il est spécifié par une règle de @media, «importRule» s’il est spécifié par une règle de @import, «linkedSheet» en cas de spécification par un attribut «Media» dans la balise de liaison d’une feuille de style de feuille de style</span><span class="sxs-lookup"><span data-stu-id="16045-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="16045-316">sourceURL</span></span> <br /> <i><span data-ttu-id="16045-317">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-318">URL du document contenant la description de la requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-319">portée</span><span class="sxs-lookup"><span data-stu-id="16045-319">range</span></span> <br /> <i><span data-ttu-id="16045-320">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="16045-321">La règle associée (@media ou @import) dans la feuille de style englobante (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-322">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="16045-323">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="16045-324">Identificateur de la feuille de style contenant cet objet (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-325">le médiane</span><span class="sxs-lookup"><span data-stu-id="16045-325">mediaList</span></span> <br /> <i><span data-ttu-id="16045-326">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="16045-327">Tableau de requêtes multimédias.</span><span class="sxs-lookup"><span data-stu-id="16045-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="16045-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="16045-328">MediaQuery</span></span> `object`

<span data-ttu-id="16045-329">Descripteur de requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-330">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-331">contenu</span><span class="sxs-lookup"><span data-stu-id="16045-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="16045-332">Tableau d’expressions de requête multimédias.</span><span class="sxs-lookup"><span data-stu-id="16045-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-333">active</span><span class="sxs-lookup"><span data-stu-id="16045-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-334">Si la condition de requête multimédia est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="16045-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="16045-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="16045-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="16045-336">Descriptor expression de requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-337">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-338">value</span><span class="sxs-lookup"><span data-stu-id="16045-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="16045-339">Valeur de l’expression de requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-340">centres</span><span class="sxs-lookup"><span data-stu-id="16045-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-341">Unités d’expression de requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-342">fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="16045-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-343">Fonctionnalité d’expression de requête multimédia.</span><span class="sxs-lookup"><span data-stu-id="16045-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="16045-344">valueRange</span></span> <br /> <i><span data-ttu-id="16045-345">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="16045-346">Plage associée du texte de la valeur figurant dans la feuille de style englobante (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="16045-347">computedLength</span></span> <br /> <i><span data-ttu-id="16045-348">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="16045-349">Durée calculée de l’expression de requête multimédia (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="16045-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="16045-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="16045-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="16045-351">Informations sur le nombre de glyphes qui ont été affichés avec la police donnée.</span><span class="sxs-lookup"><span data-stu-id="16045-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-352">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-353">familyName</span><span class="sxs-lookup"><span data-stu-id="16045-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-354">Nom de la famille de polices signalé par la plate-forme.</span><span class="sxs-lookup"><span data-stu-id="16045-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="16045-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-356">Indique si la police a été téléchargée ou résolue localement.</span><span class="sxs-lookup"><span data-stu-id="16045-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="16045-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="16045-358">Nombre de glyphes qui ont été affichés avec cette police.</span><span class="sxs-lookup"><span data-stu-id="16045-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="16045-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="16045-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="16045-360">Représentation de la règle CSS frames</span><span class="sxs-lookup"><span data-stu-id="16045-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-361">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-362">animationName</span><span class="sxs-lookup"><span data-stu-id="16045-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="16045-363">Nom de l’animation.</span><span class="sxs-lookup"><span data-stu-id="16045-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-364">images clés</span><span class="sxs-lookup"><span data-stu-id="16045-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="16045-365">Liste d’images clés.</span><span class="sxs-lookup"><span data-stu-id="16045-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="16045-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="16045-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="16045-367">Représentation de la règle d’image clé CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-368">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-369">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="16045-370">facultatif</span><span class="sxs-lookup"><span data-stu-id="16045-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="16045-371">Identifiant de la feuille de style CSS (absent pour la feuille de style de l’agent utilisateur et règles de feuille de style spécifiées par l’utilisateur) dont provient cette règle.</span><span class="sxs-lookup"><span data-stu-id="16045-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-372">prêts</span><span class="sxs-lookup"><span data-stu-id="16045-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="16045-373">Origine de la feuille de style parente.</span><span class="sxs-lookup"><span data-stu-id="16045-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-374">keytext</span><span class="sxs-lookup"><span data-stu-id="16045-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="16045-375">Texte de clé associé.</span><span class="sxs-lookup"><span data-stu-id="16045-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-376">style</span><span class="sxs-lookup"><span data-stu-id="16045-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="16045-377">Déclaration de style associée.</span><span class="sxs-lookup"><span data-stu-id="16045-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="16045-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="16045-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-379">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-380">name</span><span class="sxs-lookup"><span data-stu-id="16045-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-381">Nom de la propriété de style calculée.</span><span class="sxs-lookup"><span data-stu-id="16045-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-382">value</span><span class="sxs-lookup"><span data-stu-id="16045-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-383">Valeur de propriété de style calculée.</span><span class="sxs-lookup"><span data-stu-id="16045-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="16045-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="16045-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="16045-385">Données de feuille de style CSS.</span><span class="sxs-lookup"><span data-stu-id="16045-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="16045-386">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16045-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="16045-387">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="16045-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="16045-388">Identificateur de la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="16045-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="16045-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="16045-390">URL de la ressource StyleSheet.</span><span class="sxs-lookup"><span data-stu-id="16045-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-391">désactivé</span><span class="sxs-lookup"><span data-stu-id="16045-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-392">Indique si la feuille de style est désactivée.</span><span class="sxs-lookup"><span data-stu-id="16045-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-393">isInline</span><span class="sxs-lookup"><span data-stu-id="16045-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="16045-394">Si cette feuille de STYLE est créée pour la balise de STYLE par parser.</span><span class="sxs-lookup"><span data-stu-id="16045-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="16045-395">Cet indicateur n’est pas défini pour les balises de STYLE document. crit.</span><span class="sxs-lookup"><span data-stu-id="16045-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-396">startLine</span><span class="sxs-lookup"><span data-stu-id="16045-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="16045-397">Décalage de ligne de la feuille de style dans la ressource (en fonction de zéro).</span><span class="sxs-lookup"><span data-stu-id="16045-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-398">ColonneDébut</span><span class="sxs-lookup"><span data-stu-id="16045-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="16045-399">Décalage de colonne de la feuille de style dans la ressource (en fonction de zéro).</span><span class="sxs-lookup"><span data-stu-id="16045-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="16045-400">nombre</span><span class="sxs-lookup"><span data-stu-id="16045-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="16045-401">Taille du contenu (en caractères).</span><span class="sxs-lookup"><span data-stu-id="16045-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="16045-402">Dépendances</span><span class="sxs-lookup"><span data-stu-id="16045-402">Dependencies</span></span>

[<span data-ttu-id="16045-403">DOM</span><span class="sxs-lookup"><span data-stu-id="16045-403">DOM</span></span>](dom.md)
