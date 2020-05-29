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
# CSS
Ce domaine présente les opérations en lecture/écriture CSS. Tous les objets CSS (feuilles de style, règles et styles) sont associés à des `id` opérations ultérieures sur l’objet associé. Chaque type d’objet possède une `id` structure spécifique et celles-ci ne sont pas interchangeables entre les objets de différents genres. Les objets CSS peuvent être chargés en utilisant les `get*ForNode()` appels (qui acceptent un ID de nœud DOM). Un client peut également suivre les feuilles de style par le biais des `styleSheetAdded` / `styleSheetRemoved` événements, puis charger le contenu de la feuille de style requis au moyen des `getStyleSheet[Text]()` méthodes.

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode) |
| [**Événements**](#events) | [styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved) |
| [**Types**](#types) | [StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader) |
| [**Dépendances**](#dependencies) | [DOM](dom.md) |
## Méthodes

### activer
Active l’agent CSS pour la page donnée. Les clients ne doivent pas supposer que l’agent CSS a été activé tant que le résultat de la commande n’a pas été reçu.

</p>

---

### désactiver 
Désactive l’agent CSS pour la page donnée.

</p>

---

### getInlineStylesForNode
Retourne les styles définis inline (explicitement dans l’attribut «style» et implicitement à l’aide d’attributs DOM) pour un nœud DOM identifié par `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ID</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Renvoie</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>facultatif</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Style intraligne du nœud DOM spécifié.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>facultatif</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Style d’élément défini par l’attribut (par exemple, «Width = 20 Height = 100%»).</td>
        </tr>
    </tbody>
</table>
</p>

---

### getMatchedStylesForNode
Renvoie les styles requis pour un nœud DOM identifié par `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ID</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Renvoie</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>facultatif</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Style intraligne du nœud DOM spécifié.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>facultatif</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Style d’élément défini par l’attribut (par exemple, «Width = 20 Height = 100%»).</td>
        </tr>
        <tr>
            <td>matchedCSSRules <br /> <i>facultatif</i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Règles CSS correspondant à ce nœud, de toutes les feuilles de style en vigueur.</td>
        </tr>
        <tr>
            <td>pseudoElements <br /> <i>facultatif</i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td>Correspondances de Pseudo-styles pour ce nœud.</td>
        </tr>
        <tr>
            <td>héritées <br /> <i>facultatif</i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td>Chaîne de styles hérités (du nœud immédiat parent jusqu’à la racine de l’arborescence DOM).</td>
        </tr>
        <tr>
            <td>cssKeyframesRules <br /> <i>facultatif</i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td>Liste des animations par images clés CSS correspondant à ce nœud.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getPlatformFontsForNode
Demande des informations sur les polices de plateforme que nous avons utilisées pour afficher les TextNodes enfants dans le nœud donné.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ID</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Renvoie</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>polices</td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td>Statistiques d’utilisation pour chaque police de plateforme utilisée.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getComputedStyleForNode
Renvoie le style calculé pour un nœud DOM identifié par `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ID</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Renvoie</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>computedStyle</td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td>Style calculé pour le nœud DOM spécifié.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Événements

### styleSheetAdded
Déclenché lors de l’ajout d’une feuille de style de document active.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>header</td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td>A ajouté des méta-informations.</td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetChanged
Déclenché dès que le résultat de l’opération du client est modifié.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetRemoved
Déclenché lors de la suppression d’une feuille de style de document active.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificateur de la feuille de style supprimée.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Types

### <a name="stylesheetid"></a> StyleSheetId `string`



</p>

---

### <a name="pseudoelementmatches"></a> PseudoElementMatches `object`

Collection de règles CSS pour un Pseudo-style unique.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>pseudoType</td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td>Type de pseudo-élément.</td>
        </tr>
        <tr>
            <td>matches</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Correspondances de règles CSS applicables au Pseudo-style.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> InheritedStyleEntry `object`

Collection de règles CSS héritée du nœud ancêtre.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>facultatif</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Le style intraligne du nœud ancêtre, le cas échéant, dans la chaîne d’héritage de style.</td>
        </tr>
        <tr>
            <td>matchedCSSRules</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Correspondances de règles CSS correspondant au nœud ancêtre dans la chaîne d’héritage de style.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> RuleMatch `object`

Correspondent aux données pour une règle CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>elle</td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td>Règle CSS dans la correspondance.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> Valeur `object`

Les données d’un sélecteur simple (délimitées par des virgules dans une liste de sélecteur).

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>texte</td>
            <td><code class="flyout">string</code></td>
            <td>Texte de la valeur.</td>
        </tr>
        <tr>
            <td>portée <br /> <i>facultatif</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Plage de valeurs de la ressource sous-jacente (le cas échéant).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> SelectorList `object`

Afficher les données des listes.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>sélecteurs</td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td>Sélectionneurs de la liste.</td>
        </tr>
        <tr>
            <td>texte</td>
            <td><code class="flyout">string</code></td>
            <td>Texte du sélecteur de règles</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> CSSRule `object`

Représentation de la règle CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>facultatif</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identifiant de la feuille de style CSS (absent pour la feuille de style de l’agent utilisateur et règles de feuille de style spécifiées par l’utilisateur) dont provient cette règle.</td>
        </tr>
        <tr>
            <td>selectorList <br /> <i>facultatif</i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td>Données du sélecteur de règles.</td>
        </tr>
        <tr>
            <td>prêts <br /> <i>facultatif</i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Origine de la feuille de style parente.</td>
        </tr>
        <tr>
            <td>style</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Déclaration de style associée.</td>
        </tr>
        <tr>
            <td>médias <br /> <i>facultatif</i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td>Tableau de liste de médias (pour les règles impliquant des requêtes multimédias). Le tableau recense les requêtes multimédias à partir de l’élément le plus interne, en partant du haut.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> SourceRange `object`

Plage de textes au sein d’une ressource. Tous les nombres sont en fonction du zéro.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Ligne de début de la plage.</td>
        </tr>
        <tr>
            <td>ColonneDébut</td>
            <td><code class="flyout">integer</code></td>
            <td>Colonne de début de plage (inclusive).</td>
        </tr>
        <tr>
            <td>lignefin</td>
            <td><code class="flyout">integer</code></td>
            <td>Ligne de fin de la plage</td>
        </tr>
        <tr>
            <td>ColonneFin</td>
            <td><code class="flyout">integer</code></td>
            <td>Colonne de plage de fin (exclusif).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> ShorthandEntry `object`



<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom abrégé.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valeur raccourci.</td>
        </tr>
        <tr>
            <td>essentielles <br /> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propriété comporte une annotation «! important» (implique qu’il n’en soit pas `false` ).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> CSSStyle `object`

Représentation de style CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>facultatif</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identifiant de la feuille de style CSS (absent pour la feuille de style de l’agent utilisateur et règles de feuille de style spécifiées par l’utilisateur) dont provient cette règle.</td>
        </tr>
        <tr>
            <td>cssProperties</td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td>Propriétés CSS du style.</td>
        </tr>
        <tr>
            <td>shorthandEntries</td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td>Valeurs calculées pour tous les raccourcis identifiés dans le style.</td>
        </tr>
        <tr>
            <td>cssText <br /> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Texte de la déclaration de style (le cas échéant).</td>
        </tr>
        <tr>
            <td>portée <br /> <i>facultatif</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Plage de déclaration de style dans la feuille de style englobante (le cas échéant).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> CSSProperty `object`

Données de déclaration de propriété CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de la propriété.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valeur de la propriété.</td>
        </tr>
        <tr>
            <td>essentielles <br /> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propriété comporte une annotation «! important» (implique qu’il n’en soit pas `false` ).</td>
        </tr>
        <tr>
            <td>prennent <br /> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>L’utilisation de la propriété implicite (implique `false` si absent).</td>
        </tr>
        <tr>
            <td>texte <br /> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Texte de la propriété complète, tel qu’indiqué dans le style.</td>
        </tr>
        <tr>
            <td>parsedOk <br /> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propriété est comprise par le navigateur (c’est-à-dire si elle est `true` absente).</td>
        </tr>
        <tr>
            <td>désactivé <br /> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propriété est désactivée par l’utilisateur (disponible uniquement pour les propriétés sources).</td>
        </tr>
        <tr>
            <td>portée <br /> <i>facultatif</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Plage de propriétés entière de la déclaration de style englobante (le cas échéant).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> CSSMedia `object`

Descripteur de règle multimédia CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>texte</td>
            <td><code class="flyout">string</code></td>
            <td>Texte de la requête multimédia.</td>
        </tr>
        <tr>
            <td>origine</td>
            <td><code class="flyout">string</code> <br /> <i>Valeurs autorisées: mediaRule, importRule, linkedSheet, inlineSheet</i></td>
            <td>Source de la requête multimédia: «mediaRule» s’il est spécifié par une règle de @media, «importRule» s’il est spécifié par une règle de @import, «linkedSheet» en cas de spécification par un attribut «Media» dans la balise de liaison d’une feuille de style de feuille de style</td>
        </tr>
        <tr>
            <td>sourceURL <br /> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL du document contenant la description de la requête multimédia.</td>
        </tr>
        <tr>
            <td>portée <br /> <i>facultatif</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>La règle associée (@media ou @import) dans la feuille de style englobante (le cas échéant).</td>
        </tr>
        <tr>
            <td>styleSheetId <br /> <i>facultatif</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificateur de la feuille de style contenant cet objet (le cas échéant).</td>
        </tr>
        <tr>
            <td>le médiane <br /> <i>facultatif</i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td>Tableau de requêtes multimédias.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> MediaQuery `object`

Descripteur de requête multimédia.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>contenu</td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td>Tableau d’expressions de requête multimédias.</td>
        </tr>
        <tr>
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la condition de requête multimédia est satisfaite.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> MediaQueryExpression `object`

Descriptor expression de requête multimédia.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value</td>
            <td><code class="flyout">number</code></td>
            <td>Valeur de l’expression de requête multimédia.</td>
        </tr>
        <tr>
            <td>centres</td>
            <td><code class="flyout">string</code></td>
            <td>Unités d’expression de requête multimédia.</td>
        </tr>
        <tr>
            <td>fonctionnalité</td>
            <td><code class="flyout">string</code></td>
            <td>Fonctionnalité d’expression de requête multimédia.</td>
        </tr>
        <tr>
            <td>valueRange <br /> <i>facultatif</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Plage associée du texte de la valeur figurant dans la feuille de style englobante (le cas échéant).</td>
        </tr>
        <tr>
            <td>computedLength <br /> <i>facultatif</i></td>
            <td><code class="flyout">number</code></td>
            <td>Durée calculée de l’expression de requête multimédia (le cas échéant).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> PlatformFontUsage `object`

Informations sur le nombre de glyphes qui ont été affichés avec la police donnée.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>familyName</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de la famille de polices signalé par la plate-forme.</td>
        </tr>
        <tr>
            <td>isCustomFont</td>
            <td><code class="flyout">boolean</code></td>
            <td>Indique si la police a été téléchargée ou résolue localement.</td>
        </tr>
        <tr>
            <td>glyphCount</td>
            <td><code class="flyout">number</code></td>
            <td>Nombre de glyphes qui ont été affichés avec cette police.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> CSSKeyframesRule `object`

Représentation de la règle CSS frames

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>animationName</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Nom de l’animation.</td>
        </tr>
        <tr>
            <td>images clés</td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td>Liste d’images clés.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> CSSKeyframeRule `object`

Représentation de la règle d’image clé CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>facultatif</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identifiant de la feuille de style CSS (absent pour la feuille de style de l’agent utilisateur et règles de feuille de style spécifiées par l’utilisateur) dont provient cette règle.</td>
        </tr>
        <tr>
            <td>prêts</td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Origine de la feuille de style parente.</td>
        </tr>
        <tr>
            <td>keytext</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Texte de clé associé.</td>
        </tr>
        <tr>
            <td>style</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Déclaration de style associée.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> CSSComputedStyleProperty `object`



<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de la propriété de style calculée.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valeur de propriété de style calculée.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> CSSStyleSheetHeader `object`

Données de feuille de style CSS.

<table>
    <thead>
        <tr>
            <th>Propriétés</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificateur de la feuille de style.</td>
        </tr>
        <tr>
            <td>sourceURL</td>
            <td><code class="flyout">string</code></td>
            <td>URL de la ressource StyleSheet.</td>
        </tr>
        <tr>
            <td>désactivé</td>
            <td><code class="flyout">boolean</code></td>
            <td>Indique si la feuille de style est désactivée.</td>
        </tr>
        <tr>
            <td>isInline</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si cette feuille de STYLE est créée pour la balise de STYLE par parser. Cet indicateur n’est pas défini pour les balises de STYLE document. crit.</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">number</code></td>
            <td>Décalage de ligne de la feuille de style dans la ressource (en fonction de zéro).</td>
        </tr>
        <tr>
            <td>ColonneDébut</td>
            <td><code class="flyout">number</code></td>
            <td>Décalage de colonne de la feuille de style dans la ressource (en fonction de zéro).</td>
        </tr>
        <tr>
            <td>nombre</td>
            <td><code class="flyout">number</code></td>
            <td>Taille du contenu (en caractères).</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dépendances

[DOM](dom.md)
