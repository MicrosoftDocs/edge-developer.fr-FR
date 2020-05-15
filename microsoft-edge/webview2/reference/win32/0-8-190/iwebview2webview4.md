---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 6ebed9e61bf7eda60e6e16b7a417306baa5d07bf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653259"
---
# interface IWebView2WebView4 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

Fonctionnalités supplémentaires implémentées par l’objet WebView principal.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[AddRemoteObject](#addremoteobject) | Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.
[RemoveRemoteObject](#removeremoteobject) | Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.
[OpenDevToolsWindow](#opendevtoolswindow) | Ouvre la fenêtre DevTools pour le document actif dans le WebView.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.
[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) | Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.
[WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) | Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.

Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md). Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .

## Ses

#### AddRemoteObject 

Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.

> public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR Name, variant * Object)

Les objets hôtes sont exposés en tant que proxy d’objets distants par le biais de `window.chrome.webview.remoteObjects.<name>` . Les proxys d’objets distants sont promet et sont résolus en objet représentant l’objet hôte. La promesse est refusée si l’application n’a pas ajouté d’objet portant le nom. Lorsque le code JavaScript accède à une propriété ou une méthode de l’objet, une promesse est renvoyée, qui est résolue en fonction de la valeur renvoyée par l’hôte de la propriété ou de la méthode, ou rejetée en cas d’erreur, comme il n’y a pas de propriété ou de méthode sur l’objet ou les paramètres ne sont pas valides. Par exemple, lorsque le code de l’application effectue les opérations suivantes: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 Le code JavaScript de l’affichage WebView sera en mesure d’accéder à appObject comme suit, puis d’accéder aux attributs et méthodes de appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Notez qu’en ce qui concerne les types simples, IDispatch et Array sont pris en charge, le type IUnknown, VT_DECIMAL ou VT_RECORD variant n’est pas pris en charge. Les objets JavaScript distants comme les fonctions de rappel sont représentés sous la forme d’un VT_DISPATCH VARIANT avec l’objet qui implémente IDispatch. La méthode de rappel JavaScript doit être appelée à l’aide de DISPID_VALUE pour le DISPID. Les tableaux imbriqués sont pris en charge jusqu’à une profondeur de 3. Les matrices de par types de référence ne sont pas prises en charge. VT_EMPTY et VT_NULL sont mappés dans JavaScript en tant que valeurs NULL. Dans JavaScript, les valeurs NULL et non définies sont mappées à VT_EMPTY.

De plus, tous les objets distants sont exposés en tant que `window.chrome.webview.remoteObjects.sync.<name>` . Ici, les objets hôtes sont exposés en tant que proxy d’objets distants synchrones. Celles-ci ne sont pas promesse et les appels de fonctions ou d’accès aux propriétés empêchent de manière synchrone l’exécution d’un script en attente de communication croisée pour que le code hôte s’exécute. En conséquence, cela peut entraîner des problèmes de fiabilité et nous vous conseillons d’utiliser l’API asynchrone basée sur la promesse `window.chrome.webview.remoteObjects.<name>` décrite ci-dessus.

Les proxys d’objets distants synchrones et les proxys d’objets distants asynchrones peuvent deux proxy sur le même objet distant. Les modifications distantes apportées par un proxy seront reflétées dans tous les autres proxy de ce même objet distant, qu’il s’agisse de proxys et synchrones ou asynchrones.

Si JavaScript est bloqué lors d’un appel asynchrone au code natif, ce code natif ne peut pas rappeler JavaScript. Les tentatives d’une telle opération échoueront avec HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Les proxys d’objets distants sont des objets proxy JavaScript qui interceptent l’ensemble des appels de propriété Get, de jeu de propriétés et de méthode. Les propriétés ou méthodes qui font partie du prototype de fonction ou d’objet sont exécutées localement. De plus, toute propriété ou méthode du tableau `chrome.webview.remoteObjects.options.forceLocalProperties` sera également exécutée localement. Par exemple, vous pouvez inclure des méthodes facultatives ayant une signification dans JavaScript comme `toJSON` et `Symbol.toPrimitive` . Vous pouvez en ajouter d’autres à ce tableau selon vos besoins.

Il existe une méthode `chrome.webview.remoteObjects.cleanupSome` qui consiste à utiliser au mieux le nettoyage de la mémoire proxy d’objets distants.

Les proxys d’objets distants présentent également les méthodes suivantes qui s’exécutent en local:

* applyRemote, getRemote, setRemote: effectue un appel de méthode, Get de propriété ou jeu de propriétés sur l’objet distant. Vous pouvez utiliser ces éléments pour forcer explicitement une méthode ou une propriété à s’exécuter à distance en cas de conflit entre une méthode locale ou une propriété. Par exemple, `proxy.toString()` exécute la méthode ToString locale sur l’objet proxy. Mais `proxy.applyRemote('toString')` s’exécute `toString` plutôt sur l’objet proxy distant.

* getLocal, setLocal: exécuter la propriété Get ou Property Set localement. Vous pouvez utiliser ces méthodes pour forcer l’affichage ou la définition d’une propriété sur le proxy d’objet distant lui-même plutôt que sur l’objet distant qu’elle représente. Par exemple, obtiendrez `proxy.unknownProperty` la propriété nommée `unknownProperty` de l’objet proxy distant. Toutefois `proxy.getLocal('unknownProperty')` , vous obtiendrez la valeur de la propriété `unknownProperty` sur l’objet proxy lui-même.

* synchronisation: les proxys d’objets distants asynchrones présentent une méthode de synchronisation qui renvoie une promesse de proxy d’objet distant synchrone pour le même objet distant. Par exemple, `chrome.webview.remoteObjects.sample.methodCall()` retourne un proxy asynchrone d’objet distant. Vous pouvez utiliser la `sync` méthode pour obtenir un proxy d’objet distant synchrone à la place: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: les proxys d’objets distants synchrones présentent une méthode Async qui bloque et retourne un proxy d’objet distant asynchrone pour le même objet distant. Par exemple, `chrome.webview.remoteObjects.sync.sample.methodCall()` retourne un proxy d’objet distant synchrone. Appel de la `async` méthode sur ce bloc, puis retour d’un proxy d’objet distant asynchrone pour le même objet distant: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* ensuite: les proxys d’objets distants asynchrones ont une méthode Then. Cela leur permet d’être await. `then` renverra une promesse qui est résolue en une représentation de l’objet distant. Si le proxy représente un littéral JavaScript, une copie de celui-ci est renvoyée localement. Si le proxy représente une fonction, un proxy non-await est retourné. Si le proxy représente un objet JavaScript avec une combinaison de propriétés littérales et de propriétés de fonctions, une copie de l’objet est renvoyée avec des propriétés en tant que proxy d’objets distants.

Tous les autres appels de propriété et de méthode (autres que les méthodes de proxy d’objet distant, la liste forceLocalProperties et les propriétés des prototypes de fonction et d’objet) s’exécutent à distance. Les proxys d’objets distants asynchrones retournent une promesse qui représente la complétion asynchrone d’appeler la méthode à distance ou d’obtenir la propriété. La promesse se résout une fois les opérations distantes terminées et la promesse de la valeur de l’opération. Les proxys d’objets distants synchrones s’exécutent de la même façon, mais bloquent l’exécution JavaScript et attendez la fin de l’opération à distance.

La définition d’une propriété sur un proxy asynchrone d’objet distant fonctionne légèrement différemment. Le jeu renvoie immédiatement et la valeur de retour est la valeur qui sera définie. Il s’agit d’une condition requise de l’objet proxy JavaScript. Si vous avez besoin d’attendre que le jeu de propriétés soit terminé, utilisez la méthode setRemote qui renvoie une promesse comme décrit ci-dessus. La propriété du jeu de propriétés d’objet synchrone se bloque de manière synchrone tant que la propriété est définie.

Par exemple, supposons que vous disposiez d’un objet COM avec l’interface suivante.

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

 Nous pouvons ajouter une instance de cette interface dans notre JavaScript avec `AddRemoteObject` . Dans le cas présent, vous nommerez ce message `sample` :

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

 Ensuite, dans le document HTML, vous pouvez utiliser cet objet COM via `chrome.webview.remoteObjects.sample` :

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

#### RemoveRemoteObject 

Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.

> public HRESULT [RemoveRemoteObject](#removeremoteobject)(nom LPCWSTR)

Même si de nouvelles tentatives d’accès seront refusées, si l’objet est déjà obtenu par le code JavaScript du WebView, le code JavaScript continuera à avoir accès à cet objet. Il n’est pas nécessaire d’appeler cette méthode pour un nom qui a déjà été supprimé ou n’ayant jamais été ajouté.

#### OpenDevToolsWindow 

Ouvre la fenêtre DevTools pour le document actif dans le WebView.

> public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Ne peut pas être appelé lorsque la fenêtre DevTools est déjà ouverte

#### add_AcceleratorKeyPressed 

Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.

> [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)par le biais du[mot de passe](IWebView2AcceleratorKeyPressedEventHandler.md)

AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé. Un raccourci est considéré comme un accélérateur s’il s’agit de l’un des éléments suivants:

1. Ctrl ou Alt est en cours de conservation ou

1. la touche appuyée ne correspond pas à un caractère. Quelques touches spécifiques ne sont jamais considérées comme des accélérateurs, comme Shift. La touche Échap est toujours considérée comme un accélérateur.

Les événements de touches répétées déclenchés suite à la fermeture de la clé entraînent également le déclenchement de cet événement. Vous pouvez les filtrer en vérifiant les arguments d’événements «KeyEventLParam ou PhysicalKeyStatus.

En mode fenêtre, ce gestionnaire d’événements est appelé de manière synchrone. Tant que vous n’avez pas appelé handle () sur les arguments d’événement ou que le gestionnaire d’événements renvoie, le processus de navigateur sera bloqué et les appels COM entre processus entrants échoueront avec RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Toutes les méthodes de l’API WebView2 fonctionneront toutefois.

En mode sans fenêtre, le gestionnaire d’événements est appelé de manière asynchrone. L’entrée supplémentaire n’atteint pas le navigateur tant que le gestionnaire d’événements n’a pas renvoyé ou que le gestionnaire d’événements n’est pas appelé, mais que le processus du navigateur proprement dit ne sera pas bloqué et que les appels COM sortants fonctionneront normalement.

Il est recommandé d’appeler handle (vrai) dès que vous en savez que vous voulez gérer la touche accélérateur.

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

#### remove_AcceleratorKeyPressed 

Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.

> [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)par le biais du mot-clé public HRESULT

#### WEBVIEW2_KEY_EVENT_TYPE 

Type d’événement de touche qui déclenchait un événement AcceleratorKeyPressed.

> énumération [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN            | Correspond à WM_KEYDOWN de messages de fenêtre.
WEBVIEW2_KEY_EVENT_TYPE_KEY_UP            | Correspond à WM_KEYUP de messages de fenêtre.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN            | Correspond à WM_SYSKEYDOWN de messages de fenêtre.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP            | Correspond à WM_SYSKEYUP de messages de fenêtre.

#### WEBVIEW2_PHYSICAL_KEY_STATUS 

Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.

> [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) typedef

Pour plus d’informations, consultez la documentation de WM_KEYDOWN[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

