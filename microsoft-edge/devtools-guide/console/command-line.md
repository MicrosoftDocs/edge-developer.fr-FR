---
description: Utiliser la ligne de commande console pour interagir avec une page en cours d’exécution
title: DevTools-console-ligne de commande
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, ligne de commande de la console
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566389"
---
# <span data-ttu-id="4c8d6-104">Ligne de commande de la console</span><span class="sxs-lookup"><span data-stu-id="4c8d6-104">Console command line</span></span>

<span data-ttu-id="4c8d6-105">Utilisez la ligne de commande console pour afficher et modifier les valeurs d’une page et exécuter du code de débogage à la volée, tout en tirant parti de la saisie semi-automatique de Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) .</span><span class="sxs-lookup"><span data-stu-id="4c8d6-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="4c8d6-106">Entrez simplement n’importe quel code JavaScript valide à l’invite de la ligne de commande, puis appuyez sur `Enter` exécuter.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="4c8d6-107">Pour une entrée multiligne, utilisez `Shift+Enter` la fonction de saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="4c8d6-108">Utilisez les `Up` `Down` touches de direction et pour parcourir les commandes de console précédentes que vous avez entrées lors de la session devtools actuelle.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="4c8d6-109">Outre le langage JavaScript standard et l' [API console](./console-api.md), la console prend également en charge les commandes suivantes pour:</span><span class="sxs-lookup"><span data-stu-id="4c8d6-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="4c8d6-110">Sélection d’objets DOM</span><span class="sxs-lookup"><span data-stu-id="4c8d6-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="4c8d6-111">Inspecter les propriétés de l’objet</span><span class="sxs-lookup"><span data-stu-id="4c8d6-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="4c8d6-112">Recherche de tous les écouteurs d’événements sur un objet donné</span><span class="sxs-lookup"><span data-stu-id="4c8d6-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="4c8d6-113">Le script entré dans la ligne de commande s’exécute dans l' [étendue globale](/scripting/javascript/advanced/variable-scope-javascript) de la fenêtre actuellement sélectionnée, sauf si celle-ci est suspendue à un point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="4c8d6-114">Les commandes de console entrées alors que la page est en pause s’exécutent dans l' [étendue locale](/scripting/javascript/advanced/variable-scope-javascript) de la fonction Current dans la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="4c8d6-115">La console dispose d’une liste déroulante de contexte d’exécution **cible** juste au-dessus de la zone de sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="4c8d6-116">La sélection par défaut est le document de niveau supérieur **_top**.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="4c8d6-117">Les iframes du document ou de l’exécution d’extensions apparaissent également sous la forme d’options, ce qui vous permet d’exécuter d’autres commandes dans ces zones.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="4c8d6-118">Sélecteurs DOM</span><span class="sxs-lookup"><span data-stu-id="4c8d6-118">DOM selectors</span></span>
<span data-ttu-id="4c8d6-119">Ces sélecteurs de console fournissent des raccourcis simples pour accéder rapidement aux objets au sein du DOM:</span><span class="sxs-lookup"><span data-stu-id="4c8d6-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="4c8d6-120">$ (*Chaîne de sélecteur CSS*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="4c8d6-121">Retourne le premier élément dans le document correspondant au [Sélecteur de feuilles de style CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) spécifié (ou au groupe de sélecteurs de valeurs séparées par des virgules).</span><span class="sxs-lookup"><span data-stu-id="4c8d6-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="4c8d6-122">Sténo pour [document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="4c8d6-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="4c8d6-123">Par exemple: Ouvrez la console et tapez `$('#main')` pour renvoyer l’objet div `id='main'` sur la page suivante.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Exemple d’utilisation du sélecteur' $ '](../media/console_cmd_$.png)

### <span data-ttu-id="4c8d6-125">$ $ (*Chaîne de sélecteur CSS*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="4c8d6-126">Retourne un tableau d’éléments dans le document correspondant au [Sélecteur de feuilles de style CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) spécifié (ou au groupe de sélecteurs de valeurs séparées par des virgules).</span><span class="sxs-lookup"><span data-stu-id="4c8d6-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="4c8d6-127">Sténo pour [document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="4c8d6-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="4c8d6-128">Par exemple: Ouvrez la console et tapez `$$('.container')` pour renvoyer tous les objets div with `class='container'` sur cette page.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Exemple d’utilisation du sélecteur' $ $ '](../media/console_cmd_$$.png)

### <span data-ttu-id="4c8d6-130">$0, $1, $2,...</span><span class="sxs-lookup"><span data-stu-id="4c8d6-130">$0, $1, $2,...</span></span>
<span data-ttu-id="4c8d6-131">Renvoie les derniers éléments sélectionnés dans le panneau [**éléments**](../elements.md) , où `$0` représente l’élément sélectionné, `$1` l’élément sélectionné auparavant, etc.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="4c8d6-132">Par exemple: Ouvrez DevTools sur l’onglet **éléments** , appuyez sur `CTRL + B` pour activer l’outil **Sélectionner l’élément** , puis cliquez sur une zone de cette page à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="4c8d6-133">Ouvrez ensuite la console et tapez `$0` pour renvoyer l’élément sur lequel vous avez cliqué.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Exemple d’utilisation du sélecteur' $0 '](../media/console_cmd_$0.png)

### <span data-ttu-id="4c8d6-135">$x (*expression XPath*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="4c8d6-136">Retourne un tableau d’éléments qui correspond à l’expression [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="4c8d6-137">Par exemple: Ouvrez la console et tapez `$x('//script[@defer]')` pour renvoyer tous les `<script>` éléments de cette page qui contiennent un `defer` attribut.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Exemple d’utilisation du sélecteur de $x](../media/console_cmd_$x.png)

## <span data-ttu-id="4c8d6-139">Inspection d’objets</span><span class="sxs-lookup"><span data-stu-id="4c8d6-139">Object inspection</span></span>

<span data-ttu-id="4c8d6-140">Ces commandes fournissent des méthodes rapides pour inspecter les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="4c8d6-141">L’objet spécifié doit être défini soit dans l’espace de noms global, soit dans l’étendue actuelle du débogueur.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="4c8d6-142">dir (*objet*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-142">dir(*object*)</span></span>
<span data-ttu-id="4c8d6-143">Renvoie une liste d’arborescence des propriétés de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="4c8d6-144">Par exemple: Ouvrez la console et tapez `dir(document)` pour afficher les propriétés de l’objet document correspondant à cette page.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Exemple d’utilisation de la méthode dir](../media/console_cmd_dir.png)

### <span data-ttu-id="4c8d6-146">Keys (*objet*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-146">keys(*object*)</span></span>
<span data-ttu-id="4c8d6-147">Renvoie un tableau de noms de propriété joints à l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="4c8d6-148">Par exemple: Ouvrez la console et tapez `keys(window)` pour renvoyer toutes les propriétés définies sur l’objet Window global.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Exemple d’utilisation de la méthode «Keys»](../media/console_cmd_keys.png)

### <span data-ttu-id="4c8d6-150">valeurs (*objet*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-150">values(*object*)</span></span>
<span data-ttu-id="4c8d6-151">Retourne un tableau de valeurs de propriété jointes à l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="4c8d6-152">Par exemple: Ouvrez la console et tapez `values(window)` pour renvoyer les valeurs de toutes les propriétés (clés) définies sur l’objet fenêtre globale.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Exemple d’utilisation de la méthode «values»](../media/console_cmd_values.png)

## <span data-ttu-id="4c8d6-154">Écouteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="4c8d6-154">Event listeners</span></span>

<span data-ttu-id="4c8d6-155">Cette commande vous permet d’inspecter les détecteurs d’événements enregistrés sur un objet donné.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="4c8d6-156">L’objet spécifié doit être défini soit dans l’espace de noms global, soit dans l’étendue actuelle du débogueur.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="4c8d6-157">getEventListeners (*objet*)</span><span class="sxs-lookup"><span data-stu-id="4c8d6-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="4c8d6-158">Renvoie un objet contenant une clé pour chaque type d’événement inscrit sur l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="4c8d6-159">La valeur de chaque clé est un tableau de détecteurs d’événements et leurs informations associées.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="4c8d6-160">Par exemple: Ouvrez la console et tapez `getEventListeners(document)` pour afficher tous les écouteurs d’événements enregistrés dans l’objet document de cette page.</span><span class="sxs-lookup"><span data-stu-id="4c8d6-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Exemple d’utilisation de la méthode «getEventListeners»](../media/console_cmd_getEventListeners.png)
