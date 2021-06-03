---
description: Enterprise documentation de stratégie pour les extensions Edge (Chromium).
title: Correspondance des modèles
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: fcb87b62cac063c7663f575fa3d992b187408c28
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461247"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="match-patterns"></a><span data-ttu-id="90723-104">Correspondance des modèles</span><span class="sxs-lookup"><span data-stu-id="90723-104">Match Patterns</span></span>

<span data-ttu-id="90723-105">Les autorisations d’hôte et la correspondance de script de contenu sont basées sur un ensemble d’URL définies par des modèles de correspondance.</span><span class="sxs-lookup"><span data-stu-id="90723-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="90723-106">Un modèle de correspondance est essentiellement une URL qui commence par un schéma autorisé ( , , ou , et qui peut contenir `http` `https` ' ' ' `file` `ftp` `*` caractères.</span><span class="sxs-lookup"><span data-stu-id="90723-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="90723-107">Le modèle spécial `<all_urls>` correspond à toute URL qui commence par un schéma autorisé.</span><span class="sxs-lookup"><span data-stu-id="90723-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="90723-108">Chaque modèle de correspondance possède 3 parties :</span><span class="sxs-lookup"><span data-stu-id="90723-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="90723-109">_schéma_ , par exemple, `http` `file` ou</span><span class="sxs-lookup"><span data-stu-id="90723-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="90723-110">L’accès `file` aux URL n’est pas automatique.</span><span class="sxs-lookup"><span data-stu-id="90723-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="90723-111">L’utilisateur doit visiter la page de gestion des extensions et choisir d’accéder à `file` chaque extension qui le demande.</span><span class="sxs-lookup"><span data-stu-id="90723-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="90723-112">— par exemple, `www.google.com` ou ; si le schéma est un `*.google.com` `*` fichier, il n’y a pas de partie hôte.</span><span class="sxs-lookup"><span data-stu-id="90723-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="90723-113">— par exemple, `/*` , `/foo*` ou `/foo/bar` .</span><span class="sxs-lookup"><span data-stu-id="90723-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="90723-114">Le chemin d’accès doit être présent dans une autorisation d’hôte, mais il est toujours traité comme `/*` .</span><span class="sxs-lookup"><span data-stu-id="90723-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="90723-115">Syntaxe de base :</span><span class="sxs-lookup"><span data-stu-id="90723-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="90723-116">La signification varie selon qu’il se trouve dans le `*` schéma, l’hôte ou le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="90723-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="90723-117">Si le schéma est `*` , il correspond à l’une ou `http` `https` l’autre ou `file` non, ou `ftp` .</span><span class="sxs-lookup"><span data-stu-id="90723-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="90723-118">Si l’hôte est `*` juste, il correspond à n’importe quel hôte.</span><span class="sxs-lookup"><span data-stu-id="90723-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="90723-119">Si l’hôte est , il correspond à l’hôte spécifié ou à l’un `*.hostname` des sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="90723-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="90723-120">Dans la section chemin d’accès, `*` chaque caractère correspond à 0 caractère ou plus.</span><span class="sxs-lookup"><span data-stu-id="90723-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="90723-121">Le tableau suivant présente certains modèles valides.</span><span class="sxs-lookup"><span data-stu-id="90723-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="90723-122">Modèle</span><span class="sxs-lookup"><span data-stu-id="90723-122">Pattern</span></span> | <span data-ttu-id="90723-123">Ce qu’il fait</span><span class="sxs-lookup"><span data-stu-id="90723-123">What it does</span></span> | <span data-ttu-id="90723-124">Exemples d’URL correspondantes</span><span class="sxs-lookup"><span data-stu-id="90723-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="90723-125">Correspond à n’importe quelle URL qui utilise le schéma http</span><span class="sxs-lookup"><span data-stu-id="90723-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="90723-126">Correspond à toute URL qui utilise le schéma http, sur n’importe quel hôte, tant que le chemin commence par</span><span class="sxs-lookup"><span data-stu-id="90723-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="90723-127">Correspond à toute URL qui utilise le schéma https, se trouve sur un hôte `google.com` \(par `www.google.com` `docs.google.com` exemple, , ou `google.com` \), tant que le chemin d’accès commence par et `/foo` se termine par</span><span class="sxs-lookup"><span data-stu-id="90723-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="90723-128">Correspond à l’URL spécifiée</span><span class="sxs-lookup"><span data-stu-id="90723-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="90723-129">Correspond à tout fichier local dont le chemin d’accès commence par</span><span class="sxs-lookup"><span data-stu-id="90723-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="90723-130">Correspond à toute URL qui utilise le `http` schéma et qui se trouve sur l’hôte</span><span class="sxs-lookup"><span data-stu-id="90723-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="90723-131">Correspond à n’importe quelle URL qui commence par `http://mail.google.com` ou `https://mail.google.com` .</span><span class="sxs-lookup"><span data-stu-id="90723-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="90723-132">Correspond à toute URL qui utilise un schéma autorisé.</span><span class="sxs-lookup"><span data-stu-id="90723-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="90723-133">\(Voir le début de cette section pour obtenir la liste des schémas autorisés.\)</span><span class="sxs-lookup"><span data-stu-id="90723-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="90723-134">Voici quelques exemples de `_invalid_` correspondances de modèle :</span><span class="sxs-lookup"><span data-stu-id="90723-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="90723-135">Modèle non bon</span><span class="sxs-lookup"><span data-stu-id="90723-135">Bad pattern</span></span> | <span data-ttu-id="90723-136">Pourquoi est-il mauvais ?</span><span class="sxs-lookup"><span data-stu-id="90723-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="90723-137">Non</span><span class="sxs-lookup"><span data-stu-id="90723-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="90723-138">' `*` ' in the host can be followed only by a ' ' or ' ' `.` `/` '</span><span class="sxs-lookup"><span data-stu-id="90723-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="90723-139">Si ' `*` ' ' est dans le , il doit `_host_` s’agit du premier caractère</span><span class="sxs-lookup"><span data-stu-id="90723-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="90723-140">Séparateur `_scheme_` manquant \(' `/` ' doit être " `//` «\)</span><span class="sxs-lookup"><span data-stu-id="90723-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="90723-141">Invalid</span><span class="sxs-lookup"><span data-stu-id="90723-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="90723-142">Certains schémas ne sont pas pris en charge dans tous les contextes.</span><span class="sxs-lookup"><span data-stu-id="90723-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="90723-143">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90723-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="90723-144">La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/match_patterns)</span><span class="sxs-lookup"><span data-stu-id="90723-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="90723-146">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90723-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
