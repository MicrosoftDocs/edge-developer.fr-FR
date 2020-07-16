---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Référence aux codes de console courants et aux suggestions de correction
title: 'DevTools: codes d’erreur et d’état de la console'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils F12, devtools, codes de la console
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1daa4e2a02802763ad75db91d06bd785fea9ec08
ms.sourcegitcommit: 1e33cd41e5afb2e6dbdc19353011ff6c2b019f9c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2020
ms.locfileid: "10866063"
---
# Codes d’erreur et d’état de la console  

Cette référence vous permet d’interpréter les messages d’erreur et d’état de la [console](../console.md) DevTools.  Utilisez le tableau suivant pour rechercher les codes par leur préfixe \(dans lequel le «x» représente un chiffre entre 0&ndash;9\):

| Préfixe du code | Domaine | Description |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Stratégie de sécurité du contenu | Ressources bloquées par l’utilisation d’un en-tête HTTP `Content-Security-Policy`.  |  
| [CSS31xx](#css-codes) | Feuilles de style | Erreurs liées au *Web Open Font Format* \(WOFF\) et à la source de polices *Embedded OpenType* \(EOT\) et aux problèmes de serveur hôte.  |  
| [HTML1112-1300](#html-codes) | HTML | La plupart d’entre eux sont des codes hérités spécifiques aux concepts de Microsoft InternetExplorer, tels que le *Mode document* et l’ *Affichage de compatibilité*.  |  
| [HTML1400-1532](#html5-parser-warnings) | Analyse HTML5 | Avertissements de validation générés par l’analyseur HTML5.  |  
| [HTTP](#http-codes) | Erreurs et état du serveur | Codes renvoyés par des serveurs distants en réponse aux demandes HTTP.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | Erreurs de syntaxe JavaScript | Se produit lorsque la structure de l’une de vos instructions JavaScript enfreint une ou plusieurs règles syntaxiques.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | Erreurs d’exécution JavaScript | Se produit lorsque votre script tente d’exécuter une action que le système ne peut pas exécuter.  |  
| [SEC71xx](#security-codes) | Sécurité | Indique les conditions de sécurité appliquées par MicrosoftEdge, comme par exemple, le *Contenu mixte* et la *Protection contre le suivi*.  |  
| [SVG560x](#svg-codes) | Graphiques Vectoriels Adaptables (SVG) |  Le débogage SVG étendu n’est actuellement pas pris en charge, mais certains messages de la console sont fournis à des fins de débogage.  |  
| WebGL11_xxx | WebGL | Messages d’erreur du contexte WebGL.  Voir aussi les [Erreurs GLSL](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Erreurs lors de l’analyse et de la validation XML.  |  

## Codes CSP  

Les ressources bloquées par l’utilisation d’un en-tête HTTP `Content-Security-Policy` sont signalées via la console DevTools et, éventuellement, communiquées au serveur sous forme de rapport.

| Code | Message | Description | Suggestion de correction |
|:--- |:--- |:--- |:--- |
| CSP14301 | «Échec de l’analyse du \[type de stratégie\] car \<the reason for canceling the operation\>. La stratégie sera ignorée.» | Le type de stratégie de sécurité spécifié \(par exemple, script-src, base-uri\) a échoué en raison du motif identifié et sera ignoré.  | Assurez-vous de répertorier toutes les ressources requises d’un type spécifique dans une seule directive.  Par exemple, dans `script-src https://host1.com; script-src https://host2.com`, la deuxième directive sera ignorée.  L’exemple suivant indique correctement les deux origines comme étant valides: `script-src https://host1.com https://host2.com`.  |
| CSP14302 | «Échec de l’analyse de la source dans \[type de stratégie\] pour la directive \[type de directive\] à \[URL source\]. La source sera ignorée.»                                                         | La plupart des directives CSP nécessitent une ou plusieurs sources de contenu \(indiquant une URL à partir de laquelle le contenu peut être chargé\).  Cette erreur signale une stratégie avec une directive qui contient une URL source ayant échoué lors de l’analyse.  | Vérifiez la source de contenu \(le plus souvent une URL\) définie dans la directive spécifiée, que vous pouvez trouver dans le type de stratégie spécifié.  Corrigez ou remplacez l’URL source ou supprimez la directive.  <br /> *\*Votre stratégie doit inclure une directive de stratégie src par défaut, qui constitue un substitut pour les autres types de ressources lorsqu’ils ne disposent pas de leurs propres stratégies.* |
| CSP14303 | «La stratégie [type de stratégie] était vide». | Le type de stratégie \(par exemple, Content-Security-Policy dans l’en-tête HTTP\) est vide.  | Une référence rapide sur la configuration d’une stratégie de sécurité du contenu peut être trouvée sur [http://content-security-policy.com](http://content-security-policy.com).  |
| CSP14304 | «La source \[URL source\] inconnue pour la directive \[type de directive\] dans la source \[type de stratégie\] sera ignorée.» | Les sources du contenu approuvé et (\sûr\) dans la directive identifiée sont inconnues et seront ignorées.  | Vérifiez la source de contenu identifiée \(il s’agit souvent d’une URL\) pour vous assurer qu’elle est correcte.  |
| CSP14305 | «La source \[URL source\] non prise en charge pour la directive \[type de directive\] dans la source \[type de stratégie\] sera ignorée.» | La source \(URL, mot-clé ou données) répertoriée dans cette directive n’est pas prise en charge et sera ignorée.  | L’adresse du site source peut inclure un caractère générique facultatif \(le caractère astérisque, `*`\).  Par exemple, http://`*`. foo.com ou mail.foo.com:*.  Les hôtes sont séparés par des espaces.  Les sources peuvent également être des mots clés \(none, self, unsafe-inline et unsafe-eval sont tous pris en charge\) ou des données \(data:URIs, mediastream:URIs\).  |
| CSP14306 | «Aucune source indiquée pour la directive \[type de directive\] pour [\type de politique\]. Ce qui équivaut à utiliser ’aucun’ et empêchera le téléchargement de toutes les ressources de ce type.» | Donner une directive et ne répertorier aucune source d’accès sécurisé au contenu équivaut à ne pas autoriser le téléchargement des ressources du type spécifié dans la directive.  | Une source peut être un ou plusieurs noms d’hôtes ou adresses IP Internet, ainsi qu’un schéma d’URL et/ou un numéro de port facultatif.  |
| CSP14307 | «La source [URL source] était déjà fournie pour la directive \[type de directive\] pour \[type de stratégie\].» | Une source \(URL, mot-clé ou données\) en double a été répertoriée dans cette directive et sera ignorée.  | Supprimez la source en double identifiée.  |
| CSP14308 | «Échec de l’analyse de la directive dans \[type de stratégie \] à [nom de la directive].» | La directive identifiée a échoué.  Si vous souhaitez obtenir des instructions sur la rédaction de directives prises en charge, rendez-vous sur [http://content-security-policy.com](http://content-security-policy.com/).  | Les directives doivent être séparées par des points-virgules.  Par exemple, si vous avez une application qui charge toutes ses ressources à partir d’un réseau de distribution de contenu \(par exemple, `https://cdn.example.net`\), et que vous savez que vous n’avez pas besoin de contenu trame ou de plug-ins, votre stratégie peut ressembler à ce qui suit: `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` *\*Alors que les directives sont séparées par des points-virgules, les sources dans une directive ne doivent être séparées que par un espace.* |
| CSP14309 | «Directive inconnue dans \[nom de la directive\] dans \[type de stratégie\]. La directive sera ignorée.» | La directive définie dans la stratégie CSP est inconnue et sera ignorée.  | Si vous souhaitez obtenir une liste des protocoles pris en charge, rendez-vous sur [http://content-security-policy.com](http://content-security-policy.com/).  |
| CSP14310 | «Directive [nom de la directive] non prise en charge dans \[type de politique]. La directive sera ignorée.» | Une directive détectée au cours de l’analyse dans le type de stratégie \(par exemple, le champ d’en-tête `Content-Security-policy-Report-Only`\) n’est pas prise en charge et sera ignorée.  Si vous souhaitez obtenir une liste des directives prises en charge, rendez-vous sur [http://content-security-policy.com](http://content-security-policy.com/).  | Supprimez la directive non prise en charge.  **REMARQUE**: certaines directives ne sont pas prises en charge dans l’élément \<meta\> ou dans le champ d’en-tête `Content-Security-policy-Report-Only`.  |
| CSP14311 | «La directive \[nom de la directive\] était déjà fournie dans \[type de stratégie\]. La directive en double sera ignorée.» | Une directive en double a été détectée pendant l’analyse. La deuxième directive et ses expressions sources seront ignorées.  | Supprimez le script en double.  |
| CSP14312 | «La ressource a enfreint la directive [nom de la directive] dans [type de stratégie]: [URI cible].  La ressource sera bloquée.» | Dans cet exemple: «la ressource a enfreint la directive ’script-src ms-appx: data: ’unsafe-eval’ dans Host Defined Policy: inline script.  La ressource sera bloquée.» | Un script inline \(Uri cible\) a été bloqué en raison de la directive `'script-src ms-appx: data: 'unsafe-eval'` dans la stratégie ’host defined’.  <br /> Les auteurs doivent déplacer tous les scripts inline et styles out-of-line car l’agent utilisateur ne peut pas déterminer si un script en ligne a été injecté par un attaquant.  Supprimez les scripts inline et placez-les dans un fichier externe.  |
| CSP14313 | «La ressource a enfreint la directive [nom de la directive] dans [type de stratégie]: [URI cible].  La ressource ne sera pas bloquée car la stratégie est uniquement liée aux rapports.» | Une ressource enfreignant la directive spécifiée dans le champ d’en-tête `Content-Security-policy-Report-Only` a été détecté.  Comme il s’agit d’un type de stratégie `Report-Only`, la ressource ne sera pas bloquée.  | Déplacez la directive dans un champ d’en-tête Content-Security-policy si cette ressource doit être bloquée afin de protéger votre site.  |
| CSP14314 | «Échec de l’envoi du rapport de violation de stratégie à [uri de destination cible] en raison de [raison de l’annulation de l’opération].» | Un problème est survenu lors du signalement d’une violation de stratégie. La destination cible dans laquelle le rapport doit être envoyé et la raison pour laquelle il n’a pas été envoyé doivent être identifiées.  | La directive `report-uri` spécifie une URL dans laquelle un navigateur enverra des rapports lorsqu’une stratégie de sécurité de contenu est enfreinte.  *\*Ne peut pas être utilisé dans les balises \<meta\>.* |
| CSP14315 | «Échec de l’application de la directive de bac à sable dans [type de stratégie] car [raison de l’annulation de l’opération].» | La directive de bac à sable a échoué en raison des motifs spécifiés.  Cette directive impose des restrictions sur les actions que la page peut effectuer plutôt que sur les ressources que la page peut charger.  Si la directive de bac à sable est présente, la page est traitée comme si elle était chargée dans un iframe.  Elle peut empêcher les fenêtres contextuelles et les plug-ins et bloquer l’exécution de scripts.  | Conservez la valeur de bac à sable vide pour conserver toutes les restrictions en place, ou ajouter les valeurs: `allow-forms`, `allow-same-origin`, `allow-scripts` et `allow-top-navigation`.  *\*La directive de bac à sable n’est pas prise en charge dans l’élément \<meta\> ou dans le champ d’en-tête `Content-Security-policy-Report-Only`.* |
| CSP14316 | «L’évaluation du script est autorisée en raison du remplacement de l’hôte.» | Lorsque la directive `script-src` ou `default-src` est incluse, le script inline et `eval()` sont désactivés, sauf si vous spécifiez `unsafe-inline` et `unsafe-eval`, respectivement.  | `'unsafe-eval'` permet d’utiliser `eval()` et des méthodes similaires pour créer du code à partir de chaînes.  Vous devez inclure des guillemets simples.  ***REMARQUE**: c’est une opération risquée qui peut permettre à votre site web d’accéder à des vulnérabilités de script dans les sites.* |
| CSP14317 | «La trame [nom de la source] a été autorisée en raison du remplacement de l’hôte.» | La trame source identifiée a été autorisée en raison d’un remplacement défini dans la stratégie CSP de l’hôte.  | Une stratégie peut contenir une expression de source basé sur un nonce, ce qui signifie que la source ne peut être utilisée qu’une seule fois et que le serveur doit générer une nouvelle valeur pour la directive chaque fois qu’il transmet une stratégie.  Les nonces remplacent les restrictions dans la directive dans laquelle ils sont présents.  |

> [!NOTE]
> Microsoft Edge ne vérifie pas le type MIME d’une feuille de style pour les sites web se situant dans la zone de sécurité approuvée de l’utilisateur.  

## Codes CSS  

Ces erreurs sont présentées sous le format CSS31xx et sont liées à des problèmes de source de polices *Web Open Font Format* \(WOFF\) et *Embedded OpenType* \(EOT\) et de serveur hôte.  

| Code | Message | Description | Suggestion de correction |
|:--- |:--- |:--- |:--- |
| CSS3111 | «@font-face a rencontré une erreur inconnue» | Un problème inconnu s’est produit avec le format «Web Open Font Format (WOFF)» et la «policeEmbedded OpenType (EOT)» de la police des feuilles de style en cascade (CSS).  | Vérifiez la source des polices WOFF.  Essayez une autre règle font-face ou une autre source pour voir si le problème est toujours présent.  |
| CSS3112 | «échec de @font-face au contrôle d’intégrité WOFF» | La police Web Open Font Format \(WOFF\) est peut-être endommagée, incomplète ou le format est incorrect.  | Vérifiez la source des polices.  Essayez une règle font-face ou une autre source correcte pour voir si le problème est toujours présent.  |
| CSS3113 | «incompatibilité @font-face entre l’origine du document et la chaîne racine EOT» | La police ne peut pas être utilisée car l’URL \(rootstring\) de la police OpenType Embedded \(EOT\) ne correspond pas au domaine du document utilisant la police.  | La somme de contrôle de l’URL dans la chaine racine EOT est peut-être incorrecte, ce qui indique une URL endommagée ou altérée pour la police.  Vérifiez que la police est sous licence ou dispose des autorisations pour le site web sur lequel elle est utilisée.  |
| CSS3114 | «échec de @font-face au contrôle de l’autorisation d’intégration de OpenType.  L’autorisation doit pouvoir être installée.» | La règle font-face ne dispose pas des autorisations d’installation pour la page web active.  | Obtenez l’autorisation ou les licences appropriées pour intégrer la police.  |
| CSS3115 | «@font-face ne peut pas charger une police OpenType non valide». | La règle font-face n’est pas valide pour cette utilisation.  | Obtenez l’autorisation ou les licences pour la règle font-face actuelle et valide.  |
| CSS3116 | «@font-face a échoué à la demande d’origine croisée.  Aucun en-tête Access-Control-Allow-Origin.» | La police n’est peut-être pas configurée pour l’accès à plusieurs domaines.  | La police n’est pas comprise dans la même origine que le document.  Assurez-vous que l’hôte qui dessert la police autorise l’utilisation de cette police avec l’en-tête HTTP «Access-Control-autoriser-origine».                        |
| CSS3117 | «@font-face a échoué à la demande d’origine croisée.  L’accès aux ressources est restreint.» | L’en-tête «Access-Control-Allow-Origin» n’est peut-être pas configuré correctement ou l’hôte de police peut ne pas autoriser l’utilisation de cette police par votre page.  | Assurez-vous que la ressource dispose des autorisations appropriées et d’un en-tête de réponse HTTP correctement configuré qui a une origine d’accès inter-domaine sur l’hôte desservant les polices.  |
| CSS3118 | «Impossible de créer une feuille de style.  Il y a plus de \[maximum\] feuilles de style dans le document.» | MicrosoftEdge a créé plus de 4095objets de feuille de style au cours du processus de rendu de votre page.  | Il peut s’agir d’un processus JavaScript hors de contrôle ou d’une erreur de système de génération.  Réduisez le nombre d’objets de feuille de style en cours de génération.  |
| CSS3119 | «La requête de média ms-view-state a été supprimée.  Les requêtes de média -ms-view-state peuvent être altérées ou indisponibles pour les versions ultérieures à Windows 8.1.  Utilisez plutôt des requêtes de largeur maximale et minimale.» | Votre CSS contient une requête de média `-ms-view-state`.  | Utilisez la largeur maximale et minimale.  |

## Codes HTML

Ces codes sont présentés sous le format HTML1xxx, par exemple, HTML1115.  Beaucoup d’entre eux sont des codes hérités spécifiques aux concepts d’Internet Explorer tels que le *Mode document* et l’*Affichage de compatibilité*  

| Code | Message | Description | Suggestion de correction |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | «Redémarrage de la page de code de \[codage\] à \[codage\] » | Une page de code qui diffère de la page de code du serveur a été spécifiée.  | Utilisez la même page de code que le serveur pour éviter cette erreur.  |  
| HTML1113 | «Redémarrage du mode document de \[mode\] à \[mode\]» | La page web nécessite un mode document différent de celui actuellement affecté au navigateur.  | Ce message peut se produire lorsque l’utilisateur navigue à partir d’une autre page, ce qui le rend hors du contrôle du développeur.  |  
| HTML1114 | «La page de code \[codage\] du \[domaine\] remplace la page de code \[codage\] conflictuelle du \[domaine\]» | Les pages de codes spécifiées dans les en-têtes HTTP \(du serveur\) et HTML \(dans la page\) sont différentes.  | Modifiez-en une afin qu’elles correspondent.  |  
| HTML1115 | «La balise META compatible X-UA \(`[META tag]`\) est ignorée car le mode document est déjà finalisé» | En règle générale, la balise META est placée après une déclaration «Script» ou «Style», qui corrige le mode document pour la page.  | Déplacez la balise META compatible X-UA le plus possible vers l’en-tête.  Il est recommandé de la placer immédiatement après la valeur \<title\> et de jeu de caractères.  |  
| HTML1116 | «La Balise META compatible X-UA \(`[META tag]`\) est ignorée en raison d’une balise META compatible X-UA antérieure \(`[META tag]`\)» | Il existe plusieurs balises «META» «X-UA-Compatible » dans la section \<head\> du code source.  | Supprimez toutes les balises « META X-UA-Compatible » sauf une, et assurez-vous qu’elle apparaisse le plus tôt possible dans l’en-tête.  Il est recommandé de la placer immédiatement après la valeur \<title\> et de jeu de caractères.  |  
| HTML1121 | «La page de code \[codage\] n’est pas autorisée, seule la page de code \[codage\] est autorisée.» | Le contenu de la page web a invoqué un codage de caractères non autorisé dans ce contexte.  | Assurez-vous que tout le contenu utilise l’encodage autorisé spécifié dans le message.  |  
| HTML1122 | «Internet Explorer s’exécute en mode Entreprise en émulant IE8» | La page est actuellement affichée en mode Entreprise, une émulation de WindowsInternetExplorer8.  | Ce mode est configuré par la gestion informatique pour les sites spécifiques.  Si un utilisateur individuel doit le désactiver sur une page web, désactivez l’option mode Entreprise dans le menu Outils.  Si vous souhaitez obtenir plus d’informations sur la gestion du mode Entreprise, consultez la [documentation informatique](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | «`[domain]` est un site web que vous avez ajouté à l’Affichage de compatibilité.» | L’utilisateur a sélectionné le bouton **Affichage de compatibilité** pour le site web actuel ou l’a ajouté via les **paramètres d’affichage de compatibilité**.  | Initié par l’utilisateur.  |  
| HTML1202 | «`[domain]` s’exécute en mode Affichage de compatibilité car «afficher les sites intranet dans Affichage de compatibilité» est activé.» | L’utilisateur a coché la case **Afficher les sites intranet dans Affichage de compatibilité** dans les **Paramètres de l’Affichage de compatibilité**.  | L’utilisateur doit appuyer sur ALT+T, sélectionner **Paramètres d’affichage de compatibilité**, puis décocher la case **Afficher les sites intranet dans Affichage de compatibilité**.  |  
| HTML1203 | «`[domain]` a été configuré pour s’exécuter dans Affichage de compatibilité via la stratégie de groupe.» | L’administrateur réseau a spécifié que la page web doit être exécutée dans Affichage de compatibilité.  | Vous devez contacter l’administrateur réseau.  |  
| HTML1204 | «`[domain]` s’exécute dans Affichage de compatibilité car «Afficher tous les sites web dans Affichage de compatibilité» est activé.» | L’utilisateur a coché la case **Afficher tous les sites web dans Affichage de compatibilité** dans les **Paramètres de l’Affichage de compatibilité**.  | L’utilisateur doit appuyer sur ALT+T, sélectionner **Paramètres d’affichage de compatibilité**, puis décocher la case **Afficher tous les sites web dans Affichage de compatibilité**.  |  
| HTML1300 | «Une navigation s’est produite» | Une nouvelle page a été parcourue ou la page actuelle a été actualisée.  | Il s’agit d’un message d’information, et non d’une erreur.  |  

## Avertissements de l’analyseur HTML5  

Les avertissements suivants peuvent se produire dans le cadre de la validation effectuée lors de l’analyse HTML.  Ces avertissements ne signifient pas nécessairement qu’une page est endommagée, mais que le code HTML fourni n’est pas validé par la norme HTML5.  Le contenu créé conformément aux versions antérieures des spécifications HTML ou XHTML peut ne pas être valide en HTML5, en particulier en ce qui concerne l’utilisation des DOCTYPE.

Ces avertissements indiquent généralement des caractères manquants ou supplémentaires et des balises incompatibles.  Lorsque vous résolvez ces avertissements, la compatibilité avec les anciens navigateurs et la conformité d’une page web avec la norme HTML5 doivent s’améliorer.  Pour aider à identifier la source d’un avertissement, des informations concernant le décalage de ligne et de caractère, ainsi qu’un lien pointant vers l’emplacement où le problème a été détecté sont inclus.

| Code     | Message |  
| :--- |:--- |  
| HTML1400 | «Caractère inattendu au début de la référence de caractère numérique.  Les caractères attendus sont compris entre [0-9].» |  
| HTML1401 | «Caractère inattendu au début de la référence de caractères numériques hexadécimal.  Les caractères attendus sont compris entre [0-9], [a-f] ou [A-F].» |  
| HTML1402 | «La référence de caractères ne comporte pas de point-virgule final «;».» |  
| HTML1403 | «La référence de caractères numériques ne se termine pas par un caractère valide». |  
| HTML1404 | «Référence de caractère nommée non reconnue.» |  
| HTML1405 | «Caractère non valide: U+0000 NULL.  Les caractères null ne doivent pas être utilisés.» |  
| HTML1406 | «Début de balise non valide: \<\?.  Les points d’interrogation ne doivent pas commencer les balises.» |  
| HTML1407 | «Nom de balise non valide.  Le premier caractère doit correspondre à [a-zA-Z]. |  
| HTML1408 | «Balise de fin \</\> non valide.  Les balises de fin ne doivent pas être vides.» |  
| HTML1409 | «Caractère de nom d’attribut non valide.  Les noms d’attributs ne doivent pas contenir \(\"\), \(\’\), \(\<\), ou \(=\).» |  
| HTML1410 | «Valeur d’attribut sans guillemet non valide.  Les valeurs d’attribut sans guillemet ne doivent pas contenir \(\"\), \(\’\), \(\<\), \(=\), ou \(\`\).» |  
| HTML1411 | «Fin de fichier inattendue.» |  
| HTML1412 | «Commentaire incorrect.  Les commentaires doivent commencer par \<\!-- \>.» |  
| HTML1413 | «Caractère inattendu: U+003E signe supérieur à \(\>\)» |  
| HTML1414 | «Caractère inattendu: U+0021 point d’exclamation \(\!\)» |  
| HTML1415 | «Caractère inattendu: U+002D trait d’union \(-\)» |  
| HTML1416 | «Caractère inattendu dans la fin du commentaire.  Les caractères attendus sont «--\>».» |  
| HTML1417 | «DOCTYPE vide.  Le doctype valide le plus court est \<\!DOCTYPE html\>.» |  
| HTML1418 | «Caractère inattendu dans le DOCTYPE.» |  
| HTML1419 | «Mot clé inattendu dans le DOCTYPE.  Le mot clé «PUBLIC» ou «SYSTEM» est attendu.» |  
| HTML1420 | «Guillemets inattendus après le mot clé «PUBLIC» ou «SYSTEM».  Un espace est attendu.» |  
| HTML1421 | «Balise de fin incorrecte.  Les balises de fin ne doivent pas contenir d’attributs.» |  
| HTML1422 | «Balise de début incorrecte.  Une barre oblique d’auto-fermeture doit être suivie d’un signe supérieur U+003E (\>\).» |  
| HTML1423 | «Balise de début incorrecte.  Les attributs doivent être séparés par des espaces.» |  
| HTML1424 | «Caractère non valide» |  
| HTML1500 | «Impossible de fermer automatiquement la balise.  Utilisez une balise de fermeture explicite.» |  
| HTML1501 | «Fin de fichier inattendue.» |  
| HTML1502 | «DOCTYPE inattendue.  Un seul DOCTYPE est autorisé et il doit apparaître avant tous les autres éléments.» |  
| HTML1503 | «Balise de début inattendue. » |  
| HTML1504 | «Balise de fin inattendue.» |  
| HTML1505 | «Jeton de caractères inattendu.» |  
| HTML1506 | «Jeton inattendu.» |  
| HTML1507 | «Caractère inattendu: U+0000 NULL.  Les caractères null ne doivent pas être utilisés.» |  
| HTML1508 | «Balise de fin sans correspondance.» |  
| HTML1509 | «Balise de fin sans correspondance.» |  
| HTML1510 | «Nœuds obligatoires hors de portée.» |  
| HTML1511 | «Élément de niveau head inattendu détecté en dehors de \<head\>.» |  
| HTML1512 | «Balise de fin sans correspondance.» |  
| HTML1513 | «Balise \<html\> supplémentaire détectée.  Une seule balise \<html\> doit exister par document.» |  
| HTML1514 | «Balise \<body\> supplémentaire détectée.  Une seule balise \<body\> doit exister par document.» |  
| HTML1515 | «\<frameset\> détectée trop loin dans le document.  Cette balise doit apparaître avant que \<body\> ne soit créée». |  
| HTML1516 | «Imbrication non valide.  Une balise d’en-tête telle que \<h1\> ou \<h2\> ne doit pas être placée dans une autre balise d’en-tête.» |  
| HTML1517 | «Imbrication non valide.  Une balise \<form\> ne doit pas être placée dans un autre balise \<form\>.» |  
| HTML1518 | «Imbrication non valide.  Une balise \<button\> ne doit pas être placée dans un autre balise \<button\>.» |  
| HTML1519 | «Imbrication non valide.  Une balise \<a\> ne doit pas être placée dans un autre balise \<a\>». |  
| HTML1520 | «Balise de début inattendue: l’élément \<isindex\> est obsolète et ne doit pas être utilisé.» |  
| HTML1521 | «\</body\> ou fin de fichier inattendue.  Tous les éléments ouverts doivent être fermés avant la fin du document.» |  
| HTML1522 | «Balise de fin non valide: \</br\>.  Utilisez plutôt \<br\> ou \<br /\>.» |  
| HTML1523 | «Les balises de fin se chevauchent.  Les balises doivent être structurées de cette façon: \<b\>\<i\>\</i\>\</b\> et non comme ceci: \<b\>\<i\>\</b\>\</i\>.» |  
| HTML1524 | «DOCTYPE non valide.  Le doctype valide le plus court est \<\!DOCTYPE html\>.» |  
| HTML1525 | «Balise HTML inattendue détectée dans le contenu étranger \(MathML/SVG\).» |  
| HTML1526 | «Imbrication non valide.  Une balise \<nobr\> ne doit pas être placée dans un autre balise \<nobr\>.» |  
| HTML1527 | «DOCTYPE attendu.  Le doctype valide le plus court est \<\!DOCTYPE html\>.» |  
| HTML1528 | «\<image\> inattendue dans le contenu HTML.  Utilisez plutôt \<img\>.» |  
| HTML1529 | «Valeur d’attribut xmlns:xlink non valide.  Cette valeur doit être «\<https://w3.org/1999/xlink\>».» |  
| HTML1530 | «Texte trouvé dans un élément de table structurelle.  Le texte de table ne peut être placé qu’à l’intérieur des éléments \<caption\>, \<td\> ou \<th\>.» |  
| HTML1531 | «Valeur d’attribut xmlns non valide.  Pour les éléments SVG, la valeur doit être «\<https://w3.org/2000/svg/\>».» |  
| HTML1532 | «Valeur d’attribut xmlns non valide.  Pour les éléments MathML, la valeur doit être «\<https://w3.org/1998/Math/MathML/\>».  |  

## Codes HTTP  

Les codes d’erreur HTTP sont renvoyés par les serveurs distants en réponse aux demandes.  Le plus connu est probablement HTTP404, qui est renvoyé chaque fois que le serveur ne trouve pas la page ou le document spécifié dans le Uniform Resource Identifier \(URI\).

| Code | Message | Description |  
| :--- |:--- |:--- |  
| HTTP400 | REQUÊTE INCORRECTE | La requête n’a pas pu être traitée par le serveur en raison d’une syntaxe non valide.  |  
| HTTP401 | REFUSÉ | La ressource demandée nécessite l'authentification des utilisateurs.  |  
| HTTP402 | PAIEMENT REQUIS | N’est pas intégré dans le protocole HTTP pour le moment.  |  
| HTTP403 | INTERDIT | Le serveur a compris la requête, mais refuse de l’exécuter.  |  
| HTTP404 | INTROUVABLE | Le serveur n’a trouvé aucun élément correspondant à l’URI demandé.  |  
| HTTP405 | MÉTHODE INCORRECTE | Le verbe HTTP utilisé n’est pas autorisé.  |  
| HTTP406 | AUCUNE RÉPONSE SATISFAISANTE | Aucune réponse satisfaisante pour le client n’a été trouvée.  |  
| HTTP407 | AUTHENTIFICATION PROXY REQUISE | Authentification proxy requise.  |  
| HTTP408 | EXPIRATION DU DÉLAI DE LA REQUÊTE | Le serveur a expiré lorsqu'il attendait la demande.  |  
| HTTP409 | CONFLIT | La requête n’a pas pu être traitée en raison d’un conflit avec l’état actuel de la ressource.  |  
| HTTP410 | INDISPONIBLE | La ressource demandée n’est plus disponible sur le serveur et aucune adresse de transfert n’est connue.  |  
| HTTP411 | LONGUEUR OBLIGATOIRE | Le serveur refuse d’accepter la requête sans une longueur de contenu définie.  |  
| HTTP412 | ÉCHEC DE LA CONDITION PRÉALABLE | La condition préalable indiquée dans un ou plusieurs des champs d’en-tête de la demande a été évaluée sur false lorsque celle-ci a été testée sur le serveur.  |  
| HTTP413 | CHARGE UTILE TROP GRANDE | Le serveur refuse de traiter une requête, car l’entité de la celle-ci est plus grande que celle que le serveur est prêt à traiter ou en mesure de traiter.  |  
| HTTP414 | URI TROP LONG | Le serveur refuse de répondre à la requête, car l’URI de celle-ci est trop long pour être interprété par le serveur.  |  
| HTTP415 | TYPE DE MÉDIA NON PRIS EN CHARGE | Le serveur refuse de répondre à la requête, car l’entité de la demande est présentée sous un format non pris en charge par la ressource demandée pour la méthode demandée.  |  
| HTTP416 | PLAGE DEMANDÉE NON RÉALISABLE | Le serveur ne peut pas fournir la partie du fichier demandée par le client.  La partie peut s’étendre au-delà de la fin du fichier.  |  
| HTTP417 | ÉCHEC DE L’ATTENTE | Le serveur ne répond pas aux exigences du champ d’en-tête de demande attendu.  |  
| HTTP418 | JE SUIS UNE THÉIÈRE | Le serveur est une théière. Il ne peut pas préparer de café.  |  
| HTTP419 | EXPIRATION DU DELAI DE L’AUTHENTIFICATION | L’authentification précédemment valide a expiré.  |  
| HTTP422 | ENTITÉ IMPOSSIBLE À TRAITER | La demande a été correctement construite, mais n’a pas pu être traitée en raison d’erreurs sémantiques.  |  
| HTTP423 | VERROUILLÉ | La ressource consultée est verrouillée.  |  
| HTTP424 | ÉCHEC DE LA DÉPENDANCE | La demande a échoué en raison de l’échec d’une demande précédente.  |  
| HTTP426 | MISE À NIVEAU REQUISE | Le client doit basculer vers un autre protocole.  |  
| HTTP428 | CONDITION PRÉALABLE REQUISE | Le serveur d’origine requiert une demande conditionnelle.  |  
| HTTP429 | NOMBRE DE REQUÊTES TROP ÉLEVÉ | Le serveur refuse de traiter la requête, car un trop grand nombre de demandes ont été envoyées par le client.  |  
| HTTP431 | CHAMPS D’EN-TÊTE DE REQUÊTE TROP VOLUMINEUX | Le serveur refuse de répondre à la requête, car un champ d’en-tête, ou tous les champs d’en-tête, sont trop volumineux pour être traités par le serveur.  |  
| HTTP449 | RÉESSAYEZ AVEC | La demande doit être retentée après avoir effectué l’action appropriée.  |  
| HTTP500 | ERREUR DU SERVEUR | Le serveur a rencontré une condition inattendue l’empêchant de répondre à la demande.  |  
| HTTP501 | NON PRIS EN CHARGE | Le serveur ne prend pas en charge la fonctionnalité requise pour répondre à la demande.  |  
| HTTP502 | PASSERELLE INCORRECTE | Le serveur, tout en agissant en tant que passerelle ou proxy, a reçu une réponse non valide du serveur en amont auquel il a accédé pour tenter de répondre à la demande.  |  
| HTTP503 | SERVICE NON DISPONIBLE | Le service est temporairement surchargé.  |  
| HTTP504 | EXPIRATION DU DÉLAI DE LA PASSERELLE | La demande a expiré pendant l’attente d’une passerelle.  |  
| HTTP505 | VERSION NON PRISE EN CHARGE | Le serveur ne prend pas en charge ou refuse la prise en charge de la version du protocole HTTP utilisée dans le message de demande.  |  
| HTTP506 | RÉFÉRENCE CIRCULAIRE | La négociation transparente du contenu de la demande a donné lieu à des références circulaires.  |  
| HTTP507 | ESPACE INSUFFISANT | Le serveur ne peut pas stocker la représentation nécessaire pour terminer la demande.  |  
| HTTP508 | BOUCLE DÉTECTÉE | Le serveur a détecté une boucle infinie lors du traitement de la demande.  |  
| HTTP510 | NON ÉTENDU | Des extensions supplémentaires à la demande sont nécessaires pour que le serveur puisse y répondre.  |  
| HTTP511 | AUTHENTIFICATION RÉSEAU REQUISE | Le client doit s’authentifier pour accéder au réseau.  |  

## Erreurs de syntaxe JavaScript  

Des erreurs de syntaxe JavaScript se produisent lorsque la structure de l’une de vos instructions enfreint une ou plusieurs règles syntaxiques.  

| Numéro d’erreur | Description |  
| --- | --- |  
| 1019 | [Il ne peut pas y avoir d’instruction «break» en dehors de la boucle](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | [Il ne peut pas y avoir d’instruction «continue» en dehors de la boucle](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [La compilation conditionnelle est désactivée](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | [«default» ne peut apparaître qu’une seule fois dans une instruction «switch»](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [Le caractère attendu est «\(»](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [Le caractère attendu est «\)»](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | [Le caractère attendu est «/»](/scripting/javascript/misc/expected-minus) |  
| 1003 | [Le caractère attendu est «:»](/scripting/javascript/misc/expected-colon) |  
| 1004 | [Le caractère attendu est «;»](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | [Le caractère attendu est «@»](/scripting/javascript/misc/expected-at) |  
| 1029 | [Le caractère attendu est «@end»](/scripting/javascript/misc/expected-at-end) |  
| 1007 | [Le caractère attendu est «\]»](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | [Le caractère attendu est «{»](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | [Le caractère attendu est «}»](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [Le caractère attendu est «=»](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | [«catch» est attendu](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Constante attendue](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Chiffre hexadécimal attendu](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Identificateur attendu](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Identificateur, chaîne ou nombre attendu](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | [«while»attendu](/scripting/javascript/misc/expected-while) |  
| 1014 | [Caractère non valide](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Étiquette introuvable](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Étiquette redéfinie](/scripting/javascript/misc/label-redefined) |  
| 1018 | [Instruction «return» en dehors de la fonction](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Erreur de syntaxe](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | [Throw doit être suivi d’une expression sur la même ligne source](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Commentaire inachevé](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Constante de chaîne non terminée](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Erreurs d’hôte de script  

Les erreurs suivantes concernent l’hôte de script, mais vous pouvez les voir occasionnellement:  
  
| Erreur | HRESULT | Description |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Une erreur a été enregistrée et transmise entre le moteur de script et l’hôte.  L’hôte doit transmettre le code d’erreur à l’appelant.  |  
| SCRIPT_E_REPORTED | 0x80020101 | Le moteur de script a signalé une exception non prise en charge à l’hôte via IActiveScriptSite::OnScriptError.  L’hôte peut ignorer cette erreur.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Une erreur de script propagée à l’appelant peut se trouver dans un autre thread.  L’hôte doit transmettre le code d’erreur à l’appelant.  |  

## Erreurs d’exécution JavaScript

Des erreurs d’exécution javaScript se produisent lorsque votre script tente d’exécuter une action que le système ne peut pas exécuter.  Vous pouvez rencontrer des erreurs d’exécution lorsque des expressions de variables sont évaluées ou lorsque la mémoire est attribuée.

| Numéro d’erreur | Description |  
| --- | --- |  
| 5 | [L’accès est refusé](/scripting/javascript/misc/access-is-denied) |  
| 438 | [L’objet ne prend pas en charge cette propriété ou méthode](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Mémoire insuffisante |  

### Erreurs Windows Runtime  

 Si vous utilisez des API Windows Runtime \(WinRT\), vous pouvez rencontrer des erreurs JavaScript qui ont été converties à partir des valeurs HRESULT de Windows Runtime.  Les valeurs HRESULT de Windows Runtime supérieures à 0x80070000 sont converties en erreurs JavaScript en prenant la valeur hexadécimale des bits faibles et en la convertissant en une valeur décimale.  Par exemple, la valeur HRESULT 0x80070032 est convertie en valeur décimale 50 et l’erreur JavaScript est nommée SCRIPT50.  La valeur HRESULT 0x80074005 est convertie en valeur décimale 16389 et l’erreur JavaScript est nommée SCRIPT16389.

| Numéro d’erreur | Description |  
| --- | --- |  
| 5029 | [La longueur du tableau doit être un entier positif fini](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [La longueur du tableau doit recevoir un nombre positif fini](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Objet tableau ou arguments attendu](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Valeur booléenne attendue](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [Impossible d’attribuer à un résultat de fonction](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [Impossible d’assigner à «ceci»](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Référence circulaire dans l’argument valeur non prise en charge](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Objet date attendu](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Objet énumérateur attendu](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Exceptions thrown et not caught](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Le caractère «)» est attendu dans l’expression régulière](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [Le caractère «&#93;» est attendu dans l’expression régulière](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [La fonction ne possède pas d’objet prototype valide](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Fonction attendue](/scripting/javascript/misc/function-expected) |  
| 5008 | [Affectation non conforme](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Plage non valide dans le jeu de caractères](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Argument de remplacement non valide](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [Objet JavaScript attendu](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Nombre attendu](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objet attendu](/scripting/javascript/misc/object-expected) |  
| 5012 | [Objet membre attendu](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Objet expression régulière attendu](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Chaîne attendue](/scripting/javascript/misc/string-expected) |  
| 5017 | [Erreur de syntaxe dans l’expression régulière](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [Le nombre de chiffres fractionnaires dépasse la plage](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [La précision dépasse la plage](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [L’URI à décoder n’est pas un encodage valide](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [L’URI à coder contient un caractère non valide](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Identificateur non défini](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Quantificateur inattendu](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [VBArray attendu](/scripting/javascript/misc/vbarray-expected) |  

## Codes de sécurité

Les codes d’erreur de sécurité sont présentés sous le format `SEC7xxx`, tels que `SEC7113`.  Ces erreurs indiquent les conditions de sécurité que MicrosoftEdge applique, telles que le contenu mixte et la protection contre le suivi.

| Code | Message | Description | Suggestion de correction |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | «La sécurité HTTPS est compromise par [nom de la ressource]» | Une page (\HTTPS\) (Secure Hypertext Transfer Protocol) présente du contenu provenant d’une source non sécurisée.  | Assurez-vous que tout le contenu de la page, y compris les scripts, les objets de feuille de style et les images, proviennent de sources HTTPS.  |  
| SEC7112 | «Le script de [URL] a été bloqué en raison d’une incompatibilité de type MIME» | L’en-tête de réponse HTTP pour le fichier JavaScript spécifié par l’URL dispose d’un en-tête «X-Content-Type-Options: nosniff» et n’a pas de déclaration de type de contenu reconnu.  | Mettez à jour le serveur pour envoyer le type de contenu correct pour le fichier JavaScript \(comme par exemple text/javascript, application/javascript»\) dans l’en-tête de réponse HTTP.  Pour obtenir plus d’informations et pour consulter la liste complète des types de contenu, consultez la page [Modifications de gestion MIME dans InternetExplorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | «Le CSS a été ignoré en raison d’une incompatibilité de type mime» | Une feuille de style importée n’a pas été utilisée car le mauvais type MIME était dans l’en-tête HTTP.  | Assurez-vous que le fichier de feuille de style est remis avec l’en-tête de réponse HTTP correct, qui inclut un type de contenu de text/css.  Pour obtenir plus d’informations, consultez la page [Modifications de gestion MIME dans InternetExplorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | «Un téléchargement sur cette page a été bloqué par la protection contre le suivi. [URL fournie ici]» | L’utilisateur a bloqué un script ou un contenu à l’aide de la protection contre le suivi.  | Aucune: initié par l’utilisateur.  |  
| SEC7115 | «Les styles :visited et :link ne peuvent différer que par leur couleur.  Certains styles n’ont pas été appliqués à:visited.» | Plusieurs attributs, tels que la police ou la taille, ont été modifiés à l’aide des styles visited et link.  | Modifiez uniquement l’attribut de couleur.  |  
| SEC7116 | «Accès refusé.  Échec de la révocation de l’URL d’origine croisée: [URL].» | Un script dont le site d’origine est différent du blob a tenté de révoquer une URL de blob.  En raison des stratégies d’origine des objets blob, la tentative a échoué.  | Assurez-vous que toutes les URL d’objets blob sont révoquées à l’aide de scripts provenant du même site d’origine que le document qui a créé l’URL de l’objet blob.  |  
| SEC7120 | «Origine du [domaine] introuvable dans l’en-tête Access-Control-Allow-Origin.» | Dans la réponse à votre XMLHttpRequest, l’en-tête Access-Control-Allow-Origin a été renvoyé avec une valeur qui ne contient pas ou ne correspond pas à la valeur d’origine de votre site.  | La ressource renvoie le type de codes d’en-tête approprié, mais n’autorise pas votre site.  Contactez le développeur responsable de la ressource et demandez-lui de mettre à jour son en-tête Access-Control-allow-Origin afin que votre site soit autorisé.  Vous pouvez le diriger vers la page [CORS pour XHR dans IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) pour plus d’informations sur CORS dans les en-têtes de réponse.  |  
| SEC7121 | «Le caractère générique dans Access-Control-Allow-Origin n’est pas autorisé lorsque l’indicateur des informations d’identification est défini sur true.» | Le serveur renvoie «Access-Control-allow-Origin: *» dans les en-têtes, mais cela n’est pas autorisé lorsque l’indicateur `withCredentials` est défini sur **true** dans le XMLHttpRequest.  | Le gestionnaire côté serveur doit être modifié pour renvoyer un en-tête Access-Control-autoriser-Origin qui autorise spécifiquement votre point d’origine sur ce type de demande.  Si vous ne contrôlez pas le gestionnaire côté serveur, vous devez contacter le développeur qui s’en charge.  |  
| SEC7122 | «L’indicateur des informations d’identification a été défini sur true, mais Access-Control-Allow-Credentials n’était pas présent ou n’a pas été défini sur «true.» | Un XMLHttpRequest a été créé à l’aide de l’`withCredentials`indicateur.  Les en-têtes Access-Control-autoriser-Credentials n’ont pas été renvoyés ou ont été renvoyés avec une valeur autre que **true**.  | Il se peut qu’il y ait un problème avec vos informations d’identification ou la réponse du serveur.  Pour obtenir plus d’informations sur les demandes d’informations d’identification, consultez la [spécification XMLHttpRequest de niveau2](https://w3.org/TR/XMLHttpRequest2/).  |  
| SEC7123 | «L’en-tête de demande [en-tête] n’était pas présent dans la liste Access-Control-Allow-Headers.» | Un type d’en-tête personnalisé a été inclus dans la demande, mais la liste Access-Control-Allow-Headers de la réponse ne l’a pas inclus.  | Assurez-vous que le serveur autorise les en-têtes personnalisés et autorise spécifiquement celui envoyé dans la demande.  |  
| SEC7124 | «La méthode [méthode] de demande n’était pas présente dans la liste Access-Control-Allow-Methods.» | Une méthode de demande, telle que POST, a été utilisée dans XMLHttpRequest, mais la réponse a renvoyé un en-tête Access-Control-Allow-Methods qui ne l’a pas inclus.  | Assurez-vous que le serveur autorise ce type de méthode et que vous utilisez correctement `withCredentials` si cette méthode a un accès limité.  |  
| SEC7125 | «XMLHttpRequest for [URL] a provoqué un échec d’analyse des en-têtes de réponse.» | Les en-têtes de réponse du serveur n’ont pas été analysés. La demande a donc échoué.  | Utilisez l’[outil réseau ](https://msdn.microsoft.com/library/dn255004.aspx) pour capturer et examiner les en-têtes de réponse afin de vous assurer qu’ils répondent aux [spécifications CORS](https://w3.org/TR/cors/).  |  
| SEC7126 | «Les redirections ne sont pas autorisées pour les demandes de contrôle en amont CORS.» | Une redirection a été détectée dans l’en-tête d’origine, et l’agent utilisateur ne suivra pas les redirections pendant un contrôle en amont.  | Utilisez l’ [outil réseau](https://msdn.microsoft.com/library/dn255004.aspx) pour capturer et examiner les en-têtes de demande et vérifier qu’il existe une seule origine directe.  |  
| SEC7127 | « La redirection a été bloquée pour la demande CORS.» | Le chemin d’accès à la ressource CORS contenait une redirection enfreignant les règles de sécurité.  | Assurez-vous que vous disposez du chemin le plus direct vers la ressource CORS dans votre XMLHttpRequest.  |  
| SEC7128 | «Plusieurs en-têtes Access-Control-Allow-Origin ne sont pas autorisés pour la réponse CORS.» | L’en-tête de réponse contenait plusieurs en-têtes Access-Control-Allow-Origin.  | Il s’agit d’une erreur côté serveur.  Le serveur doit renvoyer un seul en-tête Access-Control-Allow-Origin.  Signalez cette erreur au développeur responsable de la ressource côté serveur.
| SEC7129 | «Plusieurs en-têtes Access-Control-Allow-Credentials ne sont pas autorisés pour la réponse CORS.» | L’en-tête de réponse contenait plusieurs en-têtes Access-Control-Allow-Credentials.  | Il s’agit d’une erreur côté serveur.  Le serveur doit renvoyer un seul en-tête Access-Control-Allow-Credentials.  Signalez cette erreur au développeur responsable de la ressource côté serveur.  |  
| SEC7130 | «Des scripts intersites potentiels ont été détectés dans [URL].  Le contenu a été modifié par le filtre XSS.» | Le [filtre XSS](https://msdn.microsoft.com/library/dd565647.aspx) détecté un contenu potentiellement malveillant dans la réponse de la ressource et a supprimé le contenu incriminé.  | Découvrez le [Filtre XSS](https://msdn.microsoft.com/library/dd565647.aspx).  |  
| SEC7131 | «La sécurité d’un iframe en bac à sable est potentiellement compromise en autorisant l’accès au script et à la même origine.» | Si le contenu d’une iframe en bac à sable provient d’une source non fiable ou non sécurisée, il peut s’échapper du bac à sable lorsque le script et le même accès à l’origine sont tous deux autorisés.  | Il s’agit d’un message d’avertissement informatif qui ne doit pas affecter la fonctionnalité.  Il est recommandé de ne pas combiner ces autorisations, sauf si vous êtes certain de ce qui sera exécuté dans le iframe.  |  
| SEC7132 | «Le certificat protégeant ce site web utilise un chiffrement faible» | Le certificat de sécurité TLS utilisé par ce site web utilise un chiffrement faible | Mettez à jour le certificat TLS du serveur |  

> [!NOTE]
> Microsoft Edge ne vérifie pas le type MIME d’une feuille de style pour les sites web se situant dans la zone de sécurité approuvée de l’utilisateur.

## Codes SVG  

DevTools ne prend pas en charge le débogage extensif des Graphiques Vectoriels Adaptables \(SVG\), mais certains messages de la console sont fournis pour faciliter le débogage.

| Code | Message | Description | Suggestion de correction |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | «Les données du chemin d’accès SVG ont un format incorrect et n’ont pas pu être complètement analysées.» | La chaîne du [chemin d’accès](https://msdn.microsoft.com/library/ff972086.aspx) SVG n’est pas au bon format ou contient des commandes non reconnues.  | Vérifiez le format des commandes.  |  
| SVG5602 | «La liste des points SVG a un format incorrect et n’a pas pu être complètement analysée.» | La liste des points utilisés pour un élément, tel qu’un [polyligne](https://msdn.microsoft.com/library/ff972113.aspx), n’est pas dans le bon format.  | Assurez-vous que les points sont complets et dans le bon format pour le système de coordonnées des utilisateurs.  |  

## Codes XML  

Les codes XML sont présentés sous le format XML5xxx, par exemple, XML5603.  

| Code | Message |  
|:--- |:--- |  
| XML5001 | «Application de la gestion XSLT intégrée.» |  
| XML5601 | «MX_E_MX» |  
| XML5602 | «Fin d’entrée inattendue.» |  
| XML5603 | «Codage non reconnu.» |  
| XML5604 | «Impossible de changer l’encodage.» |  
| XML5605 | «Signature de codage d’entrée non reconnue.» |  
| XML5606 | «WC_E_WC» |  
| XML5607 | «Espace attendu. » |  
| XML5608 | «Point-virgule attendu.» |  
| XML5609 | Le caractère «>» est attendu.» |  
| XML5610 | «Guillemets attendus». |  
| XML5611 | Le caractère «=» est attendu.» |  
| XML5612 | «Le caractère< n’est pas autorisé dans les valeurs d’attributs.» |  
| XML5613 | «Chiffre hexadécimal attendu.» |  
| XML5614 | «Chiffre décimal attendu.» |  
| XML5615 | Le caractère «[» est attendu.» |  
| XML5616 | Le caractère «(» est attendu.» |  
| XML5617 | «Caractère XML non conforme.» |  
| XML5618 | «Caractère de nom non conforme.» |  
| XML5619 | «Syntaxe du document incorrecte.» |  
| XML5620 | «Syntaxe de la section CDATA incorrecte.» |  
| XML5621 | «Syntaxe du commentaire incorrecte.» |  
| XML5622 | «Syntaxe de la section conditionnelle incorrecte.» |  
| XML5623 | «Syntaxe de la déclaration ATTLIST incorrecte.» |  
| XML5624 | «Syntaxe de la déclaration DOCTYPE incorrecte.» |  
| XML5625 | «Syntaxe de la déclaration ELEMENT incorrecte.» |  
| XML5626 | ««Syntaxe de la déclaration ENTITY incorrecte.» |  
| XML5627 | «Syntaxe de la déclaration NOTATION incorrecte.» |  
| XML5628 | «NDATA» attendu.» |  
| XML5629 | «PUBLIC» attendu.» |  
| XML5630 | «SYSTEM» attendu.» |  
| XML5631 | «Nom non valide.» |  
| XML5632 | «Un seul élément racine est autorisé.» |  
| XML5633 | «Le nom de l’indicateur de fin ne correspond pas au nom de la balise de début correspondante.» |  
| XML5634 | «Un attribut portant le même nom existe déjà sur cet élément.» |  
| XML5635 | «Une déclaration XML n’est autorisée qu’au début du fichier.» |  
| XML5636 | «xml» de début.» |  
| XML5637 | «Syntaxe de déclaration de texte incorrecte.» |  
| XML5638 | «Syntaxe de déclaration XML incorrecte.» |  
| XML5639 | «Syntaxe de nom de codage incorrecte.» |  
| XML5640 | «Syntaxe d’identificateur public incorrecte.» |  
| XML5641 | «Les références d’entité de paramètre ne sont pas autorisées dans les déclarations de balisage dans un sous-ensemble de DTD interne.» |  
| XML5642 | «Le texte de remplacement des références d’entité de paramètre utilisé entre les déclarations de balisage doit contenir une série de déclarations de balisage complètes.» |  
| XML5643 | «Une entité analysée ne doit pas contenir de référence directe ou indirecte à elle-même.» |  
| XML5644 | «Le contenu de l’entité spécifiée n’est pas correct.» |  
| XML5645 | «L’entité spécifiée n’a pas été déclarée.» |  
| XML5646 | «La référence d’entité ne peut pas contenir le nom d’une entité non analysée.» |  
| XML5647 | «Les valeurs d’attribut ne doivent pas contenir de références directes ou indirectes à des entités externes.» |  
| XML5648 | «Syntaxe d’instruction de traitement incorrecte.» |  
| XML5649 | «Syntaxe de l’identificateur système incorrecte.» |  
| XML5650 | «Point d’interrogation attendu \(\?\).» |  
| XML5651 | «Le délimiteur CDATA-section-close «]]>» ne doit pas être utilisé dans le contenu de l’élément.» |  
| XML5652 | «Certains blocs de données n’ont pas été lus.» |  
| XML5653 | «La DTD a été trouvée mais est interdite.» |  
| XML5654 | «Attribut xml:space trouvé avec une valeur non valide.  Les valeurs valides sont «conserver» ou «par défaut».» |  
| XML5655 | «NC_E_NC» |  
| XML5656 | «Caractère de nom qualifié nom conforme.» |  
| XML5657 | «Plusieurs signes deux-points«:»ne doivent pas apparaître dans un nom qualifié.» |  
| XML5658 | «Un signe deux-points«:»ne doit pas apparaître dans un nom.» |  
| XML5659 | «Préfixe déclaré.» |  
| XML5660 | «Le préfixe spécifié n’a pas été déclaré.» |  
| XML5661 | «Les déclarations d’espace de noms non par défaut ne doivent pas avoir un URI vide.» |  
| XML5662 | «Le préfixe «xml» est réservé et doit avoir l’URI «<https://w3.org/XML/1998/namespace/>».» |  
| XML5663 | «Le préfixe «xmlns» est réservé pour une utilisation par XML.» |  
| XML5664 | «L’URI de l’espace de noms XML \(\<https://w3.org/XML/1998/namespace/\>\) doit uniquement être affecté au préfixe «xml».» |  
| XML5665 | «L’URI de l’espace de noms xmlns \(\<https://w3.org/2000/xmlns/\>\) est réservé et ne doit pas être utilisé.» |  
| XML5666 | «SC_E_SC» |  
| XML5667 | «Nombre maximal d’éléments imbriqués dépassé.» |  
| XML5668 | «Nombre maximal d’extension d’entité dépassé.» |  
| XML5669 | «WR_E_WR» |  
| XML5670 | «WR_E_NONWHITESPACE: writer: la chaîne spécifiée n’est pas un espace vide.» |  
| XML5671 | «WR_E_NONWHITESPACE: writer: le préfixe d’espace de noms est déjà déclaré avec un autre espace de noms.» |  
| XML5672 | «WR_E_NONWHITESPACE: writer: impossible d’utiliser un préfixe avec un URI d’espace de noms vide.» |  
| XML5673 | «WR_E_DUPLICATEATTRIBUTE: writer: attribut en double.» |  
| XML5674 | «WR_E_XMLNSPREFIXDECLARATION: writer: impossible de redéfinir le préfixe xmlns.» |  
| XML5675 | «WR_E_XMLPREFIXDECLARATION: writer: le préfixe xml doit avoir l’URI \<https://w3.org/XML/1998/namespace/\>.» |  
| XML5676 | «WR_E_XMLURIDECLARATION: writer: l’URI d’espace de noms XML \(\<https://w3.org/XML/1998/namespace/\>\) doit être affecté uniquement au préfixe «xml».» |  
| XML5677 | «WR_E_XMLNSURIDECLARATION: writer: l’URI de l’espace de noms xmlns \(\<https://w3.org/2000/xmlns/\>\) est réservé et ne doit pas être utilisé.» |  
| XML5678 | «WR_E_NAMESPACEUNDECLARED: writer: l’espace de noms n’est pas déclaré.» |  
| XML5679 | «WR_E_INVALIDXMLSPACE: writer: valeur non valide de l’attribut xml:space \(les valeurs autorisées sont «default» et «Preserve»\).» |  
| XML5680 | «WR_E_INVALIDACTION: writer: l’exécution de l’action demandée aurait pour résultat un document XML non valide.» |  
| XML5681 | «WR_E_INVALIDSURROGATEPAIR: writer: l’entrée contient une paire de substitution incomplète ou non valide.» |  
| XML5682 | «Caractère inattendu dans une entité de caractère.  Chiffre décimal attendu.» |  
| XML5683 | «Caractère inattendu dans une entité de caractère.  Chiffre hexadécimal attendu.» |  
| XML5684 | «La valeur Unicode de l’entité de caractère spécifiée est non valide.» |  
| XML5685 | «Codage non valide.» |  
| XML5686 | «Erreur XML non spécifiée.» |  
