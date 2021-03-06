---
description: Référence du protocole DevTools version 0.1 (EdgeHTML) pour le domaine d’runtime.  Le domaine runtime expose le runtime JavaScript au moyen d’objets miroir et d’évaluation à distance.  Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet.  Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.
title: Domaine d’runtime - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397691"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a>Domaine d’runtime - DevTools Protocol Version 0.1 (EdgeHTML)  

Le domaine d’runtime expose le runtime JavaScript au moyen d’objets d’évaluation et de miroir distants.  Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet.  Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.  

| Classification | Membres |  
|:--- |:--- |  
| [Méthodes](#methods) | [activer](#enable), [désactiver](#disable), [évaluer](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties) |  
| [Événements](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |  
| [Types](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Méthodes  

### <a name="enable"></a>activer  

Active la notification de `executionContextsCleared` l’événement.  

&nbsp;  

---  

### <a name="disable"></a>désactiver   

Désactive le signalement de `executionContextsCleared` l’événement.  

&nbsp;  

---  

### <a name="evaluate"></a>évaluer  

Évalue l’expression sur l’objet global.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| expression | `string` | Expression à évaluer. |  
| silent \(optional\) | `boolean` | En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.  Remplace `setPauseOnException` l’état. |  
| contextId \(facultatif\) | [ExecutionContextId](#executioncontextid) | Spécifie dans quel contexte d’exécution effectuer l’évaluation.  Si le paramètre est omis, l’évaluation sera effectuée dans le contexte de la page inspectée. |  
| returnByValue \(optional\) | `boolean` | Si le résultat est censé être un objet JSON qui doit être envoyé par valeur. |  
| awaitPromise \(optional\) | `boolean` | Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Résultat de l’évaluation. |  

---  

### <a name="callfunctionon"></a>callFunctionOn  

Appelle la fonction avec déclaration donnée sur l’objet donné.  Le groupe d’objets du résultat est hérité de l’objet cible.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| functionDeclaration | `string` | Déclaration de la fonction à appeler. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificateur de l’objet sur qui appeler la fonction.  `objectId` `executionContextId` L’une ou l’autre doit être spécifiée.  objectId doit être issu de la fonction Runtime.evaluate(). |  
| arguments \(facultatif\) | [CallArgument[]](#callargument) | Arguments d’appel.  Tous les arguments d’appel doivent appartenir au même monde JavaScript que l’objet cible. |  
| silent \(optional\) | `boolean` | En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.  Remplace `setPauseOnException` l’état. |  
| returnByValue \(optional\) | `boolean` | Si le résultat est censé être un objet JSON qui doit être envoyé par valeur. |  
| awaitPromise \(optional\) | `boolean` | Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Résultat de l’appel. |  

---  

### <a name="getproperties"></a>getProperties  

Renvoie les propriétés d’un objet donné.  Le groupe d’objets du résultat est hérité de l’objet cible.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Identificateur de l’objet pour qui renvoyer les propriétés.  `objectId` doit être issu de la `Debugger.evaluateOnCallFrame()` fonction. |  
| ownProperties \(optional\) | `boolean` | Si `true` , renvoie les propriétés appartenant uniquement à l’élément lui-même, et non à sa chaîne prototype. |  
| accessorPropertiesOnly \(optional\) | `boolean` | **Expérimental**.  Si `true` , renvoie les propriétés d’accesseur \(avec getter/setter\) uniquement ; les propriétés internes ne sont pas renvoyées non plus. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [PropertyDescriptor[]](#propertydescriptor) | Propriétés de l’objet. |  

---  

## <a name="events"></a>Événements  

### <a name="executioncontextscleared"></a>executionContextsCleared  

Émis lorsque tous les executionContexts ont été effacés dans le navigateur.  

&nbsp;  

---  

### <a name="exceptionthrown"></a>exceptionThrown  

Émise lorsque l’exception a été levée et nonhandée.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| timestamp | [Horodateur](#timestamp) | Timestamp de l’exception. |  
| exceptionDetails | [ExceptionDetails](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a>Types  

### <a name="scriptid-string"></a>Chaîne ScriptId  

<a name="scriptid"></a>  

Identificateur de script unique.  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a>Chaîne RemoteObjectId  

<a name="remoteobjectid"></a>  

Identificateur d’objet unique.  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a>Chaîne UnserializableValue  

<a name="unserializablevalue"></a>  

Valeur de primitive qui ne peut pas être stringified JSON.  

##### <a name="allowed-values"></a>Valeurs autorisées  

`Infinity`, `NaN`, `-Infinity`, `-0`  

---  

### <a name="remoteobject-object"></a>Objet RemoteObject  

<a name="remoteobject"></a>  

Objet Miroir référencant un objet JavaScript d’origine.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| type | `string` | Type d’objet.  Valeurs autorisées  `object` : , , , , `function` `undefined` `string` `number` `boolean` et `symbol` |  
| subtype \(optional\) | `string` | Conseil de sous-type d’objet.  Spécifié pour les `object` valeurs de type uniquement.  Valeurs autorisées  `null` : `error` , et `promise` |  
| className \(optional\) | `string` | Nom de la classe d’objet \(constructor\).  Spécifié pour les `object` valeurs de type uniquement. |  
| value \(optional\) | `any` | Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON \(si elle a été demandée\). |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | La valeur primitive qui ne peut pas être stringified JSON n’a `value` pas , mais obtient cette propriété. |  
| description \(facultatif\) | `string` | Représentation sous la chaîne de l’objet. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificateur d’objet unique \(pour les valeurs non primitives\). |  
| msDebuggerPropertyId \(optional\) | `string` | **Expérimental**.  Microsoft : ID de propriété du débogger associé pour cet objet. |  

---  

### <a name="propertydescriptor-object"></a>Objet PropertyDescriptor  

<a name="propertydescriptor"></a>  

Descripteur de propriété d’objet.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| name | `string` | Nom de la propriété ou description du symbole. |  
| value \(optional\) | [RemoteObject](#remoteobject) | Valeur associée à la propriété. |  
| writable \(optional\) | `boolean` | `True` si la valeur associée à la propriété peut être modifiée \(descripteurs de données uniquement\). |  
| get \(optional\) | [RemoteObject](#remoteobject) | Fonction qui sert de getter pour la propriété, ou s’il n’existe pas de `undefined` getter \(descripteurs d’accesseurs uniquement\). |  
| set \(optional\) | [RemoteObject](#remoteobject) | Fonction qui sert de setter pour la propriété, ou s’il n’y a pas de `undefined` setter \(descripteurs d’accesseurs uniquement\). |  
| configurable | `boolean` | `True` si le type de ce descripteur de propriété peut être modifié et si la propriété peut être supprimée de l’objet correspondant. |  
| éumerable | `boolean` | `True` si cette propriété s’affiche lors de l’éumération des propriétés sur l’objet correspondant. |  
| wasThrown \(optional\) | `boolean` | `True` si le résultat a été lancé au cours de l’évaluation. |  
| isOwn \(optional\) | `boolean` | `True` si la propriété appartient à l’objet. |  
| msReturnValue \(optional\) | `boolean` | **Expérimental**.  Microsoft :  `True` si la propriété est une valeur de retour. |  
| symbol \(optional\) | [RemoteObject](#remoteobject) | Objet symbole de propriété, si la propriété est du `symbol` type. |  

---  

### <a name="callargument-object"></a>Objet CallArgument  

<a name="callargument"></a>  

Représente l’argument appel de fonction.  L’ID d’objet distant, la valeur de primitive non personnalisable ou l’un des deux `value` \(pour undefined\) doivent être spécifiés.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| value \(optional\) | `any` | Valeur primitive ou objet javascript sérialisable. |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Valeur de primitive qui ne peut pas être stringified JSON. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Handle d’objet distant. |  

---  

### <a name="executioncontextid-integer"></a>ExecutionContextId, integer  

<a name="executioncontextid"></a>  

ID d’un contexte d’exécution.  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a>Objet ExceptionDetails  

<a name="exceptiondetails"></a>  

Informations détaillées sur l’exception \(ou l’erreur\) qui a été lancée lors de la compilation ou de l’exécution du script.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| exceptionId | `integer` | ID d’exception. |  
| texte | `string` | Texte d’exception, qui doit être utilisé avec l’objet exception lorsqu’il est disponible. |  
| lineNumber | `integer` | Numéro de ligne de l’emplacement de l’exception \(0-based\). |  
| columnNumber | `integer` | Numéro de colonne de l’emplacement de l’exception \(0-based\). |  
| scriptId \(facultatif\) | [ScriptId](#scriptid) | ID de script de l’emplacement d’exception. |  
| url \(optional\) | `string` | URL de l’emplacement de l’exception, à utiliser lorsque le script n’a pas été signalé. |  
| stackTrace \(optional\) | [StackTrace](#stacktrace) | Trace de pile JavaScript si disponible. |  
| exception \(facultatif\) | [RemoteObject](#remoteobject) | Objet Exception, s’il est disponible. |  
| executionContextId \(optional\) | [ExecutionContextId](#executioncontextid) | Identificateur du contexte dans lequel l’exception s’est produite. |  

---  

### <a name="timestamp-integer"></a>Timestamp integer  

<a name="timestamp"></a>  

Nombre de millisecondes depuis l’époque.  

&nbsp;  

---  

### <a name="callframe-object"></a>Objet CallFrame  

<a name="callframe"></a>  

Entrée de pile pour les erreurs d’runtime et les assertions.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| functionName | `string` | Nom de la fonction JavaScript. |  
| scriptId | [ScriptId](#scriptid) | ID de script JavaScript. |  
| url | `string` | Nom ou URL du script JavaScript. |  
| lineNumber | `integer` | Numéro de ligne de script JavaScript \(0-based\). |  
| columnNumber | `integer` | Numéro de colonne de script JavaScript \(basé sur 0\). |  

---  

### <a name="stacktrace-object"></a>Objet StackTrace  

<a name="stacktrace"></a>  

Appelez des cadres pour les assertions ou les messages d’erreur.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| description \(facultatif\) | `string` | Étiquette de chaîne de cette trace de pile.  Pour les suivis async, il peut s’agit d’un nom de la fonction qui a initié l’appel async. |  
| callFrames | [CallFrame[]](#callframe) | Nom de la fonction JavaScript. |  
| parent \(facultatif\) | [StackTrace](#stacktrace) | Trace de pile JavaScript asynchrone précédant cette pile, si disponible. |  

---  
