---
description: Référence de la version 0,2 (EdgeHTML) du protocole DevTools pour le domaine du débogueur. Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.
title: Debugger Domain-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24571b3a32acf085dd9ccbd641b1e5b06b3b9504
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232862"
---
# Debugger Domain-DevTools Protocol version 0,2 (EdgeHTML)  

Le domaine du débogueur expose les fonctionnalités de débogage JavaScript. Elle permet de définir et de supprimer des points d’arrêt, de parcourir l’exécution, d’explorer les traces de pile, etc.

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [décalage](#stepover)automatique [, stepInto](#stepinto), [stepOut](#stepout), [suspendre](#pause), [reprendre](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions,](#setpauseonexceptions) [evaluateOnCallFrame](#evaluateoncallframe)et [setVariableValue](#setvariablevalue), setBlackboxPatterns [, msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) [](#setblackboxpatterns) |
| [**Événements**](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), en [Pause](#paused), [reprise](#resumed) |
| [**Types**](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [scope](#scope) |
| [**Dépendances**](#dependencies) | [Runtime](runtime.md) |
## Méthodes

### activer
Autorise le débogueur pour la page donnée. Les clients ne doivent pas supposer que le débogage a été activé tant que le résultat de cette commande n’a pas été reçu.

</p>

---

### désactiver 
Désactive le débogueur pour une page donnée.

</p>

---

### getPossibleBreakpoints
Renvoie les emplacements possibles pour le point d’arrêt. scriptId les emplacements de début et de fin doivent être identiques.

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
            <td>start</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Début de la plage pour rechercher des emplacements de point d’arrêt possibles dans.</td>
        </tr>
        <tr>
            <td>terminer</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Fin de plage pour rechercher des emplacements de point d’arrêt possibles (à l’exception de). En l’absence de spécification, la fin des scripts est utilisée en tant que fin de plage.</td>
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
            <td>régions</td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td>Liste des emplacements de points d’arrêt possibles.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointsActive
Active/désactive tous les points d’arrêt de la page.

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
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Nouvelle valeur pour l’état actif de points d’arrêt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointByUrl
Définit le point d’arrêt JavaScript à l’emplacement indiqué par URL ou expression Regex. Dès que cette commande est lancée, tous les scripts analysés existants disposent de points d’arrêt résolus et renvoyés dans <code>locations</code> propriété. La recherche de script correspondante entraînera davantage d' <code>breakpointResolved</code> événements consécutifs. Ce point d’arrêt logique survivrea les recharges de la page.

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
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de ligne sur lequel définir le point d’arrêt.</td>
        </tr>
        <tr>
            <td>url <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL des ressources sur lesquelles définir le point d’arrêt.</td>
        </tr>
        <tr>
            <td>urlRegex <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Modèle Regex pour les URL des ressources sur lesquelles définir des points d’arrêt. La valeur <code>url</code> or <code>urlRegex</code> doit être spécifiée.</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Décalage dans la ligne où définir le point d’arrêt.</td>
        </tr>
        <tr>
            <td>autant <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Expression à utiliser comme condition de point d’arrêt. Lorsque ce paramètre est spécifié, le débogueur s’arrêtera sur le point d’arrêt uniquement si cette expression a pour résultat la valeur vrai.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>ID du point d’arrêt créé pour référence.</td>
        </tr>
        <tr>
            <td>régions</td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td>Liste des emplacements résolus par le point d’arrêt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpoint
Définit un point d’arrêt JavaScript à un emplacement donné.

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
            <td>ventilation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Emplacement dans lequel définir le point d’arrêt.</td>
        </tr>
        <tr>
            <td>autant <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Expression à utiliser comme condition de point d’arrêt. Lorsque ce paramètre est spécifié, le débogueur s’arrêtera sur le point d’arrêt uniquement si cette expression a pour résultat la valeur vrai.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>ID du point d’arrêt créé pour référence.</td>
        </tr>
        <tr>
            <td>actualLocation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Emplacement dans lequel ce point d’arrêt a été résolu.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeBreakpoint
Supprime le point d’arrêt JavaScript.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### 3D
Étapes sur l’instruction.

</p>

---

### stepInto
Étapes dans l’appel de fonction.

</p>

---

### stepOut
Étapes de l’appel de fonction.

</p>

---

### pause
S’arrête sur l’instruction JavaScript suivante.

</p>

---

### resume
Réactive l’exécution JavaScript.

</p>

---

### getScriptSource
Renvoie la source du script avec l’ID donné.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>ID du script pour lequel obtenir la source.</td>
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
            <td>scriptSource</td>
            <td><code class="flyout">string</code></td>
            <td>Source de script.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setPauseOnExceptions
Définit une pause sur l’État exceptions. Peut être défini pour s’arrêter sur toutes les exceptions, ou aucune exception. Le point d’interruption initial est <code>none</code> .

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
            <td>traité</td>
            <td><code class="flyout">string</code> <br/> <i>Valeurs autorisées: aucun, non intercepté, tous</i></td>
            <td>Placez le pointeur sur le mode exceptions.</td>
        </tr>
    </tbody>
</table>
</p>

---

### evaluateOnCallFrame
Évalue l’expression sur un cadre d’appel donné.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identifiant de l’identification de l’appel.</td>
        </tr>
        <tr>
            <td>termes</td>
            <td><code class="flyout">string</code></td>
            <td>Expression à évaluer.</td>
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
            <td>provoqué</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Wrapper d’objet pour le résultat d’évaluation.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setVariableValue
Change la valeur de la variable dans un callframe. Les étendues basées sur les objets ne sont pas prises en charge et doivent être mutées manuellement.

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
            <td>scopeNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>un nombre d’étendues égal à zéro tel qu’il apparaît dans la chaîne d’étendue. Seuls les types d’étendue’local', de fermeture et de capture sont autorisés. Les autres étendues peuvent être manipulées manuellement.</td>
        </tr>
        <tr>
            <td>NomVariable</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de la variable.</td>
        </tr>
        <tr>
            <td>NouvelleValeur</td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td>Valeur de la nouvelle variable.</td>
        </tr>
        <tr>
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>ID de callframe qui contient la variable.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBlackboxPatterns
<span><b>Pratiqué. </b></span>Remplacer les modèles de Blackbox Force le serveur principal à ignorer l’étape/la suspension dans les scripts avec une URL qui correspond à l’un des modèles. Le débogueur tente de quitter le script Blackbox en exécutant plusieurs fois «étape», ce qui a pour fin en cas d’échec.

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
            <td>masques</td>
            <td><code class="flyout">string[]</code></td>
            <td>Tableau d’regexps qui seront utilisés pour vérifier l’URL du script pour l’État Blackbox.</td>
        </tr>
    </tbody>
</table>
</p>

---

### msSetDebuggerPropertyValue
<span><b>Pratiqué. </b></span>Microsoft: définit la propriété Debugger spécifiée sur la valeur spécifiée.

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
            <td>debuggerPropertyId</td>
            <td><code class="flyout">string</code></td>
            <td>Microsoft: ID de propriété (par exemple, msDebuggerPropertyId) à définir.</td>
        </tr>
        <tr>
            <td>NouvelleValeur</td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## Événements

### scriptParsed
Déclenché lorsque le script est analysé. Cet événement est également déclenché pour tous les scripts connus et non perçus lors de l’activation du débogueur.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Identificateur du script analysé.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL ou nom du script analysé (le cas échéant).</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Décalage de ligne du script dans la ressource avec l’URL donnée (pour les balises de script).</td>
        </tr>
        <tr>
            <td>ColonneDébut</td>
            <td><code class="flyout">integer</code></td>
            <td>Décalage de colonne du script dans la ressource avec l’URL donnée.</td>
        </tr>
        <tr>
            <td>lignefin</td>
            <td><code class="flyout">integer</code></td>
            <td>Dernière ligne du script.</td>
        </tr>
        <tr>
            <td>ColonneFin</td>
            <td><code class="flyout">integer</code></td>
            <td>Longueur de la dernière ligne du script.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td>Spécifie le contexte de création de script.</td>
        </tr>
        <tr>
            <td>sourceMapURL <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL du mappage source associé au script (le cas échéant).</td>
        </tr>
        <tr>
            <td>nombre <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Pratiqué. </b></span>Cette longueur de script.</td>
        </tr>
        <tr>
            <td>msParentId <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Pratiqué. </b></span>Il s’agit de l’ID de document parent.</td>
        </tr>
        <tr>
            <td>msMimeType <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Pratiqué. </b></span>Il s’agit du type MIME.</td>
        </tr>
        <tr>
            <td>msIsDynamicCode <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Pratiqué. </b></span>Cela indique s’il s’agit d’un code dynamique.</td>
        </tr>
        <tr>
            <td>msLongDocumentId <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Pratiqué. </b></span>Il s’agit de l’ID de document long.</td>
        </tr>
    </tbody>
</table>
</p>

---

### breakpointResolved
Déclenché lorsque le point d’arrêt est résolu en un script et un emplacement réels.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Identificateur unique de point d’arrêt.</td>
        </tr>
        <tr>
            <td>ventilation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Emplacement du point d’arrêt réel.</td>
        </tr>
        <tr>
            <td>msLength <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Pratiqué. </b></span>Microsoft: longueur du code (par exemple, nombre de caractères) à l’emplacement du point d’arrêt.</td>
        </tr>
    </tbody>
</table>
</p>

---

### en pause
Déclenché lorsque les débogueurs s’interrompent pour un point d’arrêt ou une exception.

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
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Pile d’appels sur laquelle le débogueur a été arrêté.</td>
        </tr>
        <tr>
            <td>tient</td>
            <td><code class="flyout">string</code> <br/> <i>Valeurs autorisées: point d’arrêt, étape, exception, other, EventListener</i></td>
            <td>Raison du pause.</td>
        </tr>
        <tr>
            <td>data <br/> <i>facultatif</i></td>
            <td><code class="flyout">object</code></td>
            <td>Objet contenant des propriétés auxiliaires spécifiques de rupture.</td>
        </tr>
        <tr>
            <td>hitBreakpoints <br/> <i>facultatif</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>ID d’arrêt du positionnement</td>
        </tr>
        <tr>
            <td>asyncStackTrace <br/> <i>facultatif</i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td>Trace de pile asynchrone JavaScript.</td>
        </tr>
    </tbody>
</table>
</p>

---

### reprend
Déclenché lorsque le débogueur reprend l’exécution.

</p>

---

## Types

### <a name="breakpointid"></a> BreakpointId `string`

Identificateur de point d’arrêt.

</p>

---

### <a name="callframeid"></a> CallFrameId `string`

Identificateur d’image d’appel.

</p>

---

### <a name="location"></a> Location `object`

Emplacement dans le code source.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>ID de script tel qu’indiqué dans le <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de ligne dans le script (0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de colonne dans le script (0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: longueur de code (par exemple, nombre de caractères) à cette image d’appel.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> BreakLocation `object`

Emplacement d’arrêt dans le code source.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>ID de script tel qu’indiqué dans le <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de ligne dans le script (0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>facultatif</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de colonne dans le script (0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Microsoft: longueur de code (par exemple, nombre de caractères) à cette image d’appel.</td>
        </tr>
        <tr>
            <td>type <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Valeurs autorisées: debuggerStatement, Call, retour.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> CallFrame `object`

Image d’un appel JavaScript. Tableau de trames d’appel qui forment la pile d’appels.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Identificateur d’image d’appel. Cet identificateur est valide uniquement lorsque le débogueur est en pause.</td>
        </tr>
        <tr>
            <td>Admises</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de la fonction JavaScript appelée sur cette image d’appel.</td>
        </tr>
        <tr>
            <td>functionLocation <br/> <i>facultatif</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b>Pratiqué. </b></span>Emplacement dans le code source.</td>
        </tr>
        <tr>
            <td>ventilation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Emplacement dans le code source.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Nom ou URL du script JavaScript.</td>
        </tr>
        <tr>
            <td>scopeChain</td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td>Chaîne d’étendue pour cette image d’appel.</td>
        </tr>
        <tr>
            <td>elle</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> objet pour cette image d’appel.</td>
        </tr>
        <tr>
            <td>returnValue <br/> <i>facultatif</i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Valeur renvoyée, si la fonction est à la valeur de retour.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> Étendue `object`

Description de l’étendue.

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
            <td>type</td>
            <td><code class="flyout">string</code> <br/> <i>Valeurs autorisées: global, local, avec, clôture, catch, bloc, script, Eval, module, retour</i></td>
            <td>Type d’étendue.</td>
        </tr>
        <tr>
            <td>object</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Objet représentant la portée. Pour <code>global</code> les <code>with</code> étendues, il s’agit de l’objet réel; pour les autres étendues, il s’agit d’un objet temporaire artificiel qui énumère les variables d’étendue en tant que propriétés.</td>
        </tr>
        <tr>
            <td>name <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td>startLocation <br/> <i>facultatif</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Emplacement dans le code source où l’étendue commence</td>
        </tr>
        <tr>
            <td>endLocation <br/> <i>facultatif</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Emplacement dans le code source où l’étendue se termine</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dépendances

[Runtime](runtime.md)
