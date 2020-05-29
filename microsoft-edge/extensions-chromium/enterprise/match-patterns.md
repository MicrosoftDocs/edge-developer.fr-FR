---
description: Extensions de la documentation sur les stratégies d’entreprise pour le chrome.
title: Correspondance des modèles
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 16f54fcdc127822e89e050c367a681d886b0c8d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565445"
---
# <span data-ttu-id="c625e-104">Correspondance des modèles</span><span class="sxs-lookup"><span data-stu-id="c625e-104">Match Patterns</span></span>

<span data-ttu-id="c625e-105">Les autorisations d’hébergement et la correspondance de script de contenu sont basées sur un ensemble d’URL définies en fonction de critères de correspondance.</span><span class="sxs-lookup"><span data-stu-id="c625e-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="c625e-106">Un modèle match est essentiellement une URL qui commence par un schéma autorisé ( `http` ,,,,, `https` `file` `ftp` et qui peut contenir « `*` ».</span><span class="sxs-lookup"><span data-stu-id="c625e-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="c625e-107">Le modèle spécial `<all_urls>` correspond à toute URL qui commence par un schéma autorisé.</span><span class="sxs-lookup"><span data-stu-id="c625e-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="c625e-108">Chaque modèle de correspondance comporte 3 parties:</span><span class="sxs-lookup"><span data-stu-id="c625e-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="c625e-109">_modèle_ , par exemple, `http` ou `file`</span><span class="sxs-lookup"><span data-stu-id="c625e-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="c625e-110">L’accès aux `file` URL n’est pas automatique.</span><span class="sxs-lookup"><span data-stu-id="c625e-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="c625e-111">L’utilisateur doit se rendre sur la page de gestion des extensions et sélectionner l' `file` accès pour chaque extension le demandant.</span><span class="sxs-lookup"><span data-stu-id="c625e-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="c625e-112">par exemple, `www.google.com` ou `*.google.com` ou `*` ; si le schéma est un fichier, il n’y a pas de partie hôte.</span><span class="sxs-lookup"><span data-stu-id="c625e-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="c625e-113">par exemple, `/*` `/foo*` ou `/foo/bar` .</span><span class="sxs-lookup"><span data-stu-id="c625e-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="c625e-114">Le chemin d’accès doit être présent dans une autorisation d’hôte, mais il est toujours traité comme `/*` .</span><span class="sxs-lookup"><span data-stu-id="c625e-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="c625e-115">La syntaxe de base:</span><span class="sxs-lookup"><span data-stu-id="c625e-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="c625e-116">La signification de `*` varie selon qu’il se trouve dans la partie schéma, hôte ou chemin.</span><span class="sxs-lookup"><span data-stu-id="c625e-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="c625e-117">S’il s’agit de la méthode `*` , elle correspond à la valeur `http` ou `https` , et non `file` , ou `ftp` .</span><span class="sxs-lookup"><span data-stu-id="c625e-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="c625e-118">S’il s’agit de l’hôte uniquement `*` , il correspond à n’importe quel hôte.</span><span class="sxs-lookup"><span data-stu-id="c625e-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="c625e-119">S’il s’agit de l’hôte `*.hostname` , il correspond à l’hôte spécifié ou à l’un de ses sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="c625e-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="c625e-120">Dans la section Path, chaque `*` caractère correspond à 0.</span><span class="sxs-lookup"><span data-stu-id="c625e-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="c625e-121">Le tableau suivant contient des modèles valides.</span><span class="sxs-lookup"><span data-stu-id="c625e-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="c625e-122">Agrément</span><span class="sxs-lookup"><span data-stu-id="c625e-122">Pattern</span></span> | <span data-ttu-id="c625e-123">Fonction</span><span class="sxs-lookup"><span data-stu-id="c625e-123">What it does</span></span> | <span data-ttu-id="c625e-124">Exemples d’URL correspondantes</span><span class="sxs-lookup"><span data-stu-id="c625e-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="c625e-125">Correspond à une URL qui utilise le schéma http.</span><span class="sxs-lookup"><span data-stu-id="c625e-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="c625e-126">Correspond à une URL qui utilise le schéma http, sur n’importe quel hôte, à condition que le chemin commence par</span><span class="sxs-lookup"><span data-stu-id="c625e-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="c625e-127">Correspond à une URL qui utilise le schéma https, qui se trouve sur un `google.com` hôte \ (par exemple `www.google.com` , `docs.google.com` ou `google.com` \), à condition que le chemin commence par `/foo` et se termine par</span><span class="sxs-lookup"><span data-stu-id="c625e-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="c625e-128">Correspond à l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c625e-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="c625e-129">Correspond à tout fichier local dont le chemin commence par</span><span class="sxs-lookup"><span data-stu-id="c625e-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="c625e-130">Correspond à une URL qui utilise le `http` schéma et est sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c625e-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="c625e-131">Correspond à une URL qui commence par `http://mail.google.com` or `https://mail.google.com` .</span><span class="sxs-lookup"><span data-stu-id="c625e-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="c625e-132">Correspond à une URL qui utilise un schéma autorisé.</span><span class="sxs-lookup"><span data-stu-id="c625e-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="c625e-133">\ (Voir le début de cette section pour obtenir la liste des schémas autorisés. \)</span><span class="sxs-lookup"><span data-stu-id="c625e-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="c625e-134">Voici quelques exemples de `_invalid_` correspondances de modèles:</span><span class="sxs-lookup"><span data-stu-id="c625e-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="c625e-135">Modèle incorrect</span><span class="sxs-lookup"><span data-stu-id="c625e-135">Bad pattern</span></span> | <span data-ttu-id="c625e-136">Pourquoi il est défectueux</span><span class="sxs-lookup"><span data-stu-id="c625e-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="c625e-137">Non</span><span class="sxs-lookup"><span data-stu-id="c625e-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="c625e-138">' `*` 'dans l’hôte peut être suivi uniquement par un' `.` 'ou' `/` '</span><span class="sxs-lookup"><span data-stu-id="c625e-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="c625e-139">Si' `*` 'est dans le `_host_` , il doit être le premier caractère</span><span class="sxs-lookup"><span data-stu-id="c625e-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="c625e-140">`_scheme_`Séparateur manquant \ (' `/` 'doit être " `//` " \)</span><span class="sxs-lookup"><span data-stu-id="c625e-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="c625e-141">Invalid</span><span class="sxs-lookup"><span data-stu-id="c625e-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="c625e-142">Certains schémas ne sont pas pris en charge dans tous les contextes.</span><span class="sxs-lookup"><span data-stu-id="c625e-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="c625e-143">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c625e-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c625e-144">La page d’origine est disponible [ici](https://developer.chrome.com/extensions/match_patterns/).</span><span class="sxs-lookup"><span data-stu-id="c625e-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns/).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="c625e-146">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c625e-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
