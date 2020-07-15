---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 8b029202843dd006be4d9ecdadc63161bebb6b39
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878056"
---
# <span data-ttu-id="61407-104">0.8.355-interface IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="61407-104">0.8.355 - interface IWebView2WebView4</span></span> 

> [!NOTE]
> <span data-ttu-id="61407-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="61407-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="61407-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="61407-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

<span data-ttu-id="61407-107">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="61407-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="61407-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="61407-108">Summary</span></span>

 <span data-ttu-id="61407-109">Ses</span><span class="sxs-lookup"><span data-stu-id="61407-109">Members</span></span>                        | <span data-ttu-id="61407-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="61407-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61407-111">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="61407-111">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="61407-112">Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="61407-112">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="61407-113">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="61407-113">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="61407-114">Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.</span><span class="sxs-lookup"><span data-stu-id="61407-114">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="61407-115">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="61407-115">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="61407-116">Ouvre la fenêtre DevTools pour le document actif dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="61407-116">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="61407-117">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="61407-117">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="61407-118">Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="61407-118">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="61407-119">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="61407-119">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="61407-120">Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="61407-120">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="61407-121">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="61407-121">WEBVIEW2_KEY_EVENT_TYPE</span></span>](#webview2_key_event_type) | <span data-ttu-id="61407-122">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="61407-122">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="61407-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="61407-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#webview2_physical_key_status) | <span data-ttu-id="61407-124">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="61407-124">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="61407-125">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="61407-125">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="61407-126">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="61407-126">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="61407-127">Ses</span><span class="sxs-lookup"><span data-stu-id="61407-127">Members</span></span>

#### <span data-ttu-id="61407-128">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="61407-128">AddRemoteObject</span></span> 

<span data-ttu-id="61407-129">Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="61407-129">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="61407-130">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR Name, variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="61407-130">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="61407-131">Les objets hôtes sont exposés en tant que proxy d’objets distants par le biais de `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="61407-131">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="61407-132">Les proxys d’objets distants sont promet et sont résolus en objet représentant l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="61407-132">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="61407-133">La promesse est refusée si l’application n’a pas ajouté d’objet portant le nom.</span><span class="sxs-lookup"><span data-stu-id="61407-133">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="61407-134">Lorsque le code JavaScript accède à une propriété ou une méthode de l’objet, une promesse est renvoyée, qui est résolue en fonction de la valeur renvoyée par l’hôte de la propriété ou de la méthode, ou rejetée en cas d’erreur, comme il n’y a pas de propriété ou de méthode sur l’objet ou les paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="61407-134">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="61407-135">Par exemple, lorsque le code de l’application effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="61407-135">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="61407-136">Le code JavaScript de l’affichage WebView sera en mesure d’accéder à appObject comme suit, puis d’accéder aux attributs et méthodes de appObject:</span><span class="sxs-lookup"><span data-stu-id="61407-136">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="61407-137">Notez qu’en ce qui concerne les types simples, IDispatch et Array sont pris en charge, le type IUnknown, VT_DECIMAL ou VT_RECORD variant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="61407-137">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="61407-138">Les objets JavaScript distants comme les fonctions de rappel sont représentés sous la forme d’un VT_DISPATCH VARIANT avec l’objet qui implémente IDispatch.</span><span class="sxs-lookup"><span data-stu-id="61407-138">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="61407-139">La méthode de rappel JavaScript doit être appelée à l’aide de DISPID_VALUE pour le DISPID.</span><span class="sxs-lookup"><span data-stu-id="61407-139">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="61407-140">Les tableaux imbriqués sont pris en charge jusqu’à une profondeur de 3.</span><span class="sxs-lookup"><span data-stu-id="61407-140">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="61407-141">Les matrices de par types de référence ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="61407-141">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="61407-142">VT_EMPTY et VT_NULL sont mappés dans JavaScript en tant que valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="61407-142">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="61407-143">Dans JavaScript, les valeurs NULL et non définies sont mappées à VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="61407-143">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="61407-144">De plus, tous les objets distants sont exposés en tant que `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="61407-144">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="61407-145">Ici, les objets hôtes sont exposés en tant que proxy d’objets distants synchrones.</span><span class="sxs-lookup"><span data-stu-id="61407-145">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="61407-146">Celles-ci ne sont pas promesse et les appels de fonctions ou d’accès aux propriétés empêchent de manière synchrone l’exécution d’un script en attente de communication croisée pour que le code hôte s’exécute.</span><span class="sxs-lookup"><span data-stu-id="61407-146">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="61407-147">En conséquence, cela peut entraîner des problèmes de fiabilité et nous vous conseillons d’utiliser l’API asynchrone basée sur la promesse `window.chrome.webview.remoteObjects.<name>` décrite ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="61407-147">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="61407-148">Les proxys d’objets distants synchrones et les proxys d’objets distants asynchrones peuvent deux proxy sur le même objet distant.</span><span class="sxs-lookup"><span data-stu-id="61407-148">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="61407-149">Les modifications distantes apportées par un proxy seront reflétées dans tous les autres proxy de ce même objet distant, qu’il s’agisse de proxys et synchrones ou asynchrones.</span><span class="sxs-lookup"><span data-stu-id="61407-149">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="61407-150">Si JavaScript est bloqué lors d’un appel asynchrone au code natif, ce code natif ne peut pas rappeler JavaScript.</span><span class="sxs-lookup"><span data-stu-id="61407-150">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="61407-151">Les tentatives d’une telle opération échoueront avec HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="61407-151">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="61407-152">Les proxys d’objets distants sont des objets proxy JavaScript qui interceptent l’ensemble des appels de propriété Get, de jeu de propriétés et de méthode.</span><span class="sxs-lookup"><span data-stu-id="61407-152">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="61407-153">Les propriétés ou méthodes qui font partie du prototype de fonction ou d’objet sont exécutées localement.</span><span class="sxs-lookup"><span data-stu-id="61407-153">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="61407-154">De plus, toute propriété ou méthode du tableau `chrome.webview.remoteObjects.options.forceLocalProperties` sera également exécutée localement.</span><span class="sxs-lookup"><span data-stu-id="61407-154">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="61407-155">Par exemple, vous pouvez inclure des méthodes facultatives ayant une signification dans JavaScript comme `toJSON` et `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="61407-155">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="61407-156">Vous pouvez en ajouter d’autres à ce tableau selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="61407-156">You can add more to this array as required.</span></span>

<span data-ttu-id="61407-157">Il existe une méthode `chrome.webview.remoteObjects.cleanupSome` qui consiste à utiliser au mieux le nettoyage de la mémoire proxy d’objets distants.</span><span class="sxs-lookup"><span data-stu-id="61407-157">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="61407-158">Les proxys d’objets distants présentent également les méthodes suivantes qui s’exécutent en local:</span><span class="sxs-lookup"><span data-stu-id="61407-158">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="61407-159">applyRemote, getRemote, setRemote: effectue un appel de méthode, Get de propriété ou jeu de propriétés sur l’objet distant.</span><span class="sxs-lookup"><span data-stu-id="61407-159">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="61407-160">Vous pouvez utiliser ces éléments pour forcer explicitement une méthode ou une propriété à s’exécuter à distance en cas de conflit entre une méthode locale ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="61407-160">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="61407-161">Par exemple, `proxy.toString()` exécute la méthode ToString locale sur l’objet proxy.</span><span class="sxs-lookup"><span data-stu-id="61407-161">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="61407-162">Mais `proxy.applyRemote('toString')` s’exécute `toString` plutôt sur l’objet proxy distant.</span><span class="sxs-lookup"><span data-stu-id="61407-162">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="61407-163">getLocal, setLocal: exécuter la propriété Get ou Property Set localement.</span><span class="sxs-lookup"><span data-stu-id="61407-163">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="61407-164">Vous pouvez utiliser ces méthodes pour forcer l’affichage ou la définition d’une propriété sur le proxy d’objet distant lui-même plutôt que sur l’objet distant qu’elle représente.</span><span class="sxs-lookup"><span data-stu-id="61407-164">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="61407-165">Par exemple, obtiendrez `proxy.unknownProperty` la propriété nommée `unknownProperty` de l’objet proxy distant.</span><span class="sxs-lookup"><span data-stu-id="61407-165">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="61407-166">Toutefois `proxy.getLocal('unknownProperty')` , vous obtiendrez la valeur de la propriété `unknownProperty` sur l’objet proxy lui-même.</span><span class="sxs-lookup"><span data-stu-id="61407-166">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="61407-167">synchronisation: les proxys d’objets distants asynchrones présentent une méthode de synchronisation qui renvoie une promesse de proxy d’objet distant synchrone pour le même objet distant.</span><span class="sxs-lookup"><span data-stu-id="61407-167">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="61407-168">Par exemple, `chrome.webview.remoteObjects.sample.methodCall()` retourne un proxy asynchrone d’objet distant.</span><span class="sxs-lookup"><span data-stu-id="61407-168">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="61407-169">Vous pouvez utiliser la `sync` méthode pour obtenir un proxy d’objet distant synchrone à la place:</span><span class="sxs-lookup"><span data-stu-id="61407-169">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="61407-170">Async: les proxys d’objets distants synchrones présentent une méthode Async qui bloque et retourne un proxy d’objet distant asynchrone pour le même objet distant.</span><span class="sxs-lookup"><span data-stu-id="61407-170">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="61407-171">Par exemple, `chrome.webview.remoteObjects.sync.sample.methodCall()` retourne un proxy d’objet distant synchrone.</span><span class="sxs-lookup"><span data-stu-id="61407-171">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="61407-172">Appel de la `async` méthode sur ce bloc, puis retour d’un proxy d’objet distant asynchrone pour le même objet distant:</span><span class="sxs-lookup"><span data-stu-id="61407-172">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="61407-173">ensuite: les proxys d’objets distants asynchrones ont une méthode Then.</span><span class="sxs-lookup"><span data-stu-id="61407-173">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="61407-174">Cela leur permet d’être await.</span><span class="sxs-lookup"><span data-stu-id="61407-174">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="61407-175">renverra une promesse qui est résolue en une représentation de l’objet distant.</span><span class="sxs-lookup"><span data-stu-id="61407-175">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="61407-176">Si le proxy représente un littéral JavaScript, une copie de celui-ci est renvoyée localement.</span><span class="sxs-lookup"><span data-stu-id="61407-176">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="61407-177">Si le proxy représente une fonction, un proxy non-await est retourné.</span><span class="sxs-lookup"><span data-stu-id="61407-177">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="61407-178">Si le proxy représente un objet JavaScript avec une combinaison de propriétés littérales et de propriétés de fonctions, une copie de l’objet est renvoyée avec des propriétés en tant que proxy d’objets distants.</span><span class="sxs-lookup"><span data-stu-id="61407-178">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="61407-179">Tous les autres appels de propriété et de méthode (autres que les méthodes de proxy d’objet distant, la liste forceLocalProperties et les propriétés des prototypes de fonction et d’objet) s’exécutent à distance.</span><span class="sxs-lookup"><span data-stu-id="61407-179">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="61407-180">Les proxys d’objets distants asynchrones retournent une promesse qui représente la complétion asynchrone d’appeler la méthode à distance ou d’obtenir la propriété.</span><span class="sxs-lookup"><span data-stu-id="61407-180">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="61407-181">La promesse se résout une fois les opérations distantes terminées et la promesse de la valeur de l’opération.</span><span class="sxs-lookup"><span data-stu-id="61407-181">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="61407-182">Les proxys d’objets distants synchrones s’exécutent de la même façon, mais bloquent l’exécution JavaScript et attendez la fin de l’opération à distance.</span><span class="sxs-lookup"><span data-stu-id="61407-182">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="61407-183">La définition d’une propriété sur un proxy asynchrone d’objet distant fonctionne légèrement différemment.</span><span class="sxs-lookup"><span data-stu-id="61407-183">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="61407-184">Le jeu renvoie immédiatement et la valeur de retour est la valeur qui sera définie.</span><span class="sxs-lookup"><span data-stu-id="61407-184">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="61407-185">Il s’agit d’une condition requise de l’objet proxy JavaScript.</span><span class="sxs-lookup"><span data-stu-id="61407-185">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="61407-186">Si vous avez besoin d’attendre que le jeu de propriétés soit terminé, utilisez la méthode setRemote qui renvoie une promesse comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="61407-186">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="61407-187">La propriété du jeu de propriétés d’objet synchrone se bloque de manière synchrone tant que la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="61407-187">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="61407-188">Par exemple, supposons que vous disposiez d’un objet COM avec l’interface suivante.</span><span class="sxs-lookup"><span data-stu-id="61407-188">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="61407-189">Nous pouvons ajouter une instance de cette interface dans notre JavaScript avec `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="61407-189">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="61407-190">Dans le cas présent, vous nommerez ce message `sample` :</span><span class="sxs-lookup"><span data-stu-id="61407-190">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="61407-191">Ensuite, dans le document HTML, vous pouvez utiliser cet objet COM via `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="61407-191">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="61407-192">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="61407-192">RemoveRemoteObject</span></span> 

<span data-ttu-id="61407-193">Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.</span><span class="sxs-lookup"><span data-stu-id="61407-193">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="61407-194">public HRESULT [RemoveRemoteObject](#removeremoteobject)(nom LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="61407-194">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="61407-195">Même si de nouvelles tentatives d’accès seront refusées, si l’objet est déjà obtenu par le code JavaScript du WebView, le code JavaScript continuera à avoir accès à cet objet.</span><span class="sxs-lookup"><span data-stu-id="61407-195">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="61407-196">Il n’est pas nécessaire d’appeler cette méthode pour un nom qui a déjà été supprimé ou n’ayant jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="61407-196">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="61407-197">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="61407-197">OpenDevToolsWindow</span></span> 

<span data-ttu-id="61407-198">Ouvre la fenêtre DevTools pour le document actif dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="61407-198">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="61407-199">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="61407-199">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="61407-200">Ne peut pas être appelé lorsque la fenêtre DevTools est déjà ouverte</span><span class="sxs-lookup"><span data-stu-id="61407-200">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="61407-201">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="61407-201">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="61407-202">Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="61407-202">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="61407-203">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)par le biais du[mot de passe](IWebView2AcceleratorKeyPressedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="61407-203">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="61407-204">AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé.</span><span class="sxs-lookup"><span data-stu-id="61407-204">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="61407-205">Un raccourci est considéré comme un accélérateur s’il s’agit de l’un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="61407-205">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="61407-206">Ctrl ou Alt est en cours de conservation ou</span><span class="sxs-lookup"><span data-stu-id="61407-206">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="61407-207">la touche appuyée ne correspond pas à un caractère.</span><span class="sxs-lookup"><span data-stu-id="61407-207">the pressed key does not map to a character.</span></span> <span data-ttu-id="61407-208">Quelques touches spécifiques ne sont jamais considérées comme des accélérateurs, comme Shift.</span><span class="sxs-lookup"><span data-stu-id="61407-208">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="61407-209">La touche Échap est toujours considérée comme un accélérateur.</span><span class="sxs-lookup"><span data-stu-id="61407-209">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="61407-210">Les événements de touches répétées déclenchés suite à la fermeture de la clé entraînent également le déclenchement de cet événement.</span><span class="sxs-lookup"><span data-stu-id="61407-210">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="61407-211">Vous pouvez les filtrer en vérifiant les arguments d’événements «KeyEventLParam ou PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="61407-211">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="61407-212">En mode fenêtre, ce gestionnaire d’événements est appelé de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="61407-212">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="61407-213">Tant que vous n’avez pas appelé handle () sur les arguments d’événement ou que le gestionnaire d’événements renvoie, le processus de navigateur sera bloqué et les appels COM entre processus entrants échoueront avec RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="61407-213">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="61407-214">Toutes les méthodes de l’API WebView2 fonctionneront toutefois.</span><span class="sxs-lookup"><span data-stu-id="61407-214">All WebView2 API methods will work, however.</span></span>

<span data-ttu-id="61407-215">En mode sans fenêtre, le gestionnaire d’événements est appelé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="61407-215">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="61407-216">L’entrée supplémentaire n’atteint pas le navigateur tant que le gestionnaire d’événements n’a pas renvoyé ou que le gestionnaire d’événements n’est pas appelé, mais que le processus du navigateur proprement dit ne sera pas bloqué et que les appels COM sortants fonctionneront normalement.</span><span class="sxs-lookup"><span data-stu-id="61407-216">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="61407-217">Il est recommandé d’appeler handle (vrai) dès que vous en savez que vous voulez gérer la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="61407-217">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_webView->add_AcceleratorKeyPressed(
        Callback<IWebView2AcceleratorKeyPressedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2AcceleratorKeyPressedEventArgs* args)
                -> HRESULT {
                WEBVIEW2_KEY_EVENT_TYPE type;
                CHECK_FAILURE(args->get_KeyEventType(&type));
                // We only care about key down events.
                if (type == WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN ||
                    type == WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->Handle(TRUE));

                        // Filter out autorepeated keys.
                        WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="61407-218">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="61407-218">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="61407-219">Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="61407-219">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="61407-220">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="61407-220">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="61407-221">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="61407-221">WEBVIEW2_KEY_EVENT_TYPE</span></span> 

<span data-ttu-id="61407-222">Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="61407-222">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="61407-223">énumération [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span><span class="sxs-lookup"><span data-stu-id="61407-223">enum [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span></span>

 <span data-ttu-id="61407-224">Doubl</span><span class="sxs-lookup"><span data-stu-id="61407-224">Values</span></span>                         | <span data-ttu-id="61407-225">Descriptions</span><span class="sxs-lookup"><span data-stu-id="61407-225">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="61407-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="61407-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span></span>            | <span data-ttu-id="61407-227">Correspond à WM_KEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="61407-227">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="61407-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="61407-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span></span>            | <span data-ttu-id="61407-229">Correspond à WM_KEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="61407-229">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="61407-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="61407-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="61407-231">Correspond à WM_SYSKEYDOWN de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="61407-231">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="61407-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="61407-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="61407-233">Correspond à WM_SYSKEYUP de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="61407-233">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="61407-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="61407-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="61407-235">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="61407-235">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="61407-236">[WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) typedef</span><span class="sxs-lookup"><span data-stu-id="61407-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span></span>

<span data-ttu-id="61407-237">Pour plus d’informations, consultez la documentation de WM_KEYDOWN[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="61407-237">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

