---
description: Référence pour le domaine de la page. Les actions et événements liés à la page inspectée appartiennent au domaine de la page.
title: Page Domain-DevTools Protocol version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 688cc1fcfce0b81c5eed0c858a4a60b4754c49a4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565467"
---
# Page
Les actions et événements liés à la page inspectée appartiennent au domaine de la page.

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable), [naviguer](#navigate), [getFrameTree](#getframetree) |
| [**Événements**](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |
| [**Types**](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |
## Méthodes

### activer
Active les notifications de domaine de page.

</p>

---

### désactiver 
Désactive les notifications de domaine de la page.

</p>

---

### naviguer
Accède à la page active à l’URL donnée.

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
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL permettant d’accéder à la page.</td>
        </tr>
        <tr>
            <td>frameId <br/> <i>facultatif</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID de cadre pour naviguer. Si ce n’est pas le cas, accède à la page du haut.</td>
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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID de cadre qui sera parcouru.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getFrameTree
Renvoie une structure d’arborescence de trames.

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
            <td>frameTree</td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td>Présenter une structure d’arborescence d’images</td>
        </tr>
    </tbody>
</table>
</p>

---

## Événements

### frameAttached
Déclenché lorsque le frame a été attaché à son parent.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID de l’image jointe.</td>
        </tr>
        <tr>
            <td>parentFrameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificateur d’image parent.</td>
        </tr>
        <tr>
            <td>graphique <br/> <i>facultatif</i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td>Trace de pile JavaScript du moment où l’image a été attachée, ne définir que le frame lancé à partir d’un script.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameDetached
Déclenché lorsque le frame a été détaché du parent.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ID de l’image qui a été dissociée.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameNavigated
Déclenché une fois que la navigation de l’image est terminée.

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
            <td>séquence</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Objet Frame.</td>
        </tr>
    </tbody>
</table>
</p>

---

### loadEventFired
Correspond à l’événement Window. OnLoad.

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
            <td>telle</td>
            <td><code class="flyout">number</code></td>
            <td>Nombre de millisecondes depuis l’époque.</td>
        </tr>
    </tbody>
</table>
</p>

---

### domContentEventFired
Correspond à l’événement document. onDOMContentLoaded.

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
            <td>telle</td>
            <td><code class="flyout">number</code></td>
            <td>Nombre de millisecondes depuis l’époque.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Types

### <a name="frameid"></a> FrameId `string`

Identificateur de cadre unique.

</p>

---

### <a name="frame"></a> Trame `object`

Des informations sur le cadre de la page.

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
            <td>id</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Cadre identificateur unique.</td>
        </tr>
        <tr>
            <td>Parent <br/> <i>facultatif</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Identificateur unique du cadre parent.</td>
        </tr>
        <tr>
            <td>name <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nom de l’image, tel que spécifié dans la balise.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL du document Frame.</td>
        </tr>
        <tr>
            <td>securityOrigin</td>
            <td><code class="flyout">string</code></td>
            <td>Origine de la sécurité du document Frame.</td>
        </tr>
        <tr>
            <td>MIME</td>
            <td><code class="flyout">string</code></td>
            <td>Le mimeType du document de cadre déterminé par le navigateur.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> FrameTree `object`

Des informations sur la hiérarchie de trames.

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
            <td>séquence</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Informations d’image pour cet élément d’arborescence.</td>
        </tr>
        <tr>
            <td>childFrames <br/> <i>facultatif</i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td>Images enfants.</td>
        </tr>
    </tbody>
</table>
</p>

---
