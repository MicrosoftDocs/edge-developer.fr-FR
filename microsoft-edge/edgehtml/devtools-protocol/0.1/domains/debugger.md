---
description: Référence du protocole DevTools version 0.1 (EdgeHTML) pour le domaine du débogueur.  Le domaine du déboguer expose les fonctionnalités de débogage JavaScript.  Il permet de définir et de supprimer des points d’arrêt, d’exécuter pas à pas, d’explorer les traces de pile, etc.
title: Domaine du débogueur - DevTools Protocol Version 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397677"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a>Domaine du débogueur - DevTools Protocol Version 0.1 (EdgeHTML)  
  
Le domaine du déboguer expose les fonctionnalités de débogage JavaScript.  Il permet de définir et de supprimer des points d’arrêt, d’exécuter pas à pas, d’explorer les traces de pile, etc.

| Classification | Membres |  
|:--- |:--- |  
| [Méthodes](#methods) | [enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) [](#stepout) |  
| [Événements](#events) | [scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed) |  
| [Types](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope) |  
| [Dépendances](#dependencies) | [Runtime](./runtime.md) |  

## <a name="methods"></a>Méthodes  

### <a name="enable"></a>activer  

Active le débogger pour la page donnée.  Les clients ne doivent pas supposer que le débogage a été activé jusqu’à ce que le résultat de cette commande soit reçu.  

&nbsp;  

---  

### <a name="disable"></a>désactiver   

Désactive le débogger pour une page donnée.  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a>getPossibleBreakpoints  

Renvoie les emplacements possibles pour le point d’arrêt.  ScriptId dans les emplacements de plage de début et de fin doit être identique.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| start | [Emplacement](#location) | Début de la plage pour rechercher les emplacements de points d’arrêt possibles. |  
| terminer | [Emplacement](#location) | Fin de la plage pour rechercher les emplacements de points d’arrêt possibles dans \(à l’exclusion de\).  Lorsqu’il n’est pas spécifié, la fin des scripts est utilisée comme fin de plage. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| emplacements | [BreakLocation](#breaklocation) | Liste des emplacements de points d’arrêt possibles. |  

---  

### <a name="setbreakpointsactive"></a>setBreakpointsActive  

Active/désactive tous les points d’arrêt sur la page.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| active | `boolean` | Nouvelle valeur pour l’état actif des points d’arrêt. |  

---  

### <a name="setbreakpointbyurl"></a>setBreakpointByUrl  

Définit le point d’arrêt JavaScript à un emplacement donné spécifié par l’URL ou l’URL regex.  Une fois cette commande émise, tous les scripts déjà assués ont des points d’arrêt résolus et renvoyés dans la `locations` propriété.  Une autre correspondance de l’examen des scripts entraîne l’émission `breakpointResolved` d’événements ultérieurs.  Ce point d’arrêt logique survivra au rechargement des pages.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| lineNumber | `integer` | Numéro de ligne sur le point d’arrêt. |  
| url \(optional\) | `string` | URL des ressources pour définir le point d’arrêt. |  
| urlRegex \(facultatif\) | `string` | Modèle d’regex pour les URL des ressources sur les points d’arrêt.  `url` `urlRegex` L’un ou l’autre doit être spécifié. |  
| columnNumber \(optional\) | `integer` | Décalez la ligne pour définir le point d’arrêt sur. |  
| condition \(optional\) | `string` | Expression à utiliser comme condition de point d’arrêt.  Lorsqu’il est spécifié, le débogger s’arrête uniquement sur le point d’arrêt si cette expression est évaluée à true. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID du point d’arrêt créé pour référence supplémentaire. |  
| emplacements | [Location[]](#location) | Liste des emplacements où ce point d’arrêt a été résolu lors de l’ajout. |  

---  

### <a name="setbreakpoint"></a>setBreakpoint  

Définit le point d’arrêt JavaScript à un emplacement donné.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| location | [Emplacement](#location) | Emplacement dans le point d’arrêt. |  
| condition \(optional\) | `string` | Expression à utiliser comme condition de point d’arrêt.  Lorsqu’il est spécifié, le débogger s’arrête uniquement sur le point d’arrêt si cette expression est évaluée à true. |  

| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID du point d’arrêt créé pour référence supplémentaire. |  
| actualLocation | [Emplacement](#location) | Emplacement où ce point d’arrêt a été résolu. |  

---  

### <a name="removebreakpoint"></a>removeBreakpoint  

Supprime le point d’arrêt JavaScript.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a>stepOver  

Étapes au-dessus de l’instruction.  

&nbsp;  

---  

### <a name="stepinto"></a>stepInto  

Étapes de l’appel de fonction.  

&nbsp;  

---  

### <a name="stepout"></a>stepOut  

Sort de l’appel de fonction.  

&nbsp;  

---  

### <a name="pause"></a>pause  

S’arrête sur l’instruction JavaScript suivante.  

&nbsp;  

---  

### <a name="resume"></a>resume  

Reprend l’exécution de JavaScript.  

&nbsp;  

---  

### <a name="getscriptsource"></a>getScriptSource  

Renvoie la source du script avec l’ID donné.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | ID du script pour obtenir la source. |  
| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| scriptSource | `string` | Source du script. |  

---  

### <a name="setpauseonexceptions"></a>setPauseOnExceptions  

Définit une pause sur l’état des exceptions.  Peut être définie pour s’arrêter sur toutes les exceptions, les exceptions non détailles ou aucune exception.  La pause initiale sur l’état des exceptions est `none` .  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| state | `string` | Mettre en pause le mode exceptions.  Valeurs autorisées  `none` : `uncaught` , et `all` |  

---  

### <a name="evaluateoncallframe"></a>evaluateOnCallFrame  

Évalue l’expression sur une trame d’appel donnée.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Identificateur d’image d’appel à évaluer. |  
| expression | `string` | Expression à évaluer. |  
| Renvoie | Type | Détails |  
|:--- |:--- |:--- |  
| result | [Runtime.RemoteObject](./runtime.md#remoteobject) | Wrapper d’objet pour le résultat d’évaluation. |  

---  

### <a name="setvariablevalue"></a>setVariableValue  

Modifie la valeur de la variable dans un callframe.  Les étendues basées sur des objets ne sont pas pris en charge et doivent être désactivées manuellement.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| scopeNumber | `integer` | Nombre d’étendues basé sur 0, tel qu’il était répertorié dans la chaîne d’étendue.  Seuls `local` , et les types `closure` `catch` d’étendue sont autorisés.  D’autres étendues peuvent être manipulées manuellement. |  
| variableName | `string` | Nom de la variable. |  
| newValue | [Runtime.CallArgument](./runtime.md#callargument) | Nouvelle valeur de variable. |  
| callFrameId | [CallFrameId](#callframeid) | ID de l’appel qui contient une variable. |  

---  

### <a name="setblackboxpatterns"></a>setBlackboxPatterns  

**Expérimental**.  Remplacez les modèles de boîte noire précédents par les modèles transmis.  Force le back-end à ignorer la mise en pause/pas à pas dans les scripts avec une URL correspondant à l’un des modèles.  Le débompeur essaiera de laisser un script en boîte noire en le faisant plusieurs fois, en y recourant en `step in` `step out` cas d’échec.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| patterns | `string[]` | Tableau de regexps qui sera utilisé pour vérifier l’état de boîte aux lettres noire de l’URL du script. |  

---  

### <a name="mssetdebuggerpropertyvalue"></a>msSetDebuggerPropertyValue  

**Expérimental**.  Microsoft : définit la propriété spécifiée du débogger sur la valeur spécifiée.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| debuggerPropertyId | `string` | Microsoft : ID de propriété \(c’est-à-dire msDebuggerPropertyId\) à définir. |  
| newValue | `string` | &nbsp; |  

---  

## <a name="events"></a>Événements  

### <a name="scriptparsed"></a>scriptParsed  

Déclenché lorsque le script est interrogé.  Cet événement est également déclenché pour tous les scripts connus et non récollects lors de l’activation du débogueur.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificateur du script en cours d’utilisation. |  
| url | `string` | URL ou nom du script lu \(le caser\). |  
| startLine | `integer` | Décalage de ligne du script dans la ressource avec une URL donnée \(pour les balises de script\). |  
| startColumn | `integer` | Décalage de colonne du script dans la ressource avec une URL donnée. |  
| endLine | `integer` | Dernière ligne du script. |  
| endColumn | `integer` | Longueur de la dernière ligne du script. |  
| executionContextId | [Runtime.ExecutionContextId](./runtime.md#executioncontextid) | Spécifie le contexte de création de script. |  
| sourceMapURL \(facultatif\) | `string` | URL de la carte source associée au script (le cas cas). |  
| length \(optional\) | `integer` | **Expérimental**.  Longueur du script. |  
| msParentId \(optional\) | `string` | **Expérimental**.  Il s’agit de l’ID de document parent. |  
| msMimeType \(optional\) | `string` | **Expérimental**.  Il s’agit du type mime. |  
| msIsDynamicCode \(optional\) | `boolean` | **Expérimental**.  Cela indique s’il s’agit d’un code dynamique. |  
| msLongDocumentId \(optional\) | `integer` | **Expérimental**.  Il s’agit de l’ID de document long. |  

---  

### <a name="breakpointresolved"></a>breakpointResolved  

Déclenché lorsque le point d’arrêt est résolu en un script et un emplacement réels.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Identificateur unique de point d’arrêt. |  
| location | [Emplacement](#location) | Emplacement réel du point d’arrêt. |  
| msLength \(optional\) | `integer` | **Expérimental**.  Microsoft : Longueur du code \(nombre de caractères\) à l’emplacement du point d’arrêt. |  

---  

### <a name="paused"></a>en pause  

Déclenché lorsque les déboggers se cassent pour un point d’arrêt ou une exception.  

| Parameters | Type | Détails |  
|:--- |:--- |:--- |  
| callFrames | [CallFrame[]](#callframe) | Pile d’appels où le débogger s’est arrêté. |  
| reason | `string` | Motif de l’interruption.  Valeurs autorisées  `breakpoint` : , `step` `exception` et `other` |  
| data \(optional\) | `object` | Objet contenant des propriétés auxiliaires spécifiques aux coupures. |  
| hitBreakpoints \(facultatif\) | `string[]` | ID des points d’arrêt d’arrêt |  

---  

### <a name="resumed"></a>reprise  

Déclenché lorsque le débogger reprend l’exécution.  

&nbsp;  

---  

## <a name="types"></a>Types  

### <a name="breakpointid-string"></a>Chaîne BreakpointId  

<a name="breakpointid"></a>  

Identificateur de point d’arrêt.  

&nbsp;  

---  

### <a name="callframeid-string"></a>Chaîne CallFrameId  

<a name="callframeid"></a>  

Identificateur d’image d’appel.  

&nbsp;  

---  

### <a name="location-object"></a>Location, objet  

<a name="location"></a>  

Emplacement dans le code source.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificateur de script tel qu’indiqué dans `Debugger.scriptParsed` le . |  
| lineNumber | `integer` | Numéro de ligne dans le script \(0-based\). |  
| columnNumber \(optional\) | `integer` | Numéro de colonne dans le script \(0-based\). |  
| msLength | `integer` | Microsoft : Longueur du code \(c’est-à-dire le nombre de caractères\) à ce cadre d’appel. |  

---  

### <a name="breaklocation-object"></a>Objet BreakLocation  

<a name="breaklocation"></a>  

Emplacement de rupture dans le code source.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Identificateur de script tel qu’indiqué dans `Debugger.scriptParsed` le . |  
| lineNumber | `integer` | Numéro de ligne dans le script \(0-based\). |  
| columnNumber \(optional\) | `integer` | Numéro de colonne dans le script \(0-based\). |  
| msLength | `integer` | Microsoft : Longueur du code \(c’est-à-dire le nombre de caractères\) à ce cadre d’appel. |  
| type \(optional\) | `string` | Valeurs autorisées  `debuggerStatement` : `call` , et `return` |  

---  

### <a name="callframe-object"></a>Objet CallFrame  

<a name="callframe"></a>  

Image d’appel JavaScript.  Un tableau de cadres d’appel forme la pile d’appels.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Identificateur d’image d’appel.  Cet identificateur n’est valide que lorsque le débogger est suspendu. |  
| functionName | `string` | Nom de la fonction JavaScript appelée sur ce cadre d’appel. |  
| functionLocation \(optional\) | [Emplacement](#location) | **Expérimental**.  Emplacement dans le code source. |  
| location | [Emplacement](#location) | Emplacement dans le code source. |  
| url | `string` | Nom ou URL du script JavaScript. |  
| scopeChain | [Scope[]](#scope) | Chaîne d’étendue pour ce cadre d’appel. |  
| this | [Runtime.RemoteObject](./runtime.md#remoteobject) | `this` pour ce cadre d’appel. |  
| returnValue \(optional\) | [Runtime.RemoteObject](./runtime.md#remoteobject) | Valeur renvoyée, si la fonction est au point de retour. |  

---  

### <a name="scope-object"></a>Objet Scope  

<a name="scope"></a>  

Description de l’étendue.  

| Propriétés | Type | Détails |  
|:--- |:--- |:--- |  
| type | `string` | Type d’étendue.  Valeurs autorisées  `global` : , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` et `module` |  
| object | [Runtime.RemoteObject](./runtime.md#remoteobject) | Objet représentant l’étendue.  Pour et les étendues, il représente l’objet réel ; pour le reste des étendues, il s’agit d’objets temporaires artificielles qui édent les variables d’étendue en tant `global` `with` que propriétés. |  
| name \(optional\) | `string` | &nbsp; |  
| startLocation \(optional\) | [Emplacement](#location) | Emplacement dans le code source où commence l’étendue. |  
| endLocation \(optional\) | [Emplacement](#location) | Emplacement dans le code source où l’étendue se termine. |  

---  

## <a name="dependencies"></a>Dépendances  

[Runtime](./runtime.md)  
