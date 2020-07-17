---
description: Référence pour le domaine Runtime. Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.
title: Domain Runtime-DevTools Protocol version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 710b3b3e0383f1f6feb7947e0468730d2e0b0e66
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882861"
---
# Domain Runtime-DevTools Protocol version 0,2 (EdgeHTML)  

Le domaine d’exécution expose le runtime JavaScript au moyen de l’évaluation à distance et des objets miroirs. Les résultats d’évaluation sont retournés sous la forme d’un objet miroir exposant le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour une référence d’objet supplémentaire. Les objets d’origine sont conservés en mémoire, sauf s’ils sont explicitement émis.

| | |
|-|-|
| [**Méthodes**](#methods) | [activer](#enable), [Désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries) |
| [**Événements**](#events) | [executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled) |
| [**Types**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |
## Méthodes

### activer
Active la création de rapports sur les <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> événements et. Lorsque la création de rapports est activée <code>executionContextCreated</code> , l’événement est envoyé immédiatement pour chaque contexte d’exécution existant.

</p>

---

### désactiver 
Désactive la création de rapports sur <code>executionContextCreated</code> les <code>executionContextDestroyed</code> <code>executionContextsCleared</code> événements et.

</p>

---

### evaluat
Évalue l’expression sur l’objet global.

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
            <td>termes</td>
            <td><code class="flyout">string</code></td>
            <td>Expression à évaluer.</td>
        </tr>
        <tr>
            <td>includeCommandLineAPI <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Détermine si une API de ligne de commande doit être disponible au cours de l’évaluation.</td>
        </tr>
        <tr>
            <td>objectGroup <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution. Remplace l' <code>setPauseOnException</code> État.</td>
        </tr>
        <tr>
            <td>contextId <br/> <i>facultatif</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Spécifie le contexte d’exécution permettant d’effectuer une évaluation. Si le paramètre est omis, l’évaluation sera exécutée dans le contexte de la page inspectée.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</td>
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
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Résultat de l’évaluation.</td>
        </tr>
    </tbody>
</table>
</p>

---

### callFunctionOn
Fonction appelle avec la déclaration fournie sur l’objet donné. Le groupe d’objets du résultat est hérité de l’objet cible.

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
            <td>functionDeclaration</td>
            <td><code class="flyout">string</code></td>
            <td>Déclaration de la fonction à appeler.</td>
        </tr>
        <tr>
            <td>Algorithm <br/> <i>facultatif</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificateur de l’objet sur lequel appeler la fonction. ObjectId ou executionContextId doit être spécifié.  objectId doit être issu de la fonction Runtime. Evaluate ().</td>
        </tr>
        <tr>
            <td>arguments <br/> <i>facultatif</i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td>Appeler des arguments. Tous les arguments d’appel doivent appartenir au même univers JavaScript que l’objet cible.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>En mode silencieux, les exceptions levées lors de l’évaluation ne sont pas communiquées et n’interrompent pas l’exécution. Remplace l' <code>setPauseOnException</code> État.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si l’exécution doit avoir <code>await</code> pour résultat la valeur résultante et l’État retour une fois la promesse attendue résolue.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>facultatif</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Spécifie le contexte d’exécution sur lequel l’objet global sera utilisé pour appeler la fonction. La valeur executionContextId ou objectId doit être spécifiée.</td>
        </tr>
        <tr>
            <td>objectGroup <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nom du groupe de symboles qui peut être utilisé pour libérer plusieurs objets. Si objectGroup n’est pas spécifié et que objectId est, objectGroup sera hérité de Object.</td>
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
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Résultat de l’appel.</td>
        </tr>
    </tbody>
</table>
</p>

---

### awaitPromise
Ajoutez le gestionnaire à la promesse avec ID d’objet promise.

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
            <td>promiseObjectId</td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificateur de la promesse.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si le résultat est censé être un objet JSON qui doit être envoyé par valeur.</td>
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
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Résultat de la promesse.  Va contenir la valeur rejetée si la promesse a été refusée.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getProperties
Renvoie les propriétés d’un objet donné. Le groupe d’objets du résultat est hérité de l’objet cible.

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
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificateur de l’objet dont vous souhaitez renvoyer les propriétés. objectId doit être issu de la fonction Debugger. evaluateOnCallFrame ().</td>
        </tr>
        <tr>
            <td>ownProperties <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la valeur est true, retourne les propriétés qui ne sont liées qu’à l’élément proprement dit, et non à sa chaîne de prototype.</td>
        </tr>
        <tr>
            <td>accessorPropertiesOnly <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Pratiqué. </b></span>Si true, retourne les propriétés d’accesseur (avec l’accesseur get/set) uniquement; les propriétés internes ne sont pas renvoyées.</td>
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
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td>Propriétés d’objet.</td>
        </tr>
    </tbody>
</table>
</p>

---

### globalLexicalScopeNames
Renvoie toutes les variables de type, de constante et de classe à partir de l’étendue globale de la console.

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
            <td>leurs</td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseObject
Libère l’objet distant avec l’ID donné.

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
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificateur de l’objet à libérer. </td>
        </tr>
    </tbody>
</table>
</p>

---

### releaseObjectGroup
Libère tous les objets distants appartenant à un groupe donné.

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
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Nom du groupe d’objets symboliques. </td>
        </tr>
    </tbody>
</table>
</p>

---

### discardConsoleEntries
Supprime les exceptions collectées et les appels d’API de console.

</p>

---

## Événements

### executionContextCreated
Émis lors de la création du contexte d’exécution.

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
            <td>contexte</td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td>Contexte d’exécution nouvellement créé.</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextDestroyed
Émis lorsque le contexte d’exécution est détruit.

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
            <td>executionContextId</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>ID du contexte détruit</td>
        </tr>
    </tbody>
</table>
</p>

---

### executionContextsCleared
Émis lorsque tous les executionContexts étaient effacés dans le navigateur

</p>

---

### exceptionThrown
Émis quand une exception a été levée et non gérée.

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
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Horodatage de l’exception.</td>
        </tr>
        <tr>
            <td>exceptionDetails</td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### consoleAPICalled


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
            <td>type</td>
            <td><code class="flyout">string</code> <br/> <i>Valeurs autorisées: Journal, informations, avertissement, erreur, déboguer, assertion, table, trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</i></td>
            <td>Type de l’appel. Il s’agit de journaux, d’informations, d’avertissement, d’erreur, de débogage, d’assertion, de table, de suivi, de Rép, de DirXML, d’effacement, de countReset, d’timeEnd, d’exception, d’horodatage, de groupe, groupCollapsed, groupEnd.</td>
        </tr>
        <tr>
            <td>args</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td>Appeler des arguments.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Identificateur du contexte dans lequel l’appel de console a été effectué.</td>
        </tr>
        <tr>
            <td>telle <br/> <i>facultatif</i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Horodatage de l’appel.</td>
        </tr>
        <tr>
            <td>Trace <br/> <i>facultatif</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Trace de pile capturée, le cas échéant</td>
        </tr>
    </tbody>
</table>
</p>

---

## Types

### <a name="scriptid"></a> ScriptId `string`

Identificateur de script unique.

</p>

---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Identifiant unique de l’objet.

</p>

---

### <a name="unserializablevalue"></a> UnserializableValue `string`

Valeur primitive qui ne peut pas être JSON-stringified.

##### Valeurs autorisées
Infinity, NaN,-Infinity,-0
</p>

---

### <a name="remoteobject"></a> RemoteObject `object`

Objet Mirror référençant l’objet JavaScript d’origine.

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
            <td><code class="flyout">string</code> <br/> <i>Valeurs autorisées: objet, fonction, non défini, chaîne, nombre, booléen, symbole</i></td>
            <td>Type d’objet.</td>
        </tr>
        <tr>
            <td>sous-type <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code> <br/> <i>Valeurs autorisées: null, erreur, promesse, nœud</i></td>
            <td>Indicateur de sous-type d’objet. Spécifié pour les <code>object</code> valeurs de type uniquement.</td>
        </tr>
        <tr>
            <td>NomClasse <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Nom de classe d’objet (constructeur). Spécifié pour les <code>object</code> valeurs de type uniquement.</td>
        </tr>
        <tr>
            <td>value <br/> <i>facultatif</i></td>
            <td><code class="flyout">any</code></td>
            <td>Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON (le cas échéant).</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>facultatif</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Valeur primitive qui ne peut pas être JSON-stringified <code>value</code>mais obtient cette propriété.</td>
        </tr>
        <tr>
            <td>description <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Représentation de chaîne de l’objet.</td>
        </tr>
        <tr>
            <td>Algorithm <br/> <i>facultatif</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Identificateur d’objet unique (pour les valeurs non Primitives).</td>
        </tr>
        <tr>
            <td>msDebuggerPropertyId <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Pratiqué. </b></span>Microsoft: ID de propriété de débogueur associé pour cet objet.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> PropertyDescriptor `object`

Descripteur de propriété objet.

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
            <td>Nom de la propriété ou description du symbole.</td>
        </tr>
        <tr>
            <td>value <br/> <i>facultatif</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Valeur associée à la propriété.</td>
        </tr>
        <tr>
            <td>accès <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si la valeur associée à la propriété est susceptible d’être modifiée (descripteurs de données uniquement).</td>
        </tr>
        <tr>
            <td>obtenir <br/> <i>facultatif</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Fonction qui sert de Getter pour la propriété, ou <code>undefined</code> s’il n’y a pas d’accesseur get (descripteurs d’accesseur uniquement).</td>
        </tr>
        <tr>
            <td>set <br/> <i>facultatif</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Fonction utilisée comme une méthode setter de la propriété, ou <code>undefined</code> s’il n’y a pas de méthodes setter (descripteurs d’accesseur uniquement).</td>
        </tr>
        <tr>
            <td>configurables</td>
            <td><code class="flyout">boolean</code></td>
            <td>True si le type de ce descripteur de propriété est modifiable et si la propriété est susceptible d’être supprimée de l’objet correspondant.</td>
        </tr>
        <tr>
            <td>tournant</td>
            <td><code class="flyout">boolean</code></td>
            <td>True si cette propriété s’affiche lors de l’énumération des propriétés de l’objet correspondant.</td>
        </tr>
        <tr>
            <td>wasThrown <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si le résultat a été levé lors de l’évaluation.</td>
        </tr>
        <tr>
            <td>isOwn <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True si la propriété est possédée pour l’objet.</td>
        </tr>
        <tr>
            <td>msReturnValue <br/> <i>facultatif</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Pratiqué. </b></span>Microsoft: true si la propriété est une valeur de retour.</td>
        </tr>
        <tr>
            <td>symbol <br/> <i>facultatif</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Objet symbol de propriété, si la propriété est de `symbol` type. </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> CallArgument `object`

Représente l’argument appel de fonction. ID d’objet distant <code>objectId</code> , primitive <code>value</code> , valeur primitive unserializable ou aucun de (pour undefined).

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
            <td>value <br/> <i>facultatif</i></td>
            <td><code class="flyout">any</code></td>
            <td>Valeur primitive ou objet JavaScript sérialisable.</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>facultatif</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Valeur primitive qui ne peut pas être JSON-stringified.</td>
        </tr>
        <tr>
            <td>Algorithm <br/> <i>facultatif</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Handle d’objet distant.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> ExecutionContextId `integer`

ID du contexte d’exécution.

</p>

---

### <a name="executioncontextdescription"></a> ExecutionContextDescription `object`

Description d’un monde isolé.

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
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>ID unique du contexte d’exécution. Il peut être utilisé pour spécifier l’évaluation du script de contexte d’exécution qui doit être effectuée.</td>
        </tr>
        <tr>
            <td>prêts</td>
            <td><code class="flyout">string</code></td>
            <td>Origine du contexte d’exécution.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nom lisible par le humain décrivant le contexte donné.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> ExceptionDetails `object`

Informations détaillées sur l’exception (ou l’erreur) levée lors de la compilation ou de l’exécution d’un script.

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
            <td>exceptionId</td>
            <td><code class="flyout">integer</code></td>
            <td>ID de l’exception.</td>
        </tr>
        <tr>
            <td>texte</td>
            <td><code class="flyout">string</code></td>
            <td>Texte de l’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de ligne de l’emplacement de l’exception (0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de colonne de l’emplacement de l’exception (0).</td>
        </tr>
        <tr>
            <td>scriptId <br/> <i>facultatif</i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>ID de script de l’emplacement de l’exception.</td>
        </tr>
        <tr>
            <td>url <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL de l’emplacement de l’exception à utiliser lorsque le script n’a pas été communiqué.</td>
        </tr>
        <tr>
            <td>Trace <br/> <i>facultatif</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Trace de pile JavaScript, le cas échéant.</td>
        </tr>
        <tr>
            <td>sauf <br/> <i>facultatif</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Objet exception, s’il est disponible.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>facultatif</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Identificateur du contexte où une exception s’est produite.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> Horodateur `integer`

Nombre de millisecondes depuis l’époque.

</p>

---

### <a name="callframe"></a> CallFrame `object`

Entrée de pile pour les erreurs d’exécution et les affirmations.

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
            <td>Admises</td>
            <td><code class="flyout">string</code></td>
            <td>Nom de la fonction JavaScript.</td>
        </tr>
        <tr>
            <td>scriptId</td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>ID de script JavaScript. ScriptId est vide si le débogueur n’est pas activé.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Nom ou URL du script JavaScript.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de ligne de script JavaScript (0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Numéro de colonne de script JavaScript (0).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> Trace `object`

Trames d’appel pour les affirmations ou messages d’erreur.

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
            <td>description <br/> <i>facultatif</i></td>
            <td><code class="flyout">string</code></td>
            <td>Étiquette de chaîne de cette trace de pile. Pour les traces Async, il s’agit du nom de la fonction qui a déclenché l’appel asynchrone.</td>
        </tr>
        <tr>
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Nom de la fonction JavaScript.</td>
        </tr>
        <tr>
            <td>dernier <br/> <i>facultatif</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Trace de pile JavaScript asynchrone qui précède cette pile, s’il est disponible.</td>
        </tr>
    </tbody>
</table>
</p>

---
