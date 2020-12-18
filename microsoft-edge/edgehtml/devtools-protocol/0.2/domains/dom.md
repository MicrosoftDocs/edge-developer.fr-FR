---
description: Référence pour le domaine DOM. Ce domaine expose les opérations en lecture/écriture DOM. Chaque nœud DOM est représenté avec son objet Mirror contenant un objet `id` . Cela `id` peut être utilisé pour obtenir des informations supplémentaires sur le nœud, le résoudre dans le wrapper d’objet JavaScript, etc. Il est important que le client reçoit les événements DOM uniquement pour les nœuds connus du client. Le principal effectue le suivi des nœuds envoyés au client et n’envoie jamais le même nœud deux fois. Il incombe au client de recueillir des informations sur les nœuds envoyés au client.<p>Notez que les `iframe` éléments de propriétaire renvoient les éléments de document correspondants comme leurs nœuds enfants.</p>
title: DOM Domain-DevTools Protocol version 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233238"
---
# DOM

Ce domaine expose les opérations en lecture/écriture DOM. Chaque nœud DOM est représenté avec son objet Mirror contenant un objet `id` . Cela `id` peut être utilisé pour obtenir des informations supplémentaires sur le nœud, le résoudre dans le wrapper d’objet JavaScript, etc. Il est important que le client reçoit les événements DOM uniquement pour les nœuds connus du client. Le principal effectue le suivi des nœuds envoyés au client et n’envoie jamais le même nœud deux fois. Il incombe au client de recueillir des informations sur les nœuds envoyés au client.<p>Notez que les `iframe` éléments de propriétaire renvoient les éléments de document correspondants comme leurs nœuds enfants.</p>

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable), [GetDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [GetAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode) |
| [**Événements**](#events) | [setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated) |
| [**Types**](#types) | [RVBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [nœud](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype) |
| [**Dépendances**](#dependencies) | [Runtime](runtime.md) |
## Méthodes

### activer
Active l’agent DOM pour la page donnée.

</p>

---

### désactiver 
Désactive l’agent DOM pour la page donnée. La désactivation du DOM rendra non valide tout nodeIds précédemment valide.

</p>

---

### getDocument
Renvoie le nœud DOM racine (et éventuellement la sous-arborescence) pour l’appelant. `getDocument`Les appels seront non valides pour les nodeIdss précédemment valides.

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
            <td>expertise</td>
            <td><code class="flyout">integer</code></td>
            <td>La profondeur maximale de récupération des enfants, par défaut de 2. Utilisez-1 pour l’ensemble de la sous-arborescence.</td>
        </tr>
        <tr>
            <td>traverser</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si les iframes doivent être parcourus lors du retour de la sous-arborescence (false par défaut).</td>
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
            <td>associé</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Nœud obtenu.</td>
        </tr>
    </tbody>
</table>
</p>

---

### highlightNode
Nœud DOM higlights avec ID donné ou wrapper d’objet. l’argument nodeId, backendNodeId ou objectId doit être spécifié.

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
            <td>ID <br/> <i>facultatif</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificateur du nœud à mettre en surbrillance.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>facultatif</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificateur du nœud principal à mettre en surbrillance.</td>
        </tr>
        <tr>
            <td>Algorithm <br/> <i>facultatif</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>ID d’objet JavaScript du nœud à mettre en surbrillance.</td>
        </tr>
        <tr>
            <td>higlightConfig</td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td>Descripteur de l’apparence de surlignage.</td>
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
            <td>associé</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Nœud obtenu.</td>
        </tr>
    </tbody>
</table>
</p>

---

### hideHighlight
Masque la surbrillance du nœud DOM actuel.

</p>

---

### requestChildNodes
Demande que les enfants du nœud avec ID donné soient renvoyés à l’appelant gué sous la forme d' `setChildNodes` événements. `setChildNodes` sera déclenché pour tous les nœuds qui n’ont pas encore renvoyé leurs enfants, en partant du nœud requis vers la profondeur spécifiée.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud à partir duquel obtenir des enfants.</td>
        </tr>
        <tr>
            <td>expertise</td>
            <td><code class="flyout">integer</code></td>
            <td>La profondeur maximale de récupération des enfants, par défaut de 1. Utilisez-1 pour l’ensemble de la sous-arborescence.</td>
        </tr>
        <tr>
            <td>traverser</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si les iframes doivent être parcourus lors du retour de la sous-arborescence (false par défaut).</td>
        </tr>
    </tbody>
</table>
</p>

---

### getAttributes
Renvoie les attributs du nœud spécifié.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud duquel récupérer attibutes.</td>
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
            <td>Propriétés</td>
            <td><code class="flyout">string[]</code></td>
            <td>Tableau entrelacé de noms et de valeurs d’attributs de nœud.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getOuterHTML
Renvoie le balisage HTML du nœud.

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
            <td>ID <br/> <i>facultatif</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificateur du nœud.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>facultatif</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Identificateur du nœud principal.</td>
        </tr>
        <tr>
            <td>Algorithm <br/> <i>facultatif</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>ID d’objet JavaScript du wrapper de nœud.</td>
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
            <td>outerHTML</td>
            <td><code class="flyout">string</code></td>
            <td>Balisage HTML externe.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pushNodesByBackendIdsToFrontend
Recherche les ID de nœud et résolve tous les parents pour les ID de nœud principal spécifiés.

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
            <td>backendNodeIds</td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td>ID de nœud principal des nœuds à résoudre</td>
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
            <td>nodeIds</td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>ID de nœud des nœuds résolus</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelector
S’exécute `querySelector` sur un nœud donné.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud sur lequel interroger.</td>
        </tr>
        <tr>
            <td>sélecteur</td>
            <td><code class="flyout">string</code></td>
            <td>Chaîne de sélecteur.</td>
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
            <td>ID</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Résultat du sélecteur de requête.</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelectorAll
S’exécute `querySelectorAll` sur un nœud donné.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud sur lequel interroger.</td>
        </tr>
        <tr>
            <td>sélecteur</td>
            <td><code class="flyout">string</code></td>
            <td>Chaîne de sélecteur.</td>
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
            <td>nodeIds</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Résultats du sélecteur de requête.</td>
        </tr>
    </tbody>
</table>
</p>

---

### requestNode
Demande que le nœud avec l’ID d’objet distant fourni soit envoyé à l’appelant. Tous les nœuds qui constituent le chemin d’accès du nœud à la racine sont également envoyés au client dans le cadre d’une série de `setChildNodes` notifications. renvoie 0 si le document contenant le nœud demandé n’a pas encore été demandé par le client.

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
            <td>Algorithm</td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>ID d’objet JavaScript à convertir en nœud.</td>
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
            <td>ID</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID de nœud pour l’objet donné.</td>
        </tr>
    </tbody>
</table>
</p>

---

### resolveNode
Résout l’objet de nœud JavaScript pour une NodeId ou BackendNodeId donnée.

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
            <td>ID <br/> <i>facultatif</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud à résoudre.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>facultatif</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>ID du nœud principal du nœud à résoudre.</td>
        </tr>
        <tr>
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</td>
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
            <td>object</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Wrapper d’objet JavaScript pour le nœud donné.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setInspectedNode
<span><b>Pratiqué. </b></span>Autorise la console à faire référence au nœud inspecté précédent avec l’ID donné via $0-$ 4.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID de nœud DOM à rendre accessible par le biais de $0-$ 4 dans l’API de ligne de commande.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Événements

### setChildNodes
Déclenché lorsque le serveur principal souhaite fournir un client avec une structure DOM introuvable. Ce problème se produit sur la plupart des appels demandant nodeIds

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
            <td>Parent</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Nœud parent à poplate avec des enfants.</td>
        </tr>
        <tr>
            <td>ceux</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Tableau de nœuds enfants.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeModified
Déclenché lorsque `Element` l’attribut a été modifié.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud qui a changé.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de l’attribut.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valeur de l’attribut.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeRemoved
Déclenché lorsque `Element` l’attribut est supprimé.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud qui a changé.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de l’attribut.</td>
        </tr>
    </tbody>
</table>
</p>

---

### characterDataModified
`DOMCharacterDataModified`Événement miroirs.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud qui a changé.</td>
        </tr>
        <tr>
            <td>charcterData</td>
            <td><code class="flyout">string</code></td>
            <td>Nouvelle valeur de texte.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeInserted
`DOMNodeInserted`Événement miroirs.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud qui a changé.</td>
        </tr>
        <tr>
            <td>previousNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du frère précédent du nœud inséré.</td>
        </tr>
        <tr>
            <td>nœud</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Données de nœud insérées.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeRemoved
`DOMNodeRemoved`Événement miroirs.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud qui a changé.</td>
        </tr>
        <tr>
            <td>ID</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ID du nœud qui a été supprimé.</td>
        </tr>
    </tbody>
</table>
</p>

---

### documentUpdated
Déclenché lors de la `Document` mise à jour. Les ID de nœud ne sont plus valides.

</p>

---

## Types

### <a name="rgba"></a> RVBA `object`

Structure contenant une couleur RVBA.

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
            <td>v</td>
            <td><code class="flyout">integer</code></td>
            <td>Composant rouge dans la plage [0-255].</td>
        </tr>
        <tr>
            <td>grand</td>
            <td><code class="flyout">integer</code></td>
            <td>Composant vert dans la plage [0-255].</td>
        </tr>
        <tr>
            <td>p</td>
            <td><code class="flyout">integer</code></td>
            <td>Composant bleu dans la plage [0-255].</td>
        </tr>
        <tr>
            <td>a <br/> <i>facultatif</i></td>
            <td><code class="flyout">number</code></td>
            <td>Composant alpha dans la plage [0-1]. La valeur par défaut est 1.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> HighlightConfig `object`

Données de configuration pour la mise en surbrillance des éléments de page.

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
            <td>contentColor <br/> <i>facultatif</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>La zone de contenu surligne la couleur de remplissage. La valeur par défaut est transparent.</td>
        </tr>
        <tr>
            <td>paddingColor <br/> <i>facultatif</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Couleur de remplissage de la mise en surbrillance. La valeur par défaut est transparent.</td>
        </tr>
        <tr>
            <td>Bordure <br/> <i>facultatif</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Couleur de remplissage de la bordure surlignée. La valeur par défaut est transparent.</td>
        </tr>
        <tr>
            <td>marginColor <br/> <i>facultatif</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Couleur de remplissage de l’accentuation des marges La valeur par défaut est transparent.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> ID `integer`

Identificateur de nœud DOM unique

</p>

---

### <a name="node"></a> Nœud `object`

Objet Mirror qui représente les nœuds DOM réels.

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
            <td>ID</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificateur de nœud utilisé pour référencer ce nœud. Le système principal déclenche les événements DOM pour les nœuds ayant un ID de nœud dont le nom est connu par le client.</td>
        </tr>
        <tr>
            <td>Parent <br/> <i>facultatif</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificateur de nœud du nœud parent, le cas échéant.</td>
        </tr>
        <tr>
            <td>backendNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Identificateur du nœud principal du nœud. Les nœuds de référence BackendNodeIds qui peuvent être connus du client, mais qui ne renvoient pas d’événements DOM sur ce nœud.</td>
        </tr>
        <tr>
            <td>nodeType</td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`nodeType.</td>
        </tr>
        <tr>
            <td>nodeName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`nodeName.</td>
        </tr>
        <tr>
            <td>Local</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`localName du</td>
        </tr>
        <tr>
            <td>nodeValue</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`nodeValue du</td>
        </tr>
        <tr>
            <td>childNodeCount <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Nombre enfant de `Container` nœuds.</td>
        </tr>
        <tr>
            <td>enfants <br/> <i>facultatif</i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Nœud enfant de ce nœud lors de la demande avec des enfants.</td>
        </tr>
        <tr>
            <td>Propriétés <br/> <i>facultatif</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Attributs des `Element` nœuds sous la forme d’un tableau à plat' [nom1, valeur1, nom2, valeur2]</td>
        </tr>
        <tr>
            <td>documentURL <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL du document `Document` pointant vers le nœud.</td>
        </tr>
        <tr>
            <td>baseURL <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL du document que `Document` les nœuds utilisent pour la fin des URL.</td>
        </tr>
        <tr>
            <td>publicId <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` PublicId du nœud.</td>
        </tr>
        <tr>
            <td>systemId <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` SystemId du nœud.</td>
        </tr>
        <tr>
            <td>internalSubset <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` InternalSubset du nœud.</td>
        </tr>
        <tr>
            <td>xmlVersion <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` Version XML du nœud dans le cas de documents XML.</td>
        </tr>
        <tr>
            <td>name <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Nom du nœud.</td>
        </tr>
        <tr>
            <td>value <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Valeur du nœud.</td>
        </tr>
        <tr>
            <td>frameId <br/> <i>facultatif</i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td>ID de frame pour les éléments de propriétaire de frame.</td>
        </tr>
        <tr>
            <td>contentDocument <br/> <i>facultatif</i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Document de contenu pour les éléments de propriétaire de frame.</td>
        </tr>
        <tr>
            <td>isSVG <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si le nœud est SVG.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> BackendNodeId `integer`

Identificateur de nœud DOM unique utilisé pour référencer un nœud qui n’a pas pu être envoyé au premier plan.

</p>

---

### <a name="pseudotype"></a> PseudoType `string`

Type de pseudo-élément.

##### Valeurs autorisées
première ligne, première lettre avant, après, sélection
</p>

---

## Dépendances

[Runtime](runtime.md)
