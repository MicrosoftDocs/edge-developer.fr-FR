---
description: Utilisez le moteur JavaScript Chakra standard pour ajouter des fonctionnalités de script à votre application Windows.
title: Hébergement du runtime JavaScript | Documents Microsoft
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 30ec744e-57cc-4ef5-8fe1-d2c27b946548
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9077284d96ff0d9ae22e152329efe9304081ae39
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565282"
---
# Hébergement du runtime JavaScript
Les API d’exécution JavaScript (JsRT) permettent aux applications de bureau, Windows Store et côté serveur qui s’exécutent sur le système d’exploitation Windows d’ajouter des fonctionnalités de script à l’application en utilisant le moteur JavaScript Chakra basé sur des normes, qui est également utilisé par Microsoft Edge et Internet Explorer. Ces API sont disponibles sur Windows 10 et toutes les versions du système d’exploitation Windows sur lequel Internet Explorer version 11,0 est installé sur l’ordinateur. Pour plus d’informations, voir [Reference (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md). Pour plus d’informations sur l’utilisation des JsRT dans les applications du Windows Store, voir [JsRT et la plateforme Windows universelle](#Windows).  
  
> [!NOTE]
>  Cette documentation suppose une connaissance générale du fonctionnement du langage JavaScript.  
  
## Concepts  
 Le fonctionnement de l’hébergement du moteur JavaScript à l’aide des API JsRT dépend de deux concepts clés: runtimes et contextes d’exécution.  
  
 Un *Runtime* représente un environnement d’exécution JavaScript complet. Chaque exécution créée possède son propre tas de nettoyage de la mémoire isolé et, par défaut, son propre thread de compilateur JIT et de nettoyage de la mémoire (CG). Un *contexte d’exécution* représente un environnement JavaScript sur lequel son propre objet global JavaScript est distinct de tous les autres contextes d’exécution. Un Runtime doit contenir plusieurs contextes d’exécution, et dans ce cas, tous les contextes d’exécution partagent le compilateur JIT et le thread CG associés au Runtime.  
  
 Les runtimes représentent un thread d’exécution unique. Un seul Runtime peut être actif sur un thread particulier à la fois, et un Runtime ne peut être actif que sur un thread à la fois. Les runtimes sont locatifs, de telle sorte qu’un Runtime qui n’est pas actif sur un thread (par exemple, n’exécute aucun code JavaScript ou ne répond à aucun appel de l’hôte) peut être utilisé sur tout thread sur lequel il n’existe pas déjà un Runtime actif.  
  
 Les contextes d’exécution sont liés à un Runtime particulier et exécutent du code au sein de ce Runtime. Contrairement aux runtimes, les contextes d’exécution multiples peuvent être actifs sur un thread en même temps. Ainsi, un hôte peut passer un appel dans un contexte d’exécution, ce contexte d’exécution peut rappeler vers l’hôte, et l’hôte peut passer un appel dans un contexte d’exécution différent.  
  
 ![Contextes d’exécution multiples](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting")  
  
 Dans la pratique, sauf si un hôte a besoin d’exécuter du code dans des environnements séparés, il est possible d’utiliser un contexte d’exécution unique. De même, sauf si un hôte doit exécuter plusieurs parties du code en même temps, un seul Runtime suffit.  
  
## Gestion de la mémoire  
 JavaScript est un langage de nettoyage de la mémoire et il existe donc plusieurs considérations à garder à l’esprit lorsque vous travaillez avec les API JsRT à partir d’une autre langue.  
  
 Dans la plupart des cas, le garbage collector JavaScript peut uniquement voir les références à des valeurs à deux emplacements: le tas de son Runtime et la pile. Par conséquent, une référence à une valeur JavaScript qui est stockée à l’intérieur d’une autre valeur JavaScript ou dans une variable locale sur la pile sera toujours visible par le récupérateur de mémoire. Toutefois, les références stockées dans d’autres emplacements (par exemple, les tas gérés par l’hôte ou le système) ne seront pas visibles par le récupérateur de mémoire et pourront entraîner une collection prématurée de valeurs qui sont toujours en cours d’utilisation par l’hôte.  
  
> [!IMPORTANT]
>  Certains compilateurs de langage (comme le compilateur Visual Studio C++) optimisent les variables locales lorsque c’est possible. Il est nécessaire de veiller à ce que les variables locales qui font référence à des valeurs JavaScript se trouvent sur la pile s’il est prévu de conserver ces valeurs actif.  
  
 Si une référence à une valeur JavaScript sera stockée dans un emplacement invisible pour le nettoyage de la mémoire, l’hôte doit ajouter et supprimer manuellement des références à l’aide des API JsRT.  
  
## Gestion des exceptions  
 Quand une exception JavaScript se produit pendant l’exécution du script, le runtime contenant est placé dans un état d’exception. Dans un état d’exception, il n’est pas possible d’exécuter le code et tous les appels d’API échoueront avec le code d’erreur `JsErrorInExceptionState` jusqu’à ce que l’hôte récupère et efface l’exception à l’aide de l' `JsGetAndClearException` API. Si l’hôte retourne à partir d’un rappel JavaScript sans vider le runtime d’un état d’exception, l’exception JavaScript est rélevée dès que le contrôle est transmis au moteur JavaScript. Cela permet également aux rappels d’hôte de «lever» une exception JavaScript en définissant le runtime dans un état d’exception, puis en renvoyant un rappel d’hôte.  
  
 Un hôte n’est pas autorisé à laisser ses propres exceptions internes à être propagées sur un rappel d’hôte: toutes les méthodes de rappel doivent intercepter toutes les exceptions d’hôte avant de redéfinir le contrôle pour le Runtime.  
  
## Utilisation des ressources au moment de l’exécution  
 Les API JsRT présentent un certain nombre de moyens de surveiller et de modifier la façon dont les runtimes utilisent les ressources. Ils sont généralement réparties dans les catégories suivantes:  
  
-   **Utilisation du thread**. Par défaut, chaque Runtime crée un thread de compilateur JIT dédié et un thread de CG dédié qui service ce Runtime. Si un Runtime est créé avec l' `JsRuntimeAttributeDisableBackgroundWork` indicateur, le processus JIT et GC sera exécuté sur le thread d’exécution proprement dit au lieu de threads d’arrière-plan distinctes pour chacun d’eux. Un hôte peut également fournir un rappel de service de thread à l' `JsCreateRuntime` appel, ce qui permet à l’hôte de planifier le fonctionnement du JIT et du CG en fonction du fonctionnement.  
  
-   **Utilisation**de la mémoire. Il existe plusieurs façons de surveiller et de modifier l’utilisation de la mémoire d’un Runtime. Si le runtime s’exécute pendant un certain temps, l’hôte peut spécifier l' `JsRuntimeAttributeEnableIdleProcessing` indicateur lors de la création du runtime, puis appeler `JsIdle` lorsque l’hôte est dans un état inactif. Cela permet au moteur de différer le nettoyage de la mémoire et de gérer le fonctionnement jusqu’au temps d’inactivité.  
  
     L’hôte peut surveiller les nettoyages de la mémoire en appelant `JsSetRuntimeBeforeCollectCallback` . Il peut également surveiller les attributions effectuées par le tas en appelant `JsSetRuntimeMemoryAllocationCallback` . Notez que cette API n’effectue pas de rappel à chaque attribution JavaScript, uniquement lorsque le tas du runtime a besoin d’espace supplémentaire à partir duquel allouer. Le rappel d’allocation de mémoire est autorisé à refuser la demande, ce qui déclenche un nettoyage de la mémoire et, si aucune mémoire n’est disponible, une erreur de mémoire insuffisante dans le Runtime.  
  
     L’hôte peut également appeler `JsSetRuntimeMemoryLimit` pour définir une limite de la quantité de mémoire utilisée par un Runtime. Lorsque le runtime atteint une limite, il déclenche un nettoyage de la mémoire et, si aucune mémoire n’est disponible, une erreur de mémoire insuffisante est levée par le Runtime.  
  
-   **Interruption et évaluation des scripts**. L’hôte peut appeler `JsDisableRuntimeExecution` pour terminer l’exécution au sein d’un Runtime. Cet appel peut être effectué à tout moment et à partir de n’importe quel thread. Dans la mesure où l’arrêt du script dépend de l’insertion de points de protection dans le code, il est possible que le script ne se termine pas au moment précis, mais qu’il le fera très prochainement. Par défaut, les points de protection de fin sont placés de manière conservatrice dans le code généré et ne peuvent pas être couverts par une boucle infinie. La création du Runtime avec l' `JsRuntimeAttributeAllowScriptInterrupt` indicateur amène le runtime à insérer des vérifications supplémentaires pour les boucles infinies, souvent au coût d’une faible surcharge des performances.  
  
     Si un hôte souhaite refuser la génération de code natif par le compilateur JIT, il peut spécifier l' `JsRuntimeAttributeDisableNativeCodeGeneration` indicateur. Un hôte peut également désactiver les scripts de manière dynamique en exécutant des scripts eux-mêmes en spécifiant l' `JsRuntimeAttributeDisableEval` indicateur.  
  
## Débogage et profilage  
 Les API JsRT prennent en charge le débogage et le profil via la technologie d’écriture de script active.  
  
 À partir de Windows 10, le moteur JavaScript Chakra prend en charge le moteur d’ancienne version d’Internet Explorer (MSHTML) et le nouveau moteur Microsoft Edge (EdgeHTML), et vous pouvez le cibler dans JsRT (pour plus d’informations sur le [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md) ). Le débogage d’un script dans Visual Studio fonctionne différemment entre le moteur hérité et le moteur Microsoft Edge. Avec le moteur hérité, l’hôte doit fournir un pointeur d' [interface IDebugApplication](/scripting/winscript/reference/idebugapplication-interface) , qui peut être obtenu à partir d’une instance d' [interface IProcessDebugManager](/scripting/winscript/reference/iprocessdebugmanager-interface) . Le moteur Microsoft Edge `IDebugApplication` est déconseillé, et le moteur Chakra autorise les fonctionnalités de débogage native et de script par le biais du débogueur Visual Studio, sans nécessiter `IDebugApplication` l’implémentation de l’utilisateur.  
  
 Pour faciliter le débogage des scripts dans un contexte d’exécution, le moteur Chakra doit basculer vers l’utilisation de méthodes d’exécution de code moins efficaces. Par exemple, le code déboguable s’exécute généralement plus lentement que le code non déboguable. Par conséquent, avec le moteur hérité, un hôte peut choisir de démarrer le débogage dans un contexte d’exécution à partir du début en fournissant le `IDebugApplication` pointeur vers l’avant `JsCreateContext` , ou il peut patienter jusqu’à ce que le débogage soit nécessaire, puis appeler `JsStartDebugging` . Le moteur Microsoft Edge `JsCreateContext` n’accepte plus un `IDebugApplication` paramètre et, par conséquent, le script est débogué uniquement après `JsStartDebugging` appelé. Lors du débogage à l’aide de Visual Studio, l’option de débogueur «script» doit être activée.  
  
 Le code JavaScript dans un contexte d’exécution peut être profilé de l’une des deux manières suivantes. La ligne de commande Visual Studio Profiler (VSPerf. exe) peut être utilisée dans Windows 8,1 et les versions ultérieures avec le commutateur/js pour générer un rapport ciblant le code JavaScript exécuté dans l’application. L’hôte peut appeler `JsStartProfiling` et fournir directement `JsStopProfiling` un rappel pour effectuer le profilage. L’hôte peut également examiner l’état du tas récupéré par le garbage collector en appelant `JsEnumerateHeap` . Le profilage dans JsRT fonctionne de la même manière que celle du moteur hérité et du moteur Microsoft Edge. Toutefois, les API de profil JsRT ( `JsStartProfiling` , `JsStopProfiling` , `JsEnumerateHeap` et `JsIsEnumeratingHeap` ) ne sont pas disponibles pour les applications Windows universelles.  
  
<a name="Windows"></a>   
## JsRT et plateforme Windows universelle  

Vous pouvez utiliser les API JsRT pour ajouter des fonctionnalités d’écriture de script à une application Windows universelle. Une application Windows universelle qui utilise les API JsRT doit cibler les API Microsoft Edge JSRT, qui à son tour cibler le moteur Chakra Edge. Pour plus d’informations, reportez-vous à la rubrique [ciblage des moteurs Microsoft Edge et hérités](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md). L’API JsRT complète est disponible pour les applications Windows universelles, à l’exception de la prise en charge de l’énumération et du profilage ( `JsStartProfiling` , `JsStopProfiling` `JsEnumerateHeap` et `JsIsEnumeratingHeap` non prise en charge).  
  
JsRT autorise également les scripts à accéder en natif aux API de la [plateforme Windows universelle (UWP)](https://msdn.microsoft.com/library/windows/apps/br211377.aspx) après avoir exposé l’espace de noms de l’API via l’API JsRT de Microsoft Edge `JsProjectWinRTNamespace` . Les applications Windows universelles ne nécessitent pas de configuration en plus des espaces de noms nécessaires pour projecter dans une application Windows classique (Win32), un mécanisme de pompage délégué initialisé par COM doit être activé `JsSetProjectionEnqueueCallback` pour activer des événements et des API asynchrones. L’exemple Win32 suivant fait appel à des API UWP asynchrones pour créer un client http et obtenir du contenu à partir d’un URI:  
  
```cpp  
typedef struct _jsCall {  
    JsProjectionCallback jsCallback;  
    JsProjectionCallbackContext jsContext;  
    HANDLE event;  
} jsCall;  
  
// Set up delegated pumping mechanism; not necessary in UWP applications.  
jsCall outstandingCall = {};  
CoInitializeEx(nullptr, COINIT_MULTITHREADED);  
JsSetProjectionEnqueueCallback([](JsProjectionCallback jsCallback,   
JsProjectionCallbackContext jsContext, void *callbackState) {  
    jsCall* call = (jsCall*)callbackState;  
    call->jsCallback = jsCallback;  
    call->jsContext = jsContext;  
    SetEvent(call->event);  
    },  
&outstandingCall);  
HANDLE event = CreateEventEx(NULL, NULL, CREATE_EVENT_MANUAL_RESET, EVENT_ALL_ACCESS);  
outstandingCall.event = event;  
  
// Project necessary namespaces.  
JsProjectWinRTNamespace(L"Windows.Foundation");  
JsProjectWinRTNamespace(L"Windows.Web");  
  
// Get content from an Uri.  
JsRunScript(L"var uri = new Windows.Foundation.Uri(\"http://somedatasource.com\"); " \  
    L"var httpClient = new Windows.Web.Http.HttpClient();" \  
    L"httpClient.getStringAsync(uri).done(function (content) { " \  
    L"    // do something with the string content " \    
    L"}, onError); " \  
    L"function onError(reason) { " \  
    L"    // error handling " \        
    L"}",   
    currentSourceContext, L"", &result);  
  
// Wait for async call to come in and then execute; not necessary in UWP applications.  
WaitForSingleObjectEx(outstandingCall.event, 10000, FALSE) == WAIT_OBJECT_0;  
outstandingCall.jsCallback(outstandingCall.jsContext);  
  
```  
  
## Voir aussi  
 [Exemple d’application JavaScript Runtime](https://go.microsoft.com/fwlink/p/?LinkID=306674&clcid=0x409)   
 [Référence (Runtime JavaScript)](../chakra-hosting/reference-javascript-runtime.md)   
 [Hébergement Runtime JavaScript](../javascript-runtime-hosting.md)  
 