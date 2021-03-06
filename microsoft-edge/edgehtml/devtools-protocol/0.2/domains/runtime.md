---
description: Référence du protocole DevTools version 0.2 (EdgeHTML) pour le domaine d’runtime. Le domaine runtime expose le runtime JavaScript au moyen d’objets miroir et d’évaluation à distance. Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet. Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.
title: Domaine d’runtime - DevTools Protocol Version 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: afc79a17c5002f60806872a9add57f518ff6cb45
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398139"
---
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a>Domaine d’runtime - DevTools Protocol Version 0.2 (EdgeHTML)  

Le domaine d’runtime expose le runtime JavaScript au moyen d’objets d’évaluation et de miroir distants. Les résultats de l’évaluation sont renvoyés en tant qu’objet miroir qui exposent le type d’objet, la représentation de chaîne et l’identificateur unique qui peuvent être utilisés pour d’autres références d’objet. Les objets d’origine sont conservés en mémoire, sauf s’ils sont libérés explicitement.  

| Classification | Membres |  
|:--- |:--- |  
| [**Méthodes**](#methods) | [enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries) |  
| [**Événements**](#events) | [executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled) |  
| [**Types**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Méthodes  

### <a name="enable"></a>activer  

Permet de signaler les `executionContextCreated` événements `executionContextDestroyed` et les `executionContextsCleared` événements.  Lorsque le rapport est activé, l’événement est envoyé immédiatement `executionContextCreated` pour chaque contexte d’exécution existant.  

---  

### <a name="disable"></a>désactiver   

Désactive le signalement des `executionContextCreated` `executionContextDestroyed` événements et des `executionContextsCleared` événements.  

---  

### <a name="evaluate"></a>évaluer  

Évalue l’expression sur l’objet global.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| expression | `string` | Expression à évaluer. |  
| includeCommandLineAPI \(optional\) | `boolean` | Détermine si l’API de ligne de commande doit être disponible pendant l’évaluation. |  
| objectGroup \(optional\) | `string` | Nom de groupe symbolique qui peut être utilisé pour libérer plusieurs objets. |  
| silent \(optional\) | `boolean` | En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution.  Remplace `setPauseOnException` l’état. |  
| contextId \(facultatif\) | [ExecutionContextId](#executioncontextid) | Spécifie dans quel contexte d’exécution effectuer l’évaluation.  Si le paramètre est omis, l’évaluation est effectuée dans le contexte de la page inspectée. |  
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
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificateur de l’objet sur qui appeler la fonction.  `objectId` `executionContextId` L’une ou l’autre doit être spécifiée.  `objectId` doit être issu de la `Runtime.evaluate()` fonction. |  
| arguments \(facultatif\) | [CallArgument[]](#callargument) | Arguments d’appel.  Tous les arguments d’appel doivent appartenir au même monde JavaScript que l’objet cible. |  
| booléen \(facultatif\) | `boolean` | En mode silencieux, les exceptions lancées lors de l’évaluation ne sont pas signalées et ne suspendent pas l’exécution. Remplace `setPauseOnException` l’état. |  
| returnByValue \(optional\) | `boolean` | Si le résultat est censé être un objet JSON qui doit être envoyé par valeur. |  
| awaitPromise \(optional\) | `boolean` | Si l’exécution doit être résolue pour la valeur et le retour une fois `await` la promesse attendue résolue. |  
| executionContextId \(optional\) | [ExecutionContextId](#executioncontextid) | Spécifie le contexte d’exécution sur lequel l’objet global sera utilisé pour appeler la fonction.  Soit
`executionContextId` ou `objectId` doit être spécifié |  
| objectGroup \(optional\) | `string` | Nom de groupe symbolique qui peut être utilisé pour libérer plusieurs objets.  Si `objectGroup` elle n’est pas spécifiée `objectId` et qu’elle l’est, elle `objectGroup` sera héritée de l’objet. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Résultat de l’appel. |  

---  

### <a name="awaitpromise"></a>awaitPromise  

Ajoutez un handler à la promesse avec un ID d’objet promise donné.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| promiseObjectId | [RemoteObjectId](#remoteobjectid) | Identificateur de la promesse. |  
| returnByValue \(optional\) | booléen | Si le résultat est censé être un objet JSON qui doit être envoyé par valeur. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [RemoteObject](#remoteobject) | Résultat de la promesse.  Contient la valeur rejetée si la promesse a été rejetée. |  

---  

### <a name="getproperties"></a>getProperties  

Renvoie les propriétés d’un objet donné. Le groupe d’objets du résultat est hérité de l’objet cible.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Identificateur de l’objet pour qui renvoyer les propriétés.  `objectId` doit être issu de la `Debugger.evaluateOnCallFrame()` fonction. |  
| ownProperties \(optional\) | `boolean` | Si `true` , renvoie les propriétés appartenant uniquement à l’élément lui-même, et non à sa chaîne prototype. |  
| accessorPropertiesOnly \(optional\) | `boolean` | **Expérimental**.  Si `true` , renvoie les propriétés d’accesseur \(avec getter/setter\) uniquement ; les propriétés internes ne sont pas renvoyées non plus. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [PropertyDescriptor[]](#propertydescriptor) | Propriétés de l’objet. |  

---  

### <a name="globallexicalscopenames"></a>globalLexicalScopeNames  

Renvoie toutes les variables let, const et class de l’étendue globale de la console.  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| names | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a>releaseObject  

Libère l’objet distant avec un ID donné.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Identificateur de l’objet à libérer. |  

---  

### <a name="releaseobjectgroup"></a>releaseObjectGroup  

Libère tous les objets distants appartenant à un groupe donné.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| objectGroup | `string` | Nom du groupe d’objets symboliques. |  

---  

### <a name="discardconsoleentries"></a>discardConsoleEntries  

Rejette les exceptions collectées et les appels d’API de console.  

---  

## <a name="events"></a>Événements  

### <a name="executioncontextcreated"></a>executionContextCreated  

Émis lors de la création d’un contexte d’exécution.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| context | [ExecutionContextDescription](#executioncontextdescription) | Contexte d’exécution nouvellement créé. |  

---  

### <a name="executioncontextdestroyed"></a>executionContextDestroyed  

Émis lorsque le contexte d’exécution est détruit.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| executionContextId | [ExecutionContextId](#executioncontextid) | ID du contexte détruit. |  

---  

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

### <a name="consoleapicalled"></a>consoleAPICalled  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| type | `string` | Type de l’appel.  Valeurs autorisées  `log` : , , , , , , , `info` , , , `warning` , , , `error` , `debug` `assert` `table` `trace` `dir` , `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` `startGroupCollapsed` et `endGroup` |  
| args | [RemoteObject[]] (#remoteobject | Arguments d’appel. |  
| executionContextId | [ExecutionContextId](#executioncontextid) | Identificateur du contexte dans lequel l’appel de console a été effectué. |  
| timestamp \(optional\) | [Horodateur](#timestamp) | Appel de l’timestamp. |  
| stackTrace \(optional\) | [StackTrace](#stacktrace) | Trace de pile capturée si disponible. |  

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
| subtype \(optional\) | `string` | Conseil de sous-type d’objet.  Spécifié pour les `object` valeurs de type uniquement.  Valeurs autorisées  `null` : `error` , `promise` et `node` |  
| className \(optional\) | `string` | Nom de la classe d’objet \(constructor\).  Spécifié pour les `object` valeurs de type uniquement. |  
| value \(optional\) | `any` | Valeur de l’objet distant en cas de valeurs primitives ou de valeurs JSON \(si elle a été demandée\). |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | La valeur primitive qui ne peut pas être stringified JSON n’a `value` pas , mais obtient cette propriété. |  
| description \(facultatif\) | `string` | Représentation sous la chaîne de l’objet. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid) | Identificateur d’objet unique \(pour les valeurs non primitives\). |  
| msDebuggerPropertyId \(optional\) | `string` | **Expérimental**.  Microsoft : ID de propriété de débogger associé pour cet objet. |  

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

Représente l’argument d’appel de fonction.  Soit l’ID d’objet distant, la primitive, la valeur de primitive non personnalisable, soit aucune des `objectId` `value` valeurs \(pour undefined\) ne doit être spécifiée.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| value \(optional\) | `any` | Valeur de primitive ou objet javascript sérialisable. |  
| unserializableValue \(optional\) | [UnserializableValue](#unserializablevalue) | Valeur de primitive qui ne peut pas être stringified JSON. |  
| objectId \(optional\) | [RemoteObjectId](#remoteobjectid)] | Handle d’objet distant. |  

---  

### <a name="executioncontextid-integer"></a>ExecutionContextId, integer  

<a name="executioncontextid"></a>  

ID d’un contexte d’exécution.  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a>Objet ExecutionContextDescription  

<a name="executioncontextdescription"></a>  

Description d’un monde isolé.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| id | [ExecutionContextId](#executioncontextid) | ID unique du contexte d’exécution.  Il peut être utilisé pour spécifier dans quel contexte d’exécution
l’évaluation de script doit être effectuée. |  
| origin | `string` | Origine du contexte d’exécution. |  
| name | `string` | Nom lisible par l’homme décrivant un contexte donné. |  

---  

### <a name="exceptiondetails-object"></a>Objet ExceptionDetails  

<a name="exceptiondetails"></a>  

Informations détaillées sur l’exception (ou l’erreur) qui a été lancée lors de la compilation ou de l’exécution du script.  

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
| scriptId | [ScriptId](#scriptid) | ID de script JavaScript. ScriptId sera vide si le débogger n’est pas activé. |  
| url | `string` | Nom ou URL du script JavaScript. |  
| lineNumber | `integer` | Numéro de ligne de script JavaScript \(0-based\). |  
| columnNumber | entier | Numéro de colonne de script JavaScript \(basé sur 0\). |  

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
