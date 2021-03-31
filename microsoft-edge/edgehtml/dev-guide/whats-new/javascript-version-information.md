---
title: Informations sur la version JavaScript
description: Comparez la prise en charge du langage JavaScript à l’ensemble des applications Microsoft Edge, Microsoft Store et Internet Explorer
ms.prod: microsoft-edge
ms.topic: language-reference
author: MSEdgeTeam
ms.author: msedgedevrel
keywords: Edge, IE, chakra, JScript, WWA, applications du Windows Store
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f420b0546f623b5b1c1d43a7b7237a888f97715
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233142"
---
# Informations sur la version JavaScript  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

La prise en charge de JavaScript varie entre les applications Microsoft Edge, Microsoft Store et différents modes de document d’Internet Explorer \(IE \). Pour plus d’informations sur le contrôle de version du code de document IE, voir définition de la [compatibilité du document](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).  

Le tableau suivant résume la prise en charge JavaScript entre les applications Internet Explorer, Microsoft Edge et Microsoft Store.  
  
> [!IMPORTANT]
> Les fonctionnalités expérimentales (activées à partir de `about:flags` \) sont indiquées par `Exp` . Dans certains cas, la prise en charge des applications du Windows Store varie en fonction des applications Windows 8 \(V8 \) et Windows 10 \(version 10 \) et de la version de bureau de Windows, comme indiqué.  
  
 | Élément Language | Excentriques, normes d’Internet Explorer 6, normes d’Internet Explorer 7 | Normes d’Internet Explorer 8 | Normes d’Internet Explorer 9 | Normes d’Internet Explorer 10 | Normes d’Internet Explorer 11 | MicrosoftEdge | Applications du Windows Store |  
 |:--- |:--- |:--- |:--- |:--- |:--- |:--- |:--- |  
| [__proto \ _ \ _ Property (objet)](/scripting/javascript/reference/proto-property-object-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (téléphone): Y |  
| [$1... $9 Propriétés (RegExp)](/scripting/javascript/reference/dollar-1-dot-dot-dot-dollar-9-properties-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété 0n](/scripting/javascript/reference/0-dot-dot-dot-n-properties-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction ABS](/scripting/javascript/reference/math-abs-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ACOS, fonction](/scripting/javascript/reference/math-acos-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction acosh](/scripting/javascript/reference/math-acosh-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Objet ActiveXObject](/scripting/javascript/reference/activexobject-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Opérateur d’assignation d’addition (+ =)](/scripting/javascript/reference/addition-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’addition (+)](/scripting/javascript/reference/addition-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [appliquer la méthode](/scripting/javascript/reference/apply-method-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet arguments](/scripting/javascript/reference/arguments-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété arguments](/scripting/javascript/reference/arguments-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet tableau](/scripting/javascript/reference/array-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Tableau. from, fonction (matrice)](/scripting/javascript/reference/array-from-function-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Array. isArray](/scripting/javascript/reference/array-isarray-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Matrice. fonction (matrice)](/scripting/javascript/reference/array-of-function-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Objet ArrayBuffer](/scripting/javascript/reference/arraybuffer-object) | N | N | N | Y | Y | Y | Y |  
| [Fonctions](/scripting/javascript/functions-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Asin, fonction](/scripting/javascript/reference/math-asin-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction Object. assignation (objet)](/scripting/javascript/reference/object-assign-function-object-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Opérateur d’affectation (=)](/scripting/javascript/reference/assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [atan, fonction](/scripting/javascript/reference/math-atan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [atan2, fonction](/scripting/javascript/reference/math-atan2-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode atEnd](/scripting/javascript/reference/atend-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Méthode de liaison](/scripting/javascript/reference/bind-method-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Opérateur de bits et d’assignation (&=)](/scripting/javascript/reference/bitwise-and-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur or au niveau du bit (&)](/scripting/javascript/reference/bitwise-and-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de décalage vers la gauche (< \ <)](/scripting/javascript/reference/bitwise-left-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur NOT binaire (~)](/scripting/javascript/reference/bitwise-not-operator-decrement-tilde-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de bits or d’assignation (&#124;=)](/scripting/javascript/reference/bitwise-or-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur or au niveau du bit (&#124;)](/scripting/javascript/reference/bitwise-or-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de décalage vers la droite binaire (>>)](/scripting/javascript/reference/bitwise-right-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’assignation votre binaire (^ =)](/scripting/javascript/reference/bitwise-xor-assignment-operator-decrement-hat-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de votre binaire (^)](/scripting/javascript/reference/bitwise-xor-operator-decrement-hat-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Blink](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Bold](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet booléen](/scripting/javascript/reference/boolean-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction Break](/scripting/javascript/reference/break-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode d’appel](/scripting/javascript/reference/call-method-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété de l’appelant](/scripting/javascript/reference/callee-property-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Caller](/scripting/javascript/reference/caller-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction catch](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction ceil](/scripting/javascript/reference/math-ceil-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode charAt](/scripting/javascript/reference/charat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode charCodeAt](/scripting/javascript/reference/charcodeat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction de classe](/scripting/javascript/reference/class-statement-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> version 10: exp. |  
| [Méthode codePointAt (chaîne)](/scripting/javascript/reference/codepointat-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Opérateur virgule (,)](/scripting/javascript/reference/comma-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [(Instruction de commentaire sur une ligne)](/scripting/javascript/reference/comment-statements-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [/*.. \ */(Instruction de commentaire multiligne)](/scripting/javascript/reference/comment-statements-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateurs de comparaison](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Compile](/scripting/javascript/reference/compile-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Concat (matrice)](/scripting/javascript/reference/concat-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Concat (chaîne)](/scripting/javascript/reference/concat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Compilation conditionnelle](/scripting/javascript/advanced/conditional-compilation-javascript) | Y | Y | Y | Y | N | N | N |  
| [Variables de compilation conditionnelle](/scripting/javascript/advanced/conditional-compilation-variables-javascript) | Y | Y | Y | Y | N | N | N |  
| [Opérateur conditionnel (ternaire) (?:)](/scripting/javascript/reference/conditional-ternary-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Constructor](/scripting/javascript/reference/constructor-property-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction Const](/scripting/javascript/reference/const-statement-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (téléphone): Y |  
| [Instruction continue](/scripting/javascript/reference/continue-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [COS, fonction](/scripting/javascript/reference/math-cos-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction créer](/scripting/javascript/reference/object-create-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objet DataView](/scripting/javascript/reference/dataview-object) | N | N | N | Y | Y | Y | Y |  
| [Objet date](/scripting/javascript/reference/date-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Déboguer un objet](/scripting/javascript/reference/debug-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Debug. setNonUserCodeExceptions](/scripting/javascript/reference/debug-setnonusercodeexceptions-property) | N | N | N | Y | Y | Y | Y |  
| [Propriété Debug. setNonUserCodeExceptions](/scripting/javascript/reference/debug-setnonusercodeexceptions-property) | N | N | N | Y | Y | Y | Y |  
| [Instruction Debugger](/scripting/javascript/reference/debugger-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction decodeURI](/scripting/javascript/reference/decodeuri-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction DecodeURIComponent](/scripting/javascript/reference/decodeuricomponent-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de décrémentation (--)](/scripting/javascript/reference/increment-and-decrement-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonctions](/scripting/javascript/functions-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> version 10: exp. |  
| [Fonction defineProperties](/scripting/javascript/reference/object-defineproperties-function-javascript) | N | X.y. | Y | Y | Y | Y | Y |  
| [Fonction defineProperty](/scripting/javascript/reference/object-defineproperty-function-javascript) | N | X.y. | Y | Y | Y | Y | Y |  
| [Opérateur de suppression](/scripting/javascript/reference/delete-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Description](/scripting/javascript/reference/description-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode dimensions](/scripting/javascript/reference/dimensions-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’affectation de division (/=)](/scripting/javascript/reference/division-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de division (/)](/scripting/javascript/reference/division-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [do... Instruction while](/scripting/javascript/reference/do-dot-dot-dot-while-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [E constante](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [encodeURI](/scripting/javascript/reference/encodeuri-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction de composant encodeURI](/scripting/javascript/reference/encodeuricomponent-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode d’entrée (matrice)](/scripting/javascript/reference/entries-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Objet Enumerator](/scripting/javascript/reference/enumerator-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Constantes de nombre](/scripting/javascript/reference/number-constants-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Opérateur d’égalité (= =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet d’erreur](/scripting/javascript/reference/error-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Stack (erreur)](/scripting/javascript/reference/stack-property-error-javascript) | N | N | N | Y | Y | Y | Y |  
| [Propriété stackTraceLimit (erreur)](/scripting/javascript/reference/stacktracelimit-property-error-javascript) | N | N | N | Y | Y | Y | Y |  
| [Fonction Escape](/scripting/javascript/reference/escape-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [eval, fonction](/scripting/javascript/reference/eval-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode exec](/scripting/javascript/reference/exec-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [chaque méthode](/scripting/javascript/reference/every-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Fonction exp](/scripting/javascript/reference/math-exp-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Fill (matrice)](/scripting/javascript/reference/fill-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Méthode de filtre](/scripting/javascript/reference/filter-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Déclaration finale](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode findIndex (matrice)](/scripting/javascript/reference/findindex-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Méthode Fixed](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet Float32Array](/scripting/javascript/reference/float32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Float64Array](/scripting/javascript/reference/float64array-object) | N | N | N | Y | Y | Y | Y |  
| [plancher, fonction](/scripting/javascript/reference/math-floor-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [fontcolor](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode FontSize](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [pour une instruction](/scripting/javascript/reference/for-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode forEach](/scripting/javascript/reference/foreach-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [pour... dans l’instruction](/scripting/javascript/reference/for-dot-dot-dot-in-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [pour... d’instruction](/scripting/javascript/reference/for-dot-dot-dot-of-statement-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Fonction Freeze](/scripting/javascript/reference/object-freeze-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Fonction fromCharCode](/scripting/javascript/reference/string-fromcharcode-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction fromCodePoint](/scripting/javascript/reference/string-fromcodepoint-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Objet fonction](/scripting/javascript/reference/function-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction fonction](/scripting/javascript/reference/function-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Générateurs nombres](/scripting/javascript/advanced/iterators-and-generators-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> version 10: exp. |  
| [getDate, méthode](/scripting/javascript/reference/getdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getDay](/scripting/javascript/reference/getday-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getFullYear](/scripting/javascript/reference/getfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getHours](/scripting/javascript/reference/gethours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getItem](/scripting/javascript/reference/getitem-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getMilliseconds](/scripting/javascript/reference/getmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getMinutes](/scripting/javascript/reference/getminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getMonth](/scripting/javascript/reference/getmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [GetObject, fonction](/scripting/javascript/reference/getobject-function-javascript) | Y | Y | N | N | N | N | N |  
| [Fonction getOwnPropertyDescriptor](/scripting/javascript/reference/object-getownpropertydescriptor-function-javascript) | N | X.y. | Y | Y | Y | Y | Y |  
| [Fonction getOwnPropertyNames](/scripting/javascript/reference/object-getownpropertynames-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Fonction getPrototypeOf](/scripting/javascript/reference/object-getprototypeof-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode getSeconds](/scripting/javascript/reference/getseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getTime](/scripting/javascript/reference/gettime-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getTimezoneOffset](/scripting/javascript/reference/gettimezoneoffset-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCDate](/scripting/javascript/reference/getutcdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCDay](/scripting/javascript/reference/getutcday-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCFullYear](/scripting/javascript/reference/getutcfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCHours](/scripting/javascript/reference/getutchours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCMilliseconds](/scripting/javascript/reference/getutcmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCMinutes](/scripting/javascript/reference/getutcminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getUTCMonth](/scripting/javascript/reference/getutcmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getUTCSeconds](/scripting/javascript/reference/getutcseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode getVarDate](/scripting/javascript/reference/getvardate-method-date-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [getYear, méthode](/scripting/javascript/reference/getyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet global](/scripting/javascript/reference/global-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété globale](/scripting/javascript/reference/global-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur supérieur à (>)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur supérieur ou égal à (>=)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode hasOwnProperty](/scripting/javascript/reference/hasownproperty-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthodes de balise HTML](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction hypot](/scripting/javascript/reference/math-hypot-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Opérateur d’identité (= = =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Si... Instruction Else](/scripting/javascript/reference/if-dot-dot-dot-else-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété ignoreCase](/scripting/javascript/reference/ignorecase-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction imul](/scripting/javascript/reference/math-imul-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Opérateur in](/scripting/javascript/reference/in-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode include (chaîne)](/scripting/javascript/reference/includes-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Opérateur incrément (+ +)](/scripting/javascript/reference/increment-and-decrement-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété index](/scripting/javascript/reference/index-property-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode indexOf (matrice)](/scripting/javascript/reference/indexof-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode indexOf (chaîne)](/scripting/javascript/reference/indexof-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’inégalité (! =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante Infinity](/scripting/javascript/reference/infinity-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété d’entrée ($ _)](/scripting/javascript/reference/input-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur instanceof](/scripting/javascript/reference/instanceof-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet Int8Array](/scripting/javascript/reference/int8array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Int16Array](/scripting/javascript/reference/int16array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Int32Array](/scripting/javascript/reference/int32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Intl. COLLATE](/scripting/javascript/reference/intl-collator-object-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (téléphone): Y |  
| [Objet Intl. DateTimeFormat](/scripting/javascript/reference/intl-datetimeformat-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Objet Intl. NumberFormat](/scripting/javascript/reference/intl-numberformat-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Fonction isFinite](/scripting/javascript/reference/isfinite-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [isArray, fonction](/scripting/javascript/reference/array-isarray-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Fonction IsExtensible](/scripting/javascript/reference/object-isextensible-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Fonction isFrozen](/scripting/javascript/reference/object-isfrozen-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Fonction isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Fonction isNaN](/scripting/javascript/reference/isnan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction isNaN (nombre)](/scripting/javascript/reference/number-isnan-function-number-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Format de date ISO](/scripting/javascript/date-and-time-strings-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode IsPrototypeOf](/scripting/javascript/reference/isprototypeof-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction isSealed](/scripting/javascript/reference/object-issealed-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode Italic](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Itérateurs](/scripting/javascript/advanced/iterators-and-generators-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Méthode Item](/scripting/javascript/reference/item-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Join](/scripting/javascript/reference/join-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet JSON](/scripting/javascript/reference/json-object-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Fonction Keys](/scripting/javascript/reference/object-keys-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode Keys (matrice)](/scripting/javascript/reference/keys-method-array-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Instruction étiquetée](/scripting/javascript/reference/labeled-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété lastIndex](/scripting/javascript/reference/lastindex-property-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [lastIndexOf méthode (matrice)](/scripting/javascript/reference/lastindexof-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [lastIndexOf, méthode (chaîne)](/scripting/javascript/reference/lastindexof-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [lastMatch, propriété ($&)](/scripting/javascript/reference/lastmatch-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété lastParen ($ +)](/scripting/javascript/reference/lastparen-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [LBound, méthode](/scripting/javascript/reference/lbound-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété leftContext ($ ')](/scripting/javascript/reference/leftcontext-property-dollar-grave-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’assignation de décalage gauche (<<=)](/scripting/javascript/reference/left-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Length (arguments)](/scripting/javascript/reference/length-property-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Length, propriété (matrice)](/scripting/javascript/reference/length-property-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Length (fonction)](/scripting/javascript/reference/length-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Length (chaîne)](/scripting/javascript/reference/length-property-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur inférieur à (<)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur inférieur ou égal à (<=)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction WHERE](/scripting/javascript/reference/let-statement-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Méthode Link](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LN2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LN10](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode localeCompare](/scripting/javascript/reference/localecompare-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [log, fonction](/scripting/javascript/reference/math-log-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LOG2E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LOG10E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur logique AND (&&)](/scripting/javascript/reference/logical-and-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur NOT logique (!)](/scripting/javascript/reference/logical-not-operator-decrement-exclpt-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur OR logique (&#124;&#124;)](/scripting/javascript/reference/logical-or-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Map](/scripting/javascript/reference/map-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objet Map](/scripting/javascript/reference/map-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Méthode match](/scripting/javascript/reference/match-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet mathématique](/scripting/javascript/reference/math-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction max](/scripting/javascript/reference/math-max-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante MAX_VALUE](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété de message](/scripting/javascript/reference/message-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction min](/scripting/javascript/reference/math-min-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante MIN_VALUE](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’affectation de reste (% =)](/scripting/javascript/reference/modulus-assignment-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur reste (%)](/scripting/javascript/reference/modulus-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode moveFirst](/scripting/javascript/reference/movefirst-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode moveNext](/scripting/javascript/reference/movenext-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété MultiLine](/scripting/javascript/reference/multiline-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’assignation de multiplication (* =)](/scripting/javascript/reference/multiplication-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de multiplication (*)](/scripting/javascript/reference/multiplication-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Name](/scripting/javascript/reference/name-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NaN (globale)](/scripting/javascript/reference/nan-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NaN (nombre)](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NEGATIVE_INFINITY](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [nouvel opérateur](/scripting/javascript/reference/new-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur pas d’identité (! = =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction Now](/scripting/javascript/reference/date-now-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objet numérique](/scripting/javascript/reference/number-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété Number](https://developer.mozilla.org/docs/Web/JavaScript/Microsoft_Extensions/Error.number) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet objet](/scripting/javascript/reference/object-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Ordre de priorité des opérateurs](/scripting/javascript/operator-subtractprecedence-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Date. Parse](/scripting/javascript/reference/date-parse-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [JSON. Parse](/scripting/javascript/reference/json-parse-function-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Fonction parseFloat](/scripting/javascript/reference/parsefloat-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction parseine](/scripting/javascript/reference/parseint-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante PI](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode pop](/scripting/javascript/reference/pop-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante POSITIVE_INFINITY](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction pow](/scripting/javascript/reference/math-pow-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction preventExtensions](/scripting/javascript/reference/object-preventextensions-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objet promise](/scripting/javascript/reference/promise-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Propriété prototype](/scripting/javascript/reference/prototype-property-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode propertyIsEnumerable](/scripting/javascript/reference/propertyisenumerable-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet proxy](/scripting/javascript/reference/proxy-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Méthode de transmission](/scripting/javascript/reference/push-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction aléatoire](/scripting/javascript/reference/math-random-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [RAW](/scripting/javascript/reference/string-raw-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Méthode Reduce](/scripting/javascript/reference/reduce-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode reduceRight](/scripting/javascript/reference/reduceright-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objet RegExp](/scripting/javascript/reference/regexp-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet Regular expression](/scripting/javascript/reference/regular-expression-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Syntaxe d’expression régulière](https://msdn.microsoft.com/ab0766e1-7037-45ed-aa23-706f58358c0e) | Y | Y | Y | Y | Y | Y | Y |  
| [Indicateur d’expression régulière/y](/scripting/javascript/reference/regular-expression-object-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> version 10: exp. |  
| [Méthode REPEAT (chaîne)](/scripting/javascript/reference/repeat-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Méthode Replace](/scripting/javascript/reference/replace-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonctions](/scripting/javascript/functions-javascript) | N | N | N | N | N | N | v 8.1: N <br /> version 10: Y |  
| [Instruction return](/scripting/javascript/reference/return-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode inverse](/scripting/javascript/reference/reverse-method-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété rightContext ($ ')](/scripting/javascript/reference/rightcontext-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’assignation de décalage vers la droite (>>=)](/scripting/javascript/reference/right-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction arrondi](/scripting/javascript/reference/math-round-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction ScriptEngine](/scripting/javascript/reference/scriptengine-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction ScriptEngineBuildVersion](/scripting/javascript/reference/scriptenginebuildversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ScriptEngineMajorVersion, fonction](/scripting/javascript/reference/scriptenginemajorversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction ScriptEngineMinorVersion](/scripting/javascript/reference/scriptengineminorversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction SCELLEE](/scripting/javascript/reference/object-seal-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode de recherche](/scripting/javascript/reference/search-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Définir l’objet](/scripting/javascript/reference/set-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Méthode setDate](/scripting/javascript/reference/setdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [setFullYear, méthode](/scripting/javascript/reference/setfullyear-method-date-javascript) |  | Y | Y | Y | Y | Y | Y |  
| [Méthode setHours](/scripting/javascript/reference/sethours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setMilliseconds](/scripting/javascript/reference/setmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setMinutes](/scripting/javascript/reference/setminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setMonth](/scripting/javascript/reference/setmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setSeconds](/scripting/javascript/reference/setseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setTime](/scripting/javascript/reference/settime-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCDate](/scripting/javascript/reference/setutcdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCFullYear](/scripting/javascript/reference/setutcfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCHours](/scripting/javascript/reference/setutchours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCMilliseconds](/scripting/javascript/reference/setutcmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCMinutes](/scripting/javascript/reference/setutcminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCMonth](/scripting/javascript/reference/setutcmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setUTCSeconds](/scripting/javascript/reference/setutcseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode setYear](/scripting/javascript/reference/setyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Shift](/scripting/javascript/reference/shift-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Sin, fonction](/scripting/javascript/reference/math-sin-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Slice (matrice)](/scripting/javascript/reference/slice-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Slice (chaîne)](/scripting/javascript/reference/slice-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [petites méthodes](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode](/scripting/javascript/reference/some-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode de tri](/scripting/javascript/reference/sort-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriété source](/scripting/javascript/reference/source-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode splice](/scripting/javascript/reference/splice-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Split](/scripting/javascript/reference/split-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonctions](/scripting/javascript/functions-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Fonction racine](/scripting/javascript/reference/math-sqrt-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante SQRT1_2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante SQRT2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [utiliser une directive stricte](/scripting/javascript/reference/use-strict-directive) | N | N | N | Y | Y | Y | Y |  
| [Méthode Strike](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet String](/scripting/javascript/reference/string-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction JSON. stringify](/scripting/javascript/reference/json-stringify-function-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [sous-méthode](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode substr](/scripting/javascript/reference/substr-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode de sous-chaîne](/scripting/javascript/reference/substring-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’assignation de soustraction (-=)](/scripting/javascript/reference/subtraction-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de soustraction (-)](/scripting/javascript/reference/subtraction-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [sup, méthode](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction switch](/scripting/javascript/reference/switch-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet Symbol](/scripting/javascript/reference/symbol-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Tan, fonction](/scripting/javascript/reference/math-tan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Chaînes de modèle](/scripting/javascript/advanced/template-strings-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Méthode de test](/scripting/javascript/reference/test-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Cette affirmation](/scripting/javascript/reference/this-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instruction throw](/scripting/javascript/reference/throw-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toArray](/scripting/javascript/reference/toarray-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toDateString](/scripting/javascript/reference/todatestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toExponential, méthode](/scripting/javascript/reference/toexponential-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toFixed](/scripting/javascript/reference/tofixed-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toGMTString](/scripting/javascript/reference/togmtstring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toISOString](/scripting/javascript/reference/toisostring-method-date-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Méthode toJSON](/scripting/javascript/reference/tojson-method-date-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Méthode toLocaleDateString](/scripting/javascript/reference/tolocaledatestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toLocaleLowercase](/scripting/javascript/reference/tolocalelowercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toLocaleString](/scripting/javascript/reference/tolocalestring-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toLocaleTimeString](/scripting/javascript/reference/tolocaletimestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toLocaleUppercase](/scripting/javascript/reference/tolocaleuppercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toLowerCase](/scripting/javascript/reference/tolowercase-method-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toPrecision](/scripting/javascript/reference/toprecision-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toString](/scripting/javascript/reference/tostring-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toTimeString](/scripting/javascript/reference/totimestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode toUpperCase](/scripting/javascript/reference/touppercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toUTCString](/scripting/javascript/reference/toutcstring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode Trim](/scripting/javascript/reference/trim-method-string-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Instruction try](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur typeof](/scripting/javascript/reference/typeof-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [UBound, méthode](/scripting/javascript/reference/ubound-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet Uint8Array](/scripting/javascript/reference/uint8array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Uint16Array](/scripting/javascript/reference/uint16array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Uint32Array](/scripting/javascript/reference/uint32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objet Uint8ClampedArray](/scripting/javascript/reference/uint8clampedarray-object-javascript) | N | N | N | N | Y | Y | V8: non <br /> v 8.1 (Win): Oui <br /> v 8.1 (téléphone): non <br /> version 10: Y |  
| [Opérateur de négation unaire (-)](/scripting/javascript/reference/subtraction-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante non définie](/scripting/javascript/reference/undefined-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction sans échappement](/scripting/javascript/reference/unescape-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Caractères d’échappement de point de code Unicode](/scripting/javascript/advanced/special-characters-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Méthode unshift](/scripting/javascript/reference/unshift-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur d’assignation de décalage droite non signé (>>>=)](/scripting/javascript/reference/unsigned-right-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Opérateur de décalage vers la droite non signé (>>>)](/scripting/javascript/reference/unsigned-right-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [utiliser une directive stricte](/scripting/javascript/reference/use-strict-directive) | N | N | N | Y | Y | Y | Y |  
| [Fonction UTC](/scripting/javascript/reference/date-utc-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode valueOf](/scripting/javascript/reference/valueof-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Méthode values (matrice)](/scripting/javascript/reference/values-method-array-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Instruction var](/scripting/javascript/reference/var-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet VBArray](/scripting/javascript/reference/vbarray-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Opérateur void](/scripting/javascript/reference/void-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet WeakMap](/scripting/javascript/reference/weakmap-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Objet WeakSet](/scripting/javascript/reference/weakset-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> version 10: Y |  
| [Instruction while](/scripting/javascript/reference/while-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objet WinRTError](/scripting/javascript/reference/winrterror-object-javascript) | N | N | N | Y | Y | Y | Y |  
| [Instruction with](/scripting/javascript/reference/with-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction Write](/scripting/javascript/reference/debug-write-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fonction writeln](/scripting/javascript/reference/debug-writeln-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
  
 \ * Prend en charge les objets DOM sans objets définis par l’utilisateur.  Les `enumerable` `configurable` attributs and peuvent être spécifiés, mais ils ne sont pas utilisés.  
