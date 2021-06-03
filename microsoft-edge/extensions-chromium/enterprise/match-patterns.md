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
# <a name="match-patterns"></a>Correspondance des modèles

Les autorisations d’hôte et la correspondance de script de contenu sont basées sur un ensemble d’URL définies par des modèles de correspondance.  Un modèle de correspondance est essentiellement une URL qui commence par un schéma autorisé ( , , ou , et qui peut contenir `http` `https` ' ' ' `file` `ftp` `*` caractères.  Le modèle spécial `<all_urls>` correspond à toute URL qui commence par un schéma autorisé.  Chaque modèle de correspondance possède 3 parties :  

*   _schéma_ , par exemple, `http` `file` ou `*`  

> [!NOTE]
> L’accès `file` aux URL n’est pas automatique.  L’utilisateur doit visiter la page de gestion des extensions et choisir d’accéder à `file` chaque extension qui le demande.  

*   `_host_` — par exemple, `www.google.com` ou ; si le schéma est un `*.google.com` `*` fichier, il n’y a pas de partie hôte.  
*   `_path_` — par exemple, `/*` , `/foo*` ou `/foo/bar` .  Le chemin d’accès doit être présent dans une autorisation d’hôte, mais il est toujours traité comme `/*` .  

Syntaxe de base :  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

La signification varie selon qu’il se trouve dans le `*` schéma, l’hôte ou le chemin d’accès.  Si le schéma est `*` , il correspond à l’une ou `http` `https` l’autre ou `file` non, ou `ftp` .  Si l’hôte est `*` juste, il correspond à n’importe quel hôte. Si l’hôte est , il correspond à l’hôte spécifié ou à l’un `*.hostname` des sous-domaine.  Dans la section chemin d’accès, `*` chaque caractère correspond à 0 caractère ou plus.  Le tableau suivant présente certains modèles valides.  

| Modèle | Ce qu’il fait | Exemples d’URL correspondantes |  
|:--- |:--- |:--- |  
| `http://*/*` | Correspond à n’importe quelle URL qui utilise le schéma http | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Correspond à toute URL qui utilise le schéma http, sur n’importe quel hôte, tant que le chemin commence par `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Correspond à toute URL qui utilise le schéma https, se trouve sur un hôte `google.com` \(par `www.google.com` `docs.google.com` exemple, , ou `google.com` \), tant que le chemin d’accès commence par et `/foo` se termine par `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Correspond à l’URL spécifiée | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Correspond à tout fichier local dont le chemin d’accès commence par `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Correspond à toute URL qui utilise le `http` schéma et qui se trouve sur l’hôte `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Correspond à n’importe quelle URL qui commence par `http://mail.google.com` ou `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Correspond à toute URL qui utilise un schéma autorisé. \(Voir le début de cette section pour obtenir la liste des schémas autorisés.\) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Voici quelques exemples de `_invalid_` correspondances de modèle :

| Modèle non bon | Pourquoi est-il mauvais ? |  
|:--- |:--- |  
| `http://www.foo.com` | Non `_path_` |  
| `http://*foo/bar` | ' `*` ' in the host can be followed only by a ' ' or ' ' `.` `/` ' |  
| `http://foo.*.bar/baz` | Si ' `*` ' ' est dans le , il doit `_host_` s’agit du premier caractère |  
| `http:/bar` | Séparateur `_scheme_` manquant \(' `/` ' doit être " `//` «\) |  
| `foo://*` | Invalid `_scheme_` |  

Certains schémas ne sont pas pris en charge dans tous les contextes.

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/match_patterns)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
