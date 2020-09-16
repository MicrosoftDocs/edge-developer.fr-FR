---
description: Extensions de la documentation sur les stratégies d’entreprise pour le chrome.
title: Correspondance des modèles
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 59427769a010ca774833a809d3025e7594634202
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015659"
---
# Correspondance des modèles

Les autorisations d’hébergement et la correspondance de script de contenu sont basées sur un ensemble d’URL définies en fonction de critères de correspondance.  Un modèle match est essentiellement une URL qui commence par un schéma autorisé ( `http` ,,,,, `https` `file` `ftp` et qui peut contenir « `*` ».  Le modèle spécial `<all_urls>` correspond à toute URL qui commence par un schéma autorisé.  Chaque modèle de correspondance comporte 3 parties:  

*   _modèle_ , par exemple, `http` ou `file` `*`  

> [!NOTE]
> L’accès aux `file` URL n’est pas automatique.  L’utilisateur doit se rendre sur la page de gestion des extensions et sélectionner l' `file` accès pour chaque extension le demandant.  

*   `_host_` par exemple, `www.google.com` ou `*.google.com` ou `*` ; si le schéma est un fichier, il n’y a pas de partie hôte.  
*   `_path_` par exemple, `/*` `/foo*` ou `/foo/bar` .  Le chemin d’accès doit être présent dans une autorisation d’hôte, mais il est toujours traité comme `/*` .  

La syntaxe de base:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

La signification de `*` varie selon qu’il se trouve dans la partie schéma, hôte ou chemin.  S’il s’agit de la méthode `*` , elle correspond à la valeur `http` ou `https` , et non `file` , ou `ftp` .  S’il s’agit de l’hôte uniquement `*` , il correspond à n’importe quel hôte. S’il s’agit de l’hôte `*.hostname` , il correspond à l’hôte spécifié ou à l’un de ses sous-domaines.  Dans la section Path, chaque `*` caractère correspond à 0.  Le tableau suivant contient des modèles valides.  

| Agrément | Fonction | Exemples d’URL correspondantes |  
|:--- |:--- |:--- |  
| `http://*/*` | Correspond à une URL qui utilise le schéma http. | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Correspond à une URL qui utilise le schéma http, sur n’importe quel hôte, à condition que le chemin commence par `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Correspond à une URL qui utilise le schéma https, qui se trouve sur un `google.com` hôte \ (par exemple `www.google.com` , `docs.google.com` ou `google.com` \), à condition que le chemin commence par `/foo` et se termine par `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Correspond à l’URL spécifiée. | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Correspond à tout fichier local dont le chemin commence par `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Correspond à une URL qui utilise le `http` schéma et est sur l’hôte. `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Correspond à une URL qui commence par `http://mail.google.com` or `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Correspond à une URL qui utilise un schéma autorisé. \ (Voir le début de cette section pour obtenir la liste des schémas autorisés. \) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Voici quelques exemples de `_invalid_` correspondances de modèles:

| Modèle incorrect | Pourquoi il est défectueux |  
|:--- |:--- |  
| `http://www.foo.com` | Non `_path_` |  
| `http://*foo/bar` | ' `*` 'dans l’hôte peut être suivi uniquement par un' `.` 'ou' `/` ' |  
| `http://foo.*.bar/baz` | Si' `*` 'est dans le `_host_` , il doit être le premier caractère |  
| `http:/bar` | `_scheme_`Séparateur manquant \ (' `/` 'doit être " `//` " \) |  
| `foo://*` | Invalid `_scheme_` |  

Certains schémas ne sont pas pris en charge dans tous les contextes.

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/extensions/match_patterns/).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
