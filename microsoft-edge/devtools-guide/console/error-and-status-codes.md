---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Référence aux codes de console courants et aux suggestions de correction
title: DevTools-erreurs de la console et codes d’État
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, codes de console
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: aa667941f619dcc0eac2411a087dbdfcf2fda613
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566377"
---
# Code d’erreur et de statut de la console  

Cette référence vous permet d’interpréter les messages d’erreur et d’État à partir de la [console](../console.md)devtools.  Utilisez le tableau suivant pour trouver des codes en fonction du préfixe \ (où "x" représente&ndash;un numéro à 9 chiffres \):

| Préfixe de code | Zone | Description |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Stratégie de sécurité du contenu | Ressources bloquées lors de l’utilisation `Content-Security-Policy` d’un en-tête http.  |  
| [CSS31xx](#css-codes) | Feuilles de style | Erreurs liées au *format de police Web ouvert* (WOFF \) et aux problèmes *intégrés* de source de police et de serveur hôte.  |  
| [HTML1112-1300](#html-codes) | HTML | La plupart d’entre eux sont des codes hérités spécifiques aux concepts de Microsoft Internet Explorer tels que le *mode document* et le mode de *compatibilité*.  |  
| [HTML1400-1532](#html5-parser-warnings) | Analyse HTML5 | Avertissements de validation renvoyés par l’analyseur HTML5.  |  
| [HTTP](#http-codes) | Erreur et statut du serveur | Codes renvoyés par les serveurs distants en réponse aux requêtes HTTP.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | Erreurs de syntaxe JavaScript | Se produit lorsque la structure de l’une de vos instructions JavaScript enfreint une ou plusieurs règles syntaxiques.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | Erreurs d’exécution JavaScript | Se produit lorsque votre script essaie d’effectuer une action que le système ne peut pas exécuter.  |  
| [SEC71xx](#security-codes) | Sécurité | Indique les conditions de sécurité appliquées par Microsoft Edge, par exemple le *contenu mixte* et la *protection contre le suivi*.  |  
| [SVG560x](#svg-codes) | Graphiques vectoriels évolutifs |  Le débogage SVG complet n’est pas actuellement pris en charge, mais certains messages de console sont fournis à des fins de débogage.  |  
| WebGL11_xxx | WebGL | Messages d’erreur du contexte WebGL.  Voir aussi [Erreurs GLSL](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Erreurs dans l’analyse et la validation XML.  |  

## Codes CSP  

Les ressources bloquées lors de l' `Content-Security-Policy` utilisation d’un en-tête http sont communiquées par le biais de la console devtools et éventuellement sous forme de rapport au serveur.

| Code | Message | Description | Correction suggérée |
|:--- |:--- |:--- |:--- |
| CSP14301 | «Échec de l’analyse du \ [type de stratégie \], car \ <la raison pour laquelle vous annulez l’opération \ >--la stratégie sera ignorée.» | Le type de la stratégie de sécurité spécifiée \ (par exemple, script-SRC, base-URI \) a échoué pour la raison définie et sera ignorée.  | Assurez-vous d’afficher la liste de toutes les ressources requises d’un type spécifique dans une seule directive.  Par exemple, dans `script-src https://host1.com; script-src https://host2.com`, la deuxième directive sera ignorée.  Le code suivant spécifie correctement les deux origines `script-src https://host1.com https://host2.com`comme valides:.  |
| CSP14302 | «Échec de l’analyse de la source dans \ [type de stratégie \] pour la directive \ [type de directive \] dans \ [URL source \]--la source sera ignorée.»                                                         | La plupart des directives de FSC requièrent une ou plusieurs sources de contenu \ (indiquant une URL dans laquelle le contenu peut être chargé à partir de \).  Cette erreur pointe dans une stratégie avec une directive qui contient une URL source qui a échoué lors de la tentative d’analyse.  | Vérifiez que la source de contenu \ (il s’agit le plus souvent d’une URL \) qui est définie dans la directive spécifiée, que vous pouvez trouver dans le type de stratégie spécifié.  Corrigez ou remplacez l’URL source ou supprimez la directive.  <br /> *\ * Votre stratégie doit inclure une directive de stratégie de SRC par défaut, qui est un secours pour d’autres types de ressources quand ils ne possèdent pas de stratégies.* |
| CSP14303 | «[Type de la stratégie] est vide». | Le type de stratégie \ (par exemple, Content-Security-Policy dans l’en-tête HTTP) est vide.  | Pour plus d’informations sur la configuration d’une stratégie de sécurité du [http://content-security-policy.com](http://content-security-policy.com)contenu, voir.  |
| CSP14304 | "Source inconnue \ [URL source \] pour la directive \ [type de directive \] dans \ [type de stratégie \] source sera ignorée.» | Les sources de contenu approuvé \ (sécurisé \) dans la directive identifiées sont inconnues et sont ignorées.  | Vérifiez que la source de contenu identifiée \ (il s’agit généralement d’une URL \) pour vérifier qu’elle est correcte.  |
| CSP14305 | «Source non prise en charge \ [URL source \] pour la directive [type de directive] dans \ [type de stratégie \] source sera ignorée.» | La source \ (URL, mot clé ou données) répertoriée dans la directive n’est pas prise en charge et sera ignorée.  | L’adresse du site source peut inclure un caractère générique de début facultatif \ (astérisque, `*`\).  Par exemple, http://`*`. foo.com ou mail.foo.com: *.  Les hôtes sont séparés par des espaces.  Les sources peuvent également être des mots clés \ (aucune, auto, Insafe-Inline, et non-eval-eval sont tous pris en charge \) ou Data \ (Data: Uri, MediaStream: URI \)  |
| CSP14306 | "Pas de sources fournies pour la directive \ [type de directive \] pour \ [type de stratégie \]--cela équivaut à utiliser «aucune» et empêchera le téléchargement de toutes les ressources de ce type.» | La mise en forme d’une directive et non la mise en liste des sources de contenu sécurisé vers Access est identique à celle qui empêche le téléchargement de ressources du type spécifié dans la directive.  | Une source peut être un ou plusieurs noms d’hôtes Internet ou adresses IP, ainsi qu’un schéma d’URL et/ou un numéro de port facultatif.  |
| CSP14307 | «Source [URL source] a déjà été fournie pour la directive \ [type de directive \] pour \ [type de stratégie \].» | Une source dupliquée \ (URL, mot clé ou données \) a été répertoriée dans la directive et sera ignorée.  | Supprimez la source dupliquée identifiés.  |
| CSP14308 | Erreur «Échec de l’analyse syntaxique dans \ [type de la stratégie \] à [nom de la directive]». | La directive identifiée a échoué.  Pour obtenir des instructions sur la façon d’écrire des [http://content-security-policy.com](http://content-security-policy.com/)directives prises en charge, voir.  | Les directives doivent être séparées par des points-virgules.  Par exemple, si vous disposez d’une application qui charge toutes ses ressources à partir d’un réseau de distribution de contenu \ `https://cdn.example.net`(par exemple, \) et que vous savez que vous n’avez pas besoin de contenu tramé ou de plug- `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` ins, votre stratégie peut ressembler à ce qui suit: *\ * les directives sont séparées par des points-virgules.* |
| CSP14309 | «Directive inconnue dans \ [nom de la directive \] dans \ [type de stratégie \]--la directive sera ignorée.» | La directive définie dans la stratégie CSP est inconnue et sera ignorée.  | Pour obtenir la liste des directives prises en [http://content-security-policy.com](http://content-security-policy.com/)charge, voir.  |
| CSP14310 | «Directive non prise en charge [nom de la directive] dans \ [type de stratégie]--la directive sera ignorée.» | Une directive a été trouvée lors de l’analyse du type de stratégie \ (par exemple `Content-Security-policy-Report-Only` , le champ d’en-tête \) qui n’est pas pris en charge et sera ignorée.  Pour les directives prises en [http://content-security-policy.com](http://content-security-policy.com/)charge, voir.  | Supprimez la directive non prise en charge.  **Remarque**: certaines directives ne sont pas prises en charge dans l’élément \ <meta \ > `Content-Security-policy-Report-Only` ou dans le champ d’en-tête.  |
| CSP14311 | La directive \ [nom de directive \] a déjà été fournie dans \ [type de stratégie \]--la directive en double sera ignorée.» | Une directive dupliquée a été trouvée lors de l’analyse, la deuxième directive et ses expressions sources seront ignorées.  | Supprimez le script dupliqué.  |
| CSP14312 | «Ressource violée directive [nom de la directive] dans [type de stratégie]: [URI cible].  La ressource sera bloquée.» | Dans cet exemple: «ressources violées» script-src MS-AppX: Data: «unsafe-eval» dans la stratégie définie par l’hôte: script inline.  La ressource sera bloquée.» | Un script inline \ (Uri cible \) a été bloqué en raison de `'script-src ms-appx: data: 'unsafe-eval'` la directive de la stratégie «hote defined».  <br /> Les auteurs doivent déplacer tous les scripts et styles intralignes hors ligne, car l’agent utilisateur ne peut pas déterminer si un script inline a été injecté par un attaquant.  Supprimez le script en ligne et placez-le dans un fichier externe.  |
| CSP14313 | «Ressource violée directive [nom de la directive] dans [type de stratégie]: [URI cible].  La ressource ne sera pas bloquée en raison d’un rapport de stratégie uniquement. | Une ressource a été identifiée et ne respecte pas la directive `Content-Security-policy-Report-Only` spécifiée dans le champ d’en-tête.  Dans la mesure où il `Report-Only` s’agit d’un type de stratégie, la ressource ne sera pas bloquée.  | Dans le cas d’un champ d’en-tête de stratégie de sécurité du contenu, déplacez la directive si cette ressource doit être bloquée afin de protéger votre site.  |
| CSP14314 | «Impossible d’envoyer le rapport de violation de stratégie à [URI de destination cible], car [raison de l’annulation de l’opération].» | Un problème est survenu lors de la création d’un signalement d’une violation de stratégie, de la destination cible à l’endroit où le rapport doit être envoyé et de la raison pour laquelle vous ne pouvez pas l’envoyer.  | La `report-uri` directive spécifie une URL dans laquelle un navigateur envoie des rapports lorsque la stratégie de sécurité du contenu est violée.  *\ * Il ne peut pas être utilisé dans \ <méta \ > indicateurs.* |
| CSP14315 | «Échec de l’application de la stratégie de bac à sable dans [type de stratégie] car [raison de l’annulation de l’opération].» | La directive de bac à sable (sandbox) n’a pas pu être spécifiée.  La directive place les restrictions relatives aux actions qu’il est possible d’effectuer sur la page à la place de celles que la page peut charger.  S’il s’agit de la directive de bac à sable (sandbox), la page est traitée comme si elle était chargée dans un IFRAME.  Les fenêtres contextuelles et les plug-ins peuvent être évitées et bloquer l’exécution des scripts.  | Conservez la valeur de bac à sable (sandbox) pour conserver toutes les restrictions `allow-forms`en `allow-same-origin`vigueur `allow-scripts`ou ajouter `allow-top-navigation`des valeurs:,, et.  *La directive bac à sable (sandbox) n’est pas prise en charge dans l’élément \ <`Content-Security-policy-Report-Only` meta \ > ou dans le champ d’en-tête.* |
| CSP14316 | «Script eval autorisé en raison de la substitution d’hôte.» | `script-src` Lorsque la directive ou `default-src` est incluse, un script inline et `eval()` est désactivé sauf si vous `unsafe-inline` spécifiez et `unsafe-eval`, respectivement.  | `'unsafe-eval'` autorise l’utilisation de `eval()` méthodes similaires pour la création de code à partir de chaînes.  Vous devez inclure les guillemets simples.  ***Remarque**: cette opération n’est pas sûre et peut ouvrir votre site Web pour les failles de script entre sites. * |
| CSP14317 | «Frame [nom de la source] en raison d’un remplacement d’hôte.» | Le frame source identifié a été autorisé en raison d’un remplacement défini dans la stratégie de fournisseur de services cryptographiques de l’hôte.  | Une stratégie peut contenir une expression de source unique, ce qui signifie que la source peut être utilisée pour une seule fois et que le serveur doit générer une nouvelle valeur de la directive chaque fois qu’elle transmet une stratégie.  Nonces remplacer les restrictions de la directive dans lesquelles ils sont présents.  |

> [!NOTE]
> Sur les sites Web figurant dans la zone de sécurité approuvée d’un utilisateur, Microsoft Edge ne vérifie pas le type MIME d’une feuille de style.  

## Codes CSS  

Ces erreurs se trouvent dans le format CSS31xx et sont liées au *format de police Web ouvert* (WOFF \) et aux problèmes *intégrés* de source de police et de serveur hôte.  

| Code | Message | Description | Correction suggérée |
|:--- |:--- |:--- |:--- |
| CSS3111 | erreur «le @font a rencontré une erreur inconnue» | Un problème connu s’est produit avec le «Web Open font format \ (WOFF \)» et «police OpenType incorporée \ (EOT \)» de la police de feuille de style en cascade (CSS).  | Vérifier la source de polices WOFF.  Pour savoir si vous pouvez reproduire le problème, essayez les polices secondaires ou la source.  |
| CSS3112 | «@font-image a échoué vérification de l’intégrité WOFF» | Le format de la police Web ouvert (WOFF \) est peut-être endommagé ou incomplet.  | Vérifiez la source des polices.  Pour savoir si vous pouvez reproduire le problème, essayez une bonne police ou une source connue.  |
| CSS3113 | «incompatibilité @font-face entre l’origine du document et la chaîne racine EOT» | La police ne peut pas être utilisée car l’URL \ (rootstring \) dans la police OpenType \ (EOT \) imbriquée ne correspond pas au domaine du document en utilisant la police.  | Le checksum d’URL dans le rootstring EOT peut être incorrect, indiquant une URL endommagée ou altérée pour la police.  Vérifiez que la police est sous licence ou a des autorisations pour le site Web sur lequel elle est utilisée.  |
| CSS3114 | «la vérification d’autorisation d’incorporation OpenType dans le @font a échoué.  L’autorisation doit être installée.» | Ce type de police ne dispose pas des autorisations nécessaires pour procéder à l’installation avec la page Web actuelle.  | Obtenez les autorisations appropriées ou les licences d’incorporation de la police.  |
| CSS3115 | «@font ne peut pas charger la police OpenType non valide.» | La police n’est pas valide pour cette utilisation.  | Obtenez l’autorisation ou les licences pour les polices actuelles et valides.  |
| CSS3116 | @font "demande de non----------------  Aucun contrôle Access-Control-allow-Origin Header. | La police n’est peut-être pas configurée pour l’accès inter-domaines.  | La police n’est pas fournie à partir de la même origine que le document.  Assurez-vous que l’hôte qui dessert la police autorise l’utilisation de cette police à l’aide de l’en-tête HTTP «Access-Control-allow-Origin».                        |
| CSS3117 | @font "demande de non----------------  L’accès aux ressources est limité.» | L’en-tête «Access-Control-allow-Origin» n’est peut-être pas configuré correctement ou il est possible que l’hôte de polices ne puisse pas utiliser cette police pour votre page.  | Assurez-vous que la ressource possède les autorisations appropriées et un en-tête de réponse HTTP correctement configuré qui dispose d’une origine d’accès inter-domaines sur l’hôte qui dessert les polices.  |
| CSS3118 | "Échec de la création de la feuille de style.  Le document comporte plus de \ [maximum \] feuilles de style. | Microsoft Edge a créé plus de 4095 objets de la feuille de style lors du processus de rendu de votre page.  | Il peut s’agir d’un processus JavaScript hors contrôle ou d’une erreur du système de génération.  Réduisez le nombre d’objets StyleSheet générés.  |
| CSS3119 | «La requête multimédia-MS-View-State a été déconseillée.  les requêtes multimédias de MS-View-State peuvent être endommagées ou indisponibles pour les versions ultérieures à Windows 8,1.  Au lieu de cela, utilisez des requêtes de longueur maximale et de longueur minimale. " | Votre CSS contient une `-ms-view-state` requête multimédia.  | Utiliser la largeur maximale et la largeur minimale.  |

## Codes HTML

Ces codes sont au format HTML1xxx, par exemple, HTML1115.  La plupart de ces éléments sont des codes hérités spécifiques aux concepts d’Internet Explorer tels que le *mode document* et l' *affichage de compatibilité*  

| Code | Message | Description | Correction suggérée |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "CodePage redémarre à partir de \ [Encoding \] vers \ [Encoding \]" | Une page de codes de CodePage a été spécifiée et diffère de la page de CodePage du serveur.  | Utilisez la même page de codes en tant que serveur pour éviter cette erreur.  |  
| HTML1113 | "Le mode document redémarre à partir de \ [mode \] vers \ [mode \]" | La page Web nécessite un mode de document différent du mode de navigation actuel.  | Ce message peut s’afficher lorsque l’utilisateur parcourt une autre page, ce qui le rend hors du contrôle du développeur.  |  
| HTML1114 | "CodePage \ [Encoding \] from \ [Domain \] remplace en conflit la page de code \ [Encoding \] from \ [Domain \]" | Les pages de codes spécifiées dans les en-têtes HTTP \ (à partir du serveur \) et HTML \ (dans la page \) sont différentes les unes des autres.  | Changez-en un pour qu’il corresponde.  |  
| HTML1115 | «Balise META compatible X-UA-(`[META tag]`\) ignoré, car le mode document est déjà finalisé» | En règle générale, la balise META a été placée après une déclaration «script» ou «style», qui a résolu le mode de document de la page.  | Déplacez la balise META compatible X-UA sur le plus tôt dans l’en-tête que possible.  Nous vous conseillons de placer le fichier immédiatement après la valeur \ <titre \ > et CharSet.  |  
| HTML1116 | «Balise META compatible x-UA-(`[META tag]`\) ignoré en raison de la balise Meta compatible x-UA plus`[META tag]`ancienne \ (\)» | Il existe plusieurs balises «META» compatibles X-UA dans la section \ <Head \ > du code source.  | Supprimez toutes les balises méta compatibles X-UA, et assurez-vous que la première fois dans l’en-tête.  Nous vous conseillons de placer le fichier immédiatement après la valeur \ <titre \ > et CharSet.  |  
| HTML1121 | "CodePage \ [Encoding \] n’est pas autorisé, seule la CodePage [Encoding] est autorisée.» | Le contenu de la page Web a appelé un codage de caractères qui n’est pas autorisé dans ce contexte.  | Assurez-vous que tout le contenu utilise le codage autorisé spécifié dans le message.  |  
| HTML1122 | «Internet Explorer s’exécute en mode entreprise émulant IE8» | La page est actuellement affichée en mode entreprise, qui est une émulation de Windows Internet Explorer 8.  | Ce mode est configuré par la gestion informatique pour des sites spécifiques.  Si un utilisateur doit le désactiver sur une page Web, désactivez l’option mode entreprise du menu outils.  Pour plus d’informations sur la gestion du mode entreprise, consultez la documentation de l' [application](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | «`[domain]` est un site Web que vous avez ajouté à l’affichage de compatibilité.» | L’utilisateur a sélectionné le bouton **mode de compatibilité** pour le site Web actuel ou l’a ajouté via les paramètres d’affichage de **compatibilité**.  | Lancée par l’utilisateur.  |  
| HTML1202 | «`[domain]` s’exécute en mode de compatibilité, car «afficher les sites intranet en mode de compatibilité» est coché.» | La case à cocher Afficher les **sites intranet en mode de compatibilité** est activée dans les **paramètres d’affichage**de compatibilité.  | L’utilisateur doit appuyer sur ALT + T, sélectionner **paramètres du mode de compatibilité**, puis décochez la case Afficher les **sites intranet en mode de compatibilité** .  |  
| HTML1203 | "`[domain]` a été configuré pour s’exécuter en mode de compatibilité via une stratégie de groupe." | L’administrateur réseau a spécifié que la page Web soit exécutée en mode de compatibilité.  | Vous devez contacter l’administrateur réseau.  |  
| HTML1204 | «`[domain]` s’exécute en mode de compatibilité, car «afficher tous les sites Web en mode de compatibilité» est coché.» | L’utilisateur a sélectionné la case à cocher **Afficher tous les sites Web en mode de compatibilité** dans les **paramètres d’affichage**de compatibilité.  | L’utilisateur doit appuyer sur ALT + T, sélectionner **paramètres du mode de compatibilité**, puis désactivez la case à cocher **Afficher tous les sites Web en mode de compatibilité** .  |  
| HTML1300 | "Navigation s’est produite" | A accédé à une nouvelle page ou la page actuelle a été actualisée.  | Il s’agit d’un message d’information, sans erreur.  |  

## Avertissements de l’analyseur HTML5  

Les avertissements suivants peuvent se produire dans le cadre de la validation effectuée lors de l’analyse HTML.  Ces avertissements n’indiquent pas nécessairement qu’une page est endommagée, mais que le code HTML fourni n’est pas valide par la norme HTML5.  Le contenu créé conformément aux versions antérieures des spécifications HTML ou XHTML n’est peut-être pas valide en HTML5, en particulier en ce qui concerne l’utilisation de la fonction enctype.

En règle générale, ces avertissements indiquent des caractères manquants ou des balises inadaptées.  Lorsque vous résolvez ces avertissements, la compatibilité avec les navigateurs plus anciens et la conformité d’une page Web avec le standard HTML5 doivent s’améliorer.  Pour faciliter l’identification de la source d’un avertissement, il inclut des informations de décalage de lignes et de caractères, ainsi qu’un lien pointant vers l’emplacement où le problème a été détecté.

| Code     | Message |  
| :--- |:--- |  
| HTML1400 | "Caractère inattendu au début de référence de caractère numérique.  Attendue [0-9].» |  
| HTML1401 | "Caractère inattendu au début de référence de caractère numérique hexadécimal.  Vous pouvez vous attendre à ED [0-9], [a-f] ou [A-F]. |  
| HTML1402 | "La référence de caractère ne comporte pas de point-virgule fermant"; "." |  
| HTML1403 | «La référence de caractère numérique n’est pas résolue en caractère valide.» |  
| HTML1404 | "Référence de caractère nommé non reconnu." |  
| HTML1405 | "Caractère non valide: U + 0000 nul.  Les caractères null ne doivent pas être utilisés.» |  
| HTML1406 | "Début de la balise non valide: \ < \?.  Les points d’interrogation ne doivent pas commencer de balises.» |  
| HTML1407 | "Nom de balise non valide.  Le premier caractère doit correspondre à [a-zA-Z].» |  
| HTML1408 | "Balise de fin non valide \ </\ >.  Les balises de fin ne doivent pas être vides.» |  
| HTML1409 | "Caractère de nom d’attribut non valide.  Les noms d’attributs ne doivent pas contenir \ (\ "\), \ (\" \), \ (\ < \) ou \ (= \). " |  
| HTML1410 | "Valeur d’attribut sans guillemet non valide.  Les valeurs d’attribut sans guillemets ne doivent pas contenir \ (\ "\), \ (\" \), \ (\ < \), \ (= \) |  
| HTML1411 | «Fin inattendue du fichier». |  
| HTML1412 | "Commentaire incorrect.  Les commentaires doivent commencer par \ < \!--\ >.» |  
| HTML1413 | "Caractère inattendu: U + 003E supérieur à (\ > \)" |  
| HTML1414 | "Caractère inattendu: point d’exclamation U + 0021 \ (\! \)" |  
| HTML1415 | "Caractère inattendu: U + 002D trait d’Union-moins \ (-\)" |  
| HTML1416 | "Caractère inattendu dans la fin du commentaire.  "--\ >". " |  
| HTML1417 | "DOCTYPE vide.  Le doctype valide le plus court est \ < \. DOCTYPE html \ >.» |  
| HTML1418 | «Caractère inattendu dans DOCTYPE». |  
| HTML1419 | «Mot clé inattendu dans DOCTYPE.  «PUBLIC» ou «SYSTEM» attendus. |  
| HTML1420 | «Guillemet inattendu après le mot clé «PUBLIC» ou «SYSTEM».  Espace blanc attendu.» |  
| HTML1421 | «Balise de fin incorrecte.  Les balises de fin ne doivent pas contenir d’attributs.» |  
| HTML1422 | "Indicateur de début incorrect.  Une barre oblique automatique doit être suivie d’un symbole U + 003E supérieur au signe ^ (\ > \).» |  
| HTML1423 | "Indicateur de début incorrect.  Les attributs doivent être séparés par des espaces blancs.» |  
| HTML1424 | "Caractère non valide" |  
| HTML1500 | «La balise ne peut pas être fermée automatiquement.  Utiliser une balise de fermeture explicite.» |  
| HTML1501 | «Fin inattendue du fichier». |  
| HTML1502 | "DOCTYPE inattendu.  Un seul DOCTYPE est autorisé et il doit intervenir avant tout élément.» |  
| HTML1503 | «Balise de début inattendu». |  
| HTML1504 | «Balise de fin inattendue». |  
| HTML1505 | «Jeton de caractères inattendus». |  
| HTML1506 | «Jeton inattendu». |  
| HTML1507 | "Caractère inattendu: U + 0000 nul.  Les caractères null ne doivent pas être utilisés.» |  
| HTML1508 | «Balise end sans correspondance». |  
| HTML1509 | «Balise end sans correspondance». |  
| HTML1510 | "Nœuds requis non dans l’étendue." |  
| HTML1511 | «Élément de niveau inattendu rencontré en dehors de \ <Head \ >.» |  
| HTML1512 | «Balise end sans correspondance». |  
| HTML1513 | "Extra \ <> HTML de la balise.  Il n’y a qu’une seule \ <balise html \ > doit exister par document.» |  
| HTML1514 | «Extra \ <corps \ > balise trouvée.  Il n’y a qu’un seul > du corps de la balise \ <par document.» |  
| HTML1515 | «Nous avons trouvé le <de jeu de cadres \ > trop loin dans le document.  Cette balise doit se produire avant la création du > du corps \ <.» |  
| HTML1516 | «Imbrication non valide.  Une balise d’en-tête telle que \ <H1 \ > ou \ <H2 \ > ne doit pas être placée à l’intérieur d’une autre balise d’en-tête.» |  
| HTML1517 | «Imbrication non valide.  Une balise \ <de formulaire \ > ne doit pas être placée dans un autre formulaire \ <\ >.» |  
| HTML1518 | «Imbrication non valide.  Le > de la balise \ <ne doit pas être placé dans un autre bouton \ <\ >.» |  
| HTML1519 | «Imbrication non valide.  Un \ <une balise \ > ne doit pas être placé dans un autre \ <a \ >.» |  
| HTML1520 | «Balise de début inattendue: l’élément <ISINDEX \ > est déconseillé et ne doit pas être utilisé.» |  
| HTML1521 | "< > ou fin inattendue du fichier.  Tous les éléments ouverts doivent être fermés avant la fin du document.» |  
| HTML1522 | "Balise de fin non valide: \ </br\ >.  Utilisez \ <br \ > ou \ <br/\ > à la place.» |  
| HTML1523 | "Indicateur de fin chevauchant.  Les balises doivent être structurées comme \ <b \ > \ <j’ai > \ </i\ > \ </b\ > au lieu de \ </b\ \ > \ </i\ > |  
| HTML1524 | "DOCTYPE non valide.  Le doctype valide le plus court est \ < \. DOCTYPE html \ >.» |  
| HTML1525 | «Balise HTML inattendue trouvée dans le contenu étranger \ (MathML/SVG \).» |  
| HTML1526 | «Imbrication non valide.  Une balise \ <nobr \ > ne doit pas être placée dans un autre \ <nobr \ >.» |  
| HTML1527 | «DOCTYPE attendu.  Le doctype valide le plus court est \ < \. DOCTYPE html \ >.» |  
| HTML1528 | «Image \ <inattendue \ > du contenu HTML.  Utilisez \ <img \ > à la place. " |  
| HTML1529 | "Valeur d’attribut xmlns: XLink non valide.  La valeur doit être «\ <https://w3.org/1999/xlink\>». |  
| HTML1530 | "Texte détecté dans un élément de tableau structurel.  Le texte de tableau ne doit être placé qu’à l’intérieur \ <sous-titre \ >, \ <TD \ > ou \ <les éléments \ >.» |  
| HTML1531 | "Valeur d’attribut xmlns non valide.  Pour les éléments SVG, la valeur doit être « https://w3.org/2000/svg/\>\ <». |  
| HTML1532 | "Valeur d’attribut xmlns non valide.  Pour les éléments MathML, la valeur doit être « https://w3.org/1998/Math/MathML/\>\ <».  |  

## Codes HTTP  

Les codes d’erreur HTTP sont renvoyés par les serveurs distants en réponse aux demandes.  Le plus souvent, c’est HTTP404, qui est retourné chaque fois que le serveur ne parvient pas à trouver la page ou le document spécifié dans l’URI (Uniform Resource Identifier).

| Code | Message | Description |  
| :--- |:--- |:--- |  
| HTTP400 | DEMANDE INCORRECTE | La requête n’a pas pu être traitée par le serveur, car une syntaxe n’est pas valide.  |  
| HTTP401 | Verr | La ressource demandée nécessite une authentification de l’utilisateur.  |  
| HTTP402 | PAIEMENT OBLIGATOIRE | Non implémentée actuellement dans le protocole HTTP.  |  
| HTTP403 | INTERDITE | Le serveur a compris la demande, mais refuse de la remplir.  |  
| HTTP404 | introuvable | Le serveur n’a trouvé aucun élément correspondant à l’URI demandé.  |  
| HTTP405 | MÉTHODE INCORRECTE | Le verbe HTTP utilisé n’est pas autorisé.  |  
| HTTP406 | AUCUNE ACCEPTÉE | Aucune réponse acceptable pour le client n’a été trouvée.  |  
| HTTP407 | AUTHENTIFICATION DU PROXY REQUISE | Authentification du proxy requise.  |  
| HTTP408 | DÉLAI DE REQUÊTE | Le serveur a expiré en attente de la requête.  |  
| HTTP409 | SONT | La requête n’a pas pu être effectuée en raison d’un conflit avec l’état actuel de la ressource.  |  
| HTTP410 | TARD | La ressource demandée n’est plus disponible sur le serveur et aucune adresse de transfert n’est connue.  |  
| HTTP411 | LONGUEUR REQUISE | Le serveur refuse d’accepter la demande sans longueur de contenu définie.  |  
| HTTP412 | ÉCHEC DE LA CONDITION PRÉALABLE | La condition préalable fournie dans un ou plusieurs des champs d’en-tête de requête a évalué la valeur false lors du test sur le serveur.  |  
| HTTP413 | CHARGE UTILE TROP GRANDE | Le serveur refuse de traiter une demande, car l’entité de la requête est plus grande que le serveur disposé ou capable de traiter.  |  
| HTTP414 | URI TROP LONG | Le serveur refuse de traiter la demande, car l’URI de la demande est plus longue que le serveur n’est pas disposé à interpréter.  |  
| HTTP415 | TYPE DE MÉDIA NON PRIS EN CHARGE | Le serveur refuse de traiter la demande, car l’entité de la requête est dans un format non pris en charge par la ressource demandée pour la méthode demandée.  |  
| HTTP416 | PLAGE REQUISE NON SATISFIABLE | Le serveur ne peut pas fournir la partie du fichier demandée par le client.  La partie s’étend au-delà de la fin du fichier.  |  
| HTTP417 | ÉCHEC DE L’ATTENTE | Le serveur ne peut pas respecter les conditions du champ d’en-tête de demande.  |  
| HTTP418 | ENVOYER UN MESSAGE INSTANTANÉ À UN TEAPOT | Le serveur est un Teapot; le café ne peut pas être brassé.  |  
| HTTP419 | DÉLAI D’AUTHENTIFICATION | L’authentification précédemment valide a expiré.  |  
| HTTP422 | ENTITÉ NON TRAITÉE | La requête était bien formée mais n’a pas pu être traitée en raison d’erreurs sémantiques.  |  
| HTTP423 | VERROUILLER | La ressource consultée est verrouillée.  |  
| HTTP424 | DÉPENDANCE EN ÉCHEC | La requête a échoué en raison de l’échec d’une requête précédente.  |  
| HTTP426 | MISE À NIVEAU REQUISE | Le client doit basculer vers un autre protocole.  |  
| HTTP428 | CONDITION PRÉALABLE REQUISE | Le serveur d’origine exige que la demande soit conditionnelle.  |  
| HTTP429 | NOMBRE DE REQUÊTES TROP IMPORTANT | Le serveur refuse de traiter la demande, car un trop grand nombre de requêtes ont été envoyées par le client.  |  
| HTTP431 | CHAMPS D’EN-TÊTE DE DEMANDE TROP VOLUMINEUX | Le serveur refuse de traiter la demande, car un champ d’en-tête ou tous les champs d’en-tête collectivement sont plus volumineux que le serveur est disposé ou capable de traiter.  |  
| HTTP449 | RÉESSAYER AVEC | La requête doit être réessayée après avoir pris l’action appropriée.  |  
| HTTP500 | ERREUR DE SERVEUR | Le serveur a rencontré une condition inattendue qui l’a empêché de répondre à la demande.  |  
| HTTP501 | NON PRIS EN CHARGE | Le serveur ne prend pas en charge la fonctionnalité requise pour répondre à la demande.  |  
| HTTP502 | PASSERELLE INCORRECTE | Le serveur, en tant que passerelle ou proxy, a reçu une réponse non valide du serveur en amont auquel il a accédé en essayant de répondre à la demande.  |  
| HTTP503 | SERVICE INDISPONIBLE | Le service est temporairement surchargé.  |  
| HTTP504 | DÉLAI D’EXPIRATION DE LA PASSERELLE | Le délai d’expiration de la requête est écoulé en attendant une passerelle.  |  
| HTTP505 | VERSION NON PRISE EN CHARGE | Le serveur n’est pas pris en charge, ou refuse de prendre en charge, la version du protocole HTTP utilisée dans le message de requête.  |  
| HTTP506 | LA VARIANTE NÉGOCIE ÉGALEMENT | La négociation de contenu transparente pour la requête a entraîné des références circulaires.  |  
| HTTP507 | ESPACE DE STOCKAGE INSUFFISANT | Le serveur ne peut pas stocker la représentation nécessaire pour exécuter la requête.  |  
| HTTP508 | BOUCLE DÉTECTÉE | Le serveur a détecté une boucle infinie lors du traitement de la requête.  |  
| HTTP510 | NON ÉTENDU | D’autres extensions de la demande sont nécessaires pour que le serveur le remplit.  |  
| HTTP511 | AUTHENTIFICATION RÉSEAU REQUISE | Le client doit s’authentifier pour obtenir l’accès au réseau.  |  

## Erreurs de syntaxe JavaScript  

Des erreurs de syntaxe JavaScript se produisent lorsque la structure de l’une de vos instructions viole une ou plusieurs règles syntaxiques.  

| Numéro d’erreur | Description |  
| --- | --- |  
| 1019 | [Ne peut pas contenir de’Break’en dehors d’une boucle](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | [Impossible d’avoir’continue’en dehors d’une boucle](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [La compilation conditionnelle est désactivée](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | ['par défaut’peut uniquement apparaître une fois dans une instruction’switch'](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [' \ (') Attendus](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [' \) 'Attendu](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | ['/'Attendu](/scripting/javascript/misc/expected-minus) |  
| 1003 | [': 'Attendu](/scripting/javascript/misc/expected-colon) |  
| 1004 | ["; 'Attendu](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | [' @ 'Attendu](/scripting/javascript/misc/expected-at) |  
| 1029 | [' @End’attendu](/scripting/javascript/misc/expected-at-end) |  
| 1007 | [' \] 'Attendu](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | [' {'Attendu](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | ['} 'Attendu](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [' = 'Attendu](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | [Capture attendue](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Constante attendue](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Chiffre hexadécimal ATTENDU](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Identificateur attendu](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Identificateur attendu, chaîne ou nombre](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | ['While’attendu](/scripting/javascript/misc/expected-while) |  
| 1014 | [Caractère non valide](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Étiquette introuvable](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Étiquette redéfinie](/scripting/javascript/misc/label-redefined) |  
| 1018 | [instruction’retour’en dehors de la fonction](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Erreur de syntaxe](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | [Throw doit être suivi d’une expression sur la même ligne source](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Commentaire inachevé](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Constante de chaîne inachevée](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Erreurs d’hébergement de script  

Les messages d’erreur suivants concernent l’hôte de script, mais vous pouvez les voir parfois:  
  
| Erreur | HRESULT | Description |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Une erreur a été enregistrée et transmise entre le moteur de script et l’hôte.  L’hôte doit transférer le code d’erreur à l’appelant.  |  
| SCRIPT_E_REPORTED | 0x80020101 | Le moteur de script a signalé une exception non gérée à l’hôte via IActiveScriptSite:: OnScriptError.  L’hôte peut ignorer cette erreur.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Une erreur de script qui est propagée à l’appelant peut se trouver dans un thread différent.  L’hôte doit transférer le code d’erreur à l’appelant.  |  

## Erreurs d’exécution JavaScript

Des erreurs d’exécution JavaScript se produisent lorsque votre script essaie d’effectuer une action que le système ne peut pas exécuter.  Des erreurs d’exécution peuvent apparaître lors de l’évaluation d’expressions de variables ou lors de l’allocation de mémoire.

| Numéro d’erreur | Description |  
| --- | --- |  
| n°5 | [Accès refusé](/scripting/javascript/misc/access-is-denied) |  
| 438 | [L’objet ne prend pas en charge cette propriété ou méthode](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Mémoire insuffisante |  

### Erreurs Windows Runtime  

 Si vous utilisez les API Windows Runtime \ (WinRT \), il est possible que des erreurs JavaScript aient été converties à partir de HRESULTs Windows Runtime.  Les valeurs HRESULTs Windows Runtime dans la plage de plus de 0x80070000 sont converties en erreurs JavaScript en utilisant la valeur hexadécimale des bits basse et en convertissant celles-ci en décimal.  Par exemple, la valeur HRESULT 0x80070032 est convertie en valeur décimale 50 et l’erreur JavaScript est SCRIPT50.  La valeur HRESULT 0x80074005 est convertie en valeur décimale 16389 et l’erreur JavaScript est SCRIPT16389.

| Numéro d’erreur | Description |  
| --- | --- |  
| 5029 | [La longueur de tableau doit être un entier positif fini.](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [Une longueur de tableau doit être attribuée à un nombre positif fini.](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Objet matrice ou arguments ATTENDU](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Valeur booléenne attendue](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [Impossible d’affecter au résultat d’une fonction](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [Impossible d’affecter à’This'](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Référence circulaire dans l’argument de valeur non prise en charge](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Objet date attendu](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Objet Enumerator ATTENDU](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Exception levée et non interceptée](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Attendue') 'dans l’expression régulière](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [&#93; attendue dans l’expression régulière](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [La fonction n’a pas d’objet prototype valide](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Fonction attendue](/scripting/javascript/misc/function-expected) |  
| 5008 | [Affectation illégale](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Plage non valide dans le jeu de caractères](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Argument de remplacement non valide](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [Objet JavaScript ATTENDU](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Nombre attendu](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objet ATTENDU](/scripting/javascript/misc/object-expected) |  
| 5012 | [Membre de l’objet ATTENDU](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Objet Regular expression ATTENDU](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Chaîne attendue](/scripting/javascript/misc/string-expected) |  
| 5017 | [Erreur de syntaxe dans l’expression régulière](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [Le nombre de décimales est hors limites.](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [La précision n’est pas comprise dans la plage](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [L’URI à décoder n’est pas un codage valide.](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [L’URI à encoder contient un caractère non valide.](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Identificateur non défini](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Quantificateur inattendu](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [VBArray ATTENDU](/scripting/javascript/misc/vbarray-expected) |  

## Code de sécurité

Les `SEC7xxx` codes d’erreur de sécurité sont au format ( `SEC7113`par exemple,.  Ces erreurs reflètent les conditions de sécurité appliquées par Microsoft Edge, par exemple le contenu mixte et la protection contre le suivi.

| Code | Message | Description | Correction suggérée |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "La sécurité HTTP est compromise par [nom de la ressource]" | Une page SSL (Secure Hypertext Transfer Protocol) (HTTPs) comporte du contenu provenant d’une source non sécurisée.  | Assurez-vous que tout le contenu de la page, y compris les scripts, objets de feuille de style et images, proviennent de sources HTTPs.  |  
| SEC7112 | «Le script de [URL] a été bloqué en raison de l’incompatibilité de type MIME | L’en-tête de réponse HTTP pour le fichier JavaScript spécifié par l’URL est associé à un en-tête «X-Content-type-insniff» et ne possède pas de déclaration du type de contenu reconnu.  | Mettez à jour le serveur pour envoyer le type de contenu approprié pour le fichier JavaScript \ (par exemple, text/JavaScript, application/JavaScript ", par exemple \) dans l’en-tête de réponse HTTP.  Pour plus d’informations et pour obtenir la liste complète des types de contenu, voir [modifications de gestion MIME dans Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | «CSS a été ignoré en raison d’une incompatibilité de type MIME.» | Une feuille de style importée n’a pas été utilisée car le type MIME incorrect était dans l’en-tête HTTP.  | Assurez-vous que le fichier de feuille de style est fourni avec l’en-tête de réponse HTTP approprié, qui inclut un type de contenu de texte/CSS.  Pour plus d’informations, reportez-vous à la section [gestion du protocole MIME dans Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | «Un téléchargement sur cette page a été bloqué par une protection contre le suivi. [URL fournie ici] " | L’utilisateur a bloqué un script ou du contenu en utilisant une protection contre le suivi.  | Aucun-initié par l’utilisateur.  |  
| SEC7115 | ": les styles de lien peuvent être différents par couleur.  Certains styles n’ont pas été appliqués à: visité.» | Plusieurs attributs, tels que la police ou la taille, ont été modifiés en utilisant les styles visité et lien.  | Modifier uniquement l’attribut couleur.  |  
| SEC7116 | "Accès refusé.  Échec de la révocation de l’URL d’origine croisée: [URL].» | Un script ayant un site d’origine différent de l’objet BLOB essayait de révoquer une URL de BLOB.  En raison des stratégies d’origine BLOB, la tentative a échoué.  | Assurez-vous que toutes les URL d’objet BLOB sont révoquées en utilisant des scripts du même site d’origine que le document qui a créé l’URL de BLOB.  |  
| SEC7120 | «Origin [Domain] introuvable dans l’en-tête Access-Control-allow-Origin.» | En réponse à votre XMLHttpRequest, l’en-tête Access-Control-allow-Origin a été renvoyé avec une valeur qui ne contient pas ou qui correspond à la valeur d’origine de votre site.  | La ressource renvoie le type approprié de codes d’en-tête, mais n’autorise pas votre site.  Contactez le développeur chargé de la ressource et demandez-lui de mettre à jour son en-tête d’accès-Control-allow-Origin pour que votre site soit autorisé.  Pour plus d’informations sur les en-têtes de réponse, vous pouvez les désigner sur [cors pour XHR dans IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) .  |  
| SEC7121 | "Caractère générique dans Access-Control-allow-Origin interdit lorsque l’indicateur d’identification est défini sur true." | Le serveur renvoie «Access-Control-allow-Origin: *» dans les en-têtes, mais cela n’est pas autorisé lorsque `withCredentials` l’indicateur est défini sur **true** dans le XMLHttpRequest.  | Le gestionnaire côté serveur doit être modifié pour renvoyer un en-tête Access-Control-allow-Origin qui autorise spécifiquement votre point d’origine sur ce type de requête.  Si vous ne contrôlez pas le gestionnaire côté serveur, vous devrez parler au développeur.  |  
| SEC7122 | «L’indicateur d’informations d’identification a été défini sur true, mais Access-Control-allow-Credential n’était pas présent ou a été défini sur «true». | Un XMLHttpRequest a été créé à `withCredentials` l’aide de l’indicateur.  Un en-tête Access-Control-allow-Credential n’a pas été retourné ou a été renvoyé par une valeur autre que **true**.  | Il y a peut-être un problème avec vos informations d’identification ou la réponse du serveur.  Pour plus d’informations sur les demandes d’informations d’identification, voir la [spécification de niveau 2 de XMLHttpRequest](https://w3.org/TR/XMLHttpRequest2/) .  |  
| SEC7123 | «L’en-tête de requête [en-tête] n’était pas présent dans la liste Access-Control-allow-headers.» | Un type d’en-tête personnalisé a été inclus dans la demande, mais la liste d’en-têtes de contrôle d’accès de la réponse n’y a pas été incluse.  | Assurez-vous que le serveur autorise les en-têtes personnalisés et qu’il autorise spécifiquement celui qui est envoyé à la demande.  |  
| SEC7124 | «La méthode de requête [Method] n’était pas présente dans la liste Access-Control-allow-methods.» | Une méthode de requête telle que POST a été utilisée dans le XMLHttpRequest, mais la réponse a renvoyé un en-tête Access-Control-allow-méthodes qui ne l’a pas inclus.  | Assurez-vous que le serveur accepte ce type de méthode de requête et que `withCredentials` vous utilisez correctement si cette méthode a un accès restreint.  |  
| SEC7125 | «XMLHttpRequest for [URL] a entraîné l’échec de l’analyse d’en-têtes de réponse.» | Les en-têtes de réponse du serveur n’ont pas pu être analysés, ce qui a pour échec la requête.  | Utilisez l' [outil réseau](https://msdn.microsoft.com/library/dn255004.aspx) pour capturer et inspecter les en-têtes de réponse afin de vous assurer qu’ils répondent aux [spécifications de cors](https://w3.org/TR/cors/).  |  
| SEC7126 | «Les redirections ne sont pas autorisées pour les demandes de contrôle de version préliminaire de CORS.» | Une redirection a été détectée dans l’en-tête Origin et l’agent utilisateur ne suivra pas les redirections lors d’une prévolée.  | Utilisez l' [outil réseau](https://msdn.microsoft.com/library/dn255004.aspx) pour capturer et inspecter les en-têtes de demande et vérifier qu’il existe une seule origine directe.  |  
| SEC7127 | «La redirection a été bloquée pour une demande CORS.» | Le chemin d’accès à la ressource CORS contenait une redirection qui violait les règles de sécurité.  | Assurez-vous d’avoir le chemin d’accès direct à la ressource CORS dans votre XMLHttpRequest.  |  
| SEC7128 | «Les en-têtes de contrôle d’accès multiples-allow-Origin ne sont pas autorisés pour la réponse CORS.» | L’en-tête Response contenait plusieurs en-têtes de contrôle d’accès d’origine.  | Il s’agit d’une erreur côté serveur.  Le serveur doit retourner un seul en-tête Access-Control-allow-Origin.  Signalez cette erreur au développeur chargé de la ressource côté serveur.
| SEC7129 | «Les en-têtes de contrôle d’accès multiples-allow-Credentials ne sont pas autorisés pour la réponse CORS.» | L’en-tête de réponse contient plusieurs en-têtes de contrôle d’accès-autorisation.  | Il s’agit d’une erreur côté serveur.  Le serveur doit retourner un en-tête de contrôle d’accès unique.  Signalez cette erreur au développeur chargé de la ressource côté serveur.  |  
| SEC7130 | «Les scripts intersites potentiels détectés dans [URL].  Le contenu a été modifié par le filtre XSS.» | Le [filtre XSS](https://msdn.microsoft.com/library/dd565647.aspx) a détecté du contenu potentiellement malveillant dans la réponse de la ressource et a supprimé le contenu incriminé.  | En savoir plus sur le [filtre XSS](https://msdn.microsoft.com/library/dd565647.aspx).  |  
| SEC7131 | «La sécurité d’un IFRAME en bac à sable est susceptible d’être compromis en permettant l’accès au script et aux mêmes origines.» | Si le contenu d’un IFRAME en bac à sable provient d’une source non approuvée ou non sécurisée, il est possible qu’il se transforme en bac à sable lorsque le script et l’accès à l’origine sont tous deux autorisés.  | Il s’agit d’un message d’avertissement d’information qui ne doit pas affecter la fonctionnalité.  Nous vous recommandons de ne pas combiner ces autorisations, sauf si vous êtes sûr de ce qui sera exécuté sur le IFRAME.  |  
| SEC7132 | «Le certificat qui protège ce site Web utilise un chiffrement faible» | Le certificat de sécurité TLS utilisé par ce site Web utilise un chiffrement faible. | Mettez à jour le certificat TLS du serveur. |  

> [!NOTE]
> Sur les sites Web figurant dans la zone de sécurité approuvée d’un utilisateur, Microsoft Edge ne vérifie pas le type MIME d’une feuille de style.

## Code SVG  

DevTools ne prend actuellement pas en charge le débogage des graphiques vectoriels évolutifs (SVG \), mais certains messages de console sont fournis pour vous aider au débogage.

| Code | Message | Description | Correction suggérée |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | «Les données de chemin d’accès SVG ont un format incorrect et ne peuvent pas être analysées entièrement.» | La chaîne de [chemin d’accès](https://msdn.microsoft.com/library/ff972086.aspx) SVG n’est pas correctement mise en forme ou contient des commandes non reconnues.  | Vérifiez le format des commandes.  |  
| SVG5602 | La liste de points SVG a un format incorrect et ne peut pas être analysé entièrement. | La liste des points utilisés pour un élément, tel qu’une forme [Polyline](https://msdn.microsoft.com/library/ff972113.aspx), est mise en forme de manière incorrecte.  | Assurez-vous que les points sont terminés et correctement mis en forme pour le système de coordonnées utilisateurs.  |  

## Codes XML  

Les codes XML s’exécutent sous la forme XML5xxx, par exemple, XML5603.  

| Code | Message |  
|:--- |:--- |  
| XML5001 | «Application du traitement XSLT intégré». |  
| XML5601 | "MX_E_MX" |  
| XML5602 | «Fin inattendue de l’entrée». |  
| XML5603 | «Codage non reconnu». |  
| XML5604 | «Impossible de changer le codage». |  
| XML5605 | «Signature de codage d’entrée non reconnue». |  
| XML5606 | "WC_E_WC" |  
| XML5607 | "Espace blanc attendu." |  
| XML5608 | "Point-virgule attendu." |  
| XML5609 | «ATTENDU» > «». |  
| XML5610 | «Guillemet attendu». |  
| XML5611 | "Attendu" = "." |  
| XML5612 | «Le < caractère n’est pas autorisé dans les valeurs d’attributs». |  
| XML5613 | "Chiffre hexadécimal attendu." |  
| XML5614 | "Chiffre décimal attendu." |  
| XML5615 | "Attendu" ["." |  
| XML5616 | "Attendu" (".") |  
| XML5617 | "Caractère XML interdit" |  
| XML5618 | "Caractère de nom interdit". |  
| XML5619 | «Syntaxe du document incorrecte». |  
| XML5620 | «Syntaxe de la section CDATA incorrecte». |  
| XML5621 | "Syntaxe des commentaires incorrecte." |  
| XML5622 | «Syntaxe de la section conditionnelle incorrecte». |  
| XML5623 | «Syntaxe de déclaration ATTLIST incorrecte». |  
| XML5624 | «Syntaxe de déclaration DOCTYPE incorrecte». |  
| XML5625 | «Syntaxe de la déclaration d’élément incorrecte». |  
| XML5626 | «Syntaxe de déclaration d’entité incorrecte». |  
| XML5627 | «Syntaxe de la déclaration de NOTATION incorrecte». |  
| XML5628 | "NDATA" attendu " |  
| XML5629 | "PUBLIC" inattendue. " |  
| XML5630 | «SYSTÈME attendu».» |  
| XML5631 | "Nom non valide". |  
| XML5632 | «Un seul élément racine est autorisé». |  
| XML5633 | «Le nom de la balise de fin ne correspond pas au nom de la balise de début correspondant.» |  
| XML5634 | «Un attribut portant le même nom existe déjà sur cet élément.» |  
| XML5635 | «Une déclaration XML est uniquement autorisée au début du fichier». |  
| XML5636 | "XML de début" |  
| XML5637 | «Syntaxe de déclaration de texte incorrecte». |  
| XML5638 | «Syntaxe de déclaration XML incorrecte». |  
| XML5639 | «Syntaxe du nom de codage incorrecte». |  
| XML5640 | «Syntaxe d’identificateur public incorrecte». |  
| XML5641 | «Les références d’entité de paramètre ne sont pas autorisées dans les déclarations de balisage dans un sous-ensemble de DTD interne.» |  
| XML5642 | «Le texte de remplacement des références d’entité de paramètre utilisé entre les déclarations de balisage doit contenir une série de déclarations de balisage complètes.» |  
| XML5643 | «Une entité analysée ne doit pas contenir de référence directe ou indirecte à elle-même.» |  
| XML5644 | «Le contenu de l’entité spécifiée n’est pas correctement formé». |  
| XML5645 | «L’entité spécifiée n’a pas été déclarée.» |  
| XML5646 | «La référence d’entité ne peut pas contenir le nom d’une entité non analysée». |  
| XML5647 | «Les valeurs d’attribut ne doivent pas contenir de références directes ou indirectes à des entités externes». |  
| XML5648 | «Syntaxe d’instructions de traitement incorrecte». |  
| XML5649 | «Syntaxe d’identification système incorrecte». |  
| XML5650 | "Le point d’interrogation est attendu: |  
| XML5651 | «Le délimiteur CDATA-section-Close»]] >» ne doit pas être utilisé dans le contenu de l’élément.» |  
| XML5652 | «Certains blocs de données n’ont pas été lus». |  
| XML5653 | «Le DTD a été trouvé mais est interdit». |  
| XML5654 | «Attribut XML: Space trouvé avec une valeur non valide.  Les valeurs valides sont «Preserve» ou «default». |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Caractère de nom qualifié illégal" |  
| XML5657 | "Plusieurs deux-points": "ne doit pas se trouver dans un nom qualifié." |  
| XML5658 | "Deux-points": "ne doit pas se trouver dans un nom". |  
| XML5659 | "Préfixe déclaré" |  
| XML5660 | «Le préfixe spécifié n’a pas été déclaré.» |  
| XML5661 | Les déclarations d’espaces de noms non par défaut ne doivent pas avoir d’URI vides.» |  
| XML5662 | Le préfixe «xml» est réservé et doit avoir l’URI «<https://w3.org/XML/1998/namespace/>». |  
| XML5663 | Le préfixe «xmlns» est réservé à une utilisation par XML.» |  
| XML5664 | «L’URI d’espace de noms XML \ https://w3.org/XML/1998/namespace/\>\) (\ <doit être affecté uniquement au préfixe «xml».» |  
| XML5665 | «L’URI d’espace de noms xmlns \ https://w3.org/2000/xmlns/\>\) (\ <est réservé et ne doit pas être utilisé.» |  
| XML5666 | "SC_E_SC" |  
| XML5667 | «Profondeur maximale du nombre d’éléments imbriqués». |  
| XML5668 | "Dépassement du nombre maximal d’extensions d’entité." |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: writer: la chaîne spécifiée n’est pas Whitespace." |  
| XML5671 | «WR_E_NSPREFIXDECLARED: writer: le préfixe d’espace de noms est déjà déclaré avec un espace de noms différent.» |  
| XML5672 | «WR_E_NSPREFIXWITHEMPTYNSURI: writer: impossible d’utiliser le préfixe avec l’URI d’espace de noms vide.» |  
| XML5673 | «WR_E_DUPLICATEATTRIBUTE: writer: attribut dupliqué». |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: writer: ne peut pas redéfinir le préfixe xmlns." |  
| XML5675 | «WR_E_XMLPREFIXDECLARATION: writer: le préfixe xml doit avoir l' https://w3.org/XML/1998/namespace/\> URI \ <.» |  
| XML5676 | «WR_E_XMLURIDECLARATION: writer: URI d’espace de noms XML \ https://w3.org/XML/1998/namespace/\>\) (\ <doit être attribué uniquement au préfixe «xml».» |  
| XML5677 | «WR_E_XMLNSURIDECLARATION: writer: URI d’espace de noms xmlns \ https://w3.org/2000/xmlns/\>\) (\ <est réservé et ne doit pas être utilisé.» |  
| XML5678 | «WR_E_NAMESPACEUNDECLARED: writer: l’espace de noms n’est pas déclaré.» |  
| XML5679 | "WR_E_INVALIDXMLSPACE: writer: valeur non valide de XML: attribut Space \ (les valeurs autorisées sont «default» et «Preserve» \).» |  
| XML5680 | «WR_E_INVALIDACTION: writer: l’exécution de l’action demandée engendrerait un document XML non valide.» |  
| XML5681 | «WR_E_INVALIDSURROGATEPAIR: writer: l’entrée comporte une paire de substitution non valide ou incomplète.» |  
| XML5682 | "Caractère inattendu dans l’entité caractère.  Chiffre décimal attendu. |  
| XML5683 | "Caractère inattendu dans l’entité caractère.  Chiffre hexadécimal attendu.» |  
| XML5684 | «La valeur Unicode de l’entité de caractères spécifiée n’est pas valide.» |  
| XML5685 | "Codage non valide". |  
| XML5686 | "Erreur XML non spécifiée" |  
