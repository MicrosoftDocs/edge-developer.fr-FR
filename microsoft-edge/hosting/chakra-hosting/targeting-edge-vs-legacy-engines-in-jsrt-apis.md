---
description: 'Découvrez comment cibler les différents moteurs JavaScript Windows 10. '
title: Ciblage du moteur Microsoft Edge et des moteurs hérités dans les API JsRT
ms.date: 06/18/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 99a3143dd5f995332524a99e5c6c5019b955fea8
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752226"
---
# Ciblage du moteur Microsoft Edge et des moteurs hérités dans les API JsRT  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Windows 10 prend en charge deux moteurs JavaScript différents:  

*   L’ancien moteur Chakra (également appelé *moteur hérité* ou jscript9.dll ci-dessous) qui est fourni avec et prend en charge Internet Explorer 11. Ce moteur est figé en temps et reste fondamentalement modifié de Win 8.1/IE11 version.  
*   Le nouveau moteur Chakra (également appelé *moteur Edge* ou chakra.dll ci-dessous) qui est fourni avec et prend en charge le nouveau navigateur dans Windows 10, Microsoft Edge. Ce moteur sera mis à jour en permanence et sera pris en charge par le moteur [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) «vivre». Dans le cas d’un moteur Microsoft Edge, il implique que le moteur Microsoft Edge ne transmettra aucune forme de fonctionnalité de script de contrôle de version à accepter.  

 Lors de la création d’une application à l’aide de l’API d’hébergement Runtime JavaScript (JsRT), vous pouvez choisir de cibler le moteur hérité ou le moteur Microsoft Edge.  

*   Si vous devez insister sur la compatibilité descendante de vos applications existantes, ciblez le moteur hérité.  
*   Si vous voulez que votre application soit transmise à l’avenir et prenne en charge de nouvelles fonctionnalités JavaScript au fur et à mesure de leur commercialisation (par exemple, ECMAScript 6), ciblez le moteur Microsoft Edge.  

Cette rubrique inclut des détails qui décrivent comment cibler les différents moteurs.  

## Cibler votre version préférée  

Lors de la création d’une application, vous pouvez sélectionner la version de JsRT qui prend en charge le moteur Microsoft Edge ou le moteur hérité. Vous pouvez choisir la version JsRT en fonction des recommandations ci-dessus. Pour tenir compte de ces distinctions, les modifications suivantes ont été apportées aux éléments `JsCreateRuntime` `JsCreateContext` et `JsStartDebugging` .  

Pour `JsCreateRuntime` :  

*   Lorsque le moteur hérité est ciblé, la `JsRuntimeVersionEdge` valeur d’énumération est déconseillée et un message vous suggère d’utiliser la valeur à la `JsRuntimeVersionInternetExplorer11` place.  
*   Lors du ciblage du moteur Microsoft Edge, le paramètre version est omis de la `JsCreateRuntime` fonction.  
    
    ```cpp
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);
    ```  
    
 Pour `JsCreateContext` et `JsStartDebugging` :  

*   Lors du ciblage du moteur hérité, l' `IDebugApplication` interface est utilisée pour fournir vos propres méthodes de débogage à distance. À des fins de débogage, `JsCreateContext` et les `JsStartDebugging` fonctions prennent `IDebugApplication` en tant que paramètre.  
*   Lorsque le moteur Microsoft Edge est ciblé, l' `IDebugApplication` interface est déconseillée. Le moteur Chakra prend en charge la fonctionnalité de débogage native et de script avec le débogueur Visual Studio sans nécessiter l’implémentation de l' `IDebugApplication` utilisateur. L’interface n’est plus un paramètre pour `JsCreateContext` and `JsStartDebugging` en conséquence.  

Les signatures des API précédentes du moteur hérité sont les suivantes:  

```cpp
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);

JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);

JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);
```  

Les signatures des API précédentes du moteur Microsoft Edge sont les suivantes:  

```cpp
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);

JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);

JsErrorCode JsStartDebugging();
```  

## Compiler pour votre version préférée à l’aide de Visual C++  

Lors de l’utilisation de Visual C++, importez l’API JsRT en incluant l’en-tête JsRT. h et assurez-vous que JsRT. lib est inclus dans la liste des fichiers en entrée de l’éditeur de liens:  

```cpp
#include <jsrt.h>
```  

![Ajout de jsrt. lib en tant que fichier d’entrée de l’éditeur de liens](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  

Si vous souhaitez cibler les fichiers binaires du moteur Microsoft Edge, vous devez définir la macro `USE_EDGEMODE_JSRT` avant d’inclure jsrt. h et au lieu de lier jsrt. lib, vous devez créer un lien vers chakrart. lib:  

```cpp
#define USE_EDGEMODE_JSRT
#include <jsrt.h>
```  

![Ajout de chakrart. lib en tant que fichier d’entrée de l’éditeur de liens](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  

Si vous commencez à utiliser une nouvelle application, vous êtes maintenant prêt à commencer à écrire du code à l’aide de l’API JsRT.  

## Compiler pour votre version préférée à l’aide de .NET  

Si vous utilisez .NET et P/Invoke, vous devez modifier vos déclarations d’API JsRT [DllImport] pour importer chakra.dll au lieu de jscript9.dll. Par ailleurs, vous pouvez modifier la définition de `JsCreateRuntime` pour supprimer le `JsRuntimeVersion` paramètre et la définition de `JsCreateContext` et `JsStartDebugging` pour supprimer le `IDebugApplication` paramètre.  

Pour le moteur hérité, utilisez le code suivant.  

```csharp
[DllImport("jscript9.dll")]
public static extern JsErrorCode JsCreateRuntime(
    JsRuntimeAttributes attributes,
    JsRuntimeVersion version,
    JsThreadServiceCallback callback,
    out JsRuntimeSafeHandle runtime
);

[DllImport("jscript9.dll")]
public static extern JsErrorCode JsCreateContext(
    JsRuntimeSafeHandle runtime,
    IDebugApplication debugApplication,
    out JsContextRef newContext
);   

[DllImport("jscript9.dll")]
public static extern JsErrorCode JsStartDebugging(
    IDebugApplication debugApplication,
);
```  

Pour le moteur Microsoft Edge, utilisez le code suivant.  

```csharp
[DllImport("chakra.dll")]
public static extern JsErrorCode JsCreateRuntime(
    JsRuntimeAttributes attributes,
    JsThreadServiceCallback callback,
    out JsRuntimeSafeHandle runtime
);  

[DllImport("chakra.dll")]
public static extern JsErrorCode JsCreateContext(
    JsRuntimeSafeHandle runtime,
    out JsContextRef newContext
);

[DllImport("chakra.dll")]
public static extern JsErrorCode JsStartDebugging();
```  

> [!CAUTION]
> Si vous marshalez manuellement le pointeur de fonction (par exemple, via LoadLibrary/GetProcAddress), il est important que vous ne mélangez pas les déclarations de la méthode ou que vous ne Réequilibrez pas la pile, ce qui se traduit par un comportement inattendable, par exemple, le blocage de votre application. Le même problème se produit si vous effectuez une opération de recherche et remplacement globale d’instances de jscript9.dll dans votre code d’importation, car vous manquez le `version` paramètre interrompu.  

## Résumé  

Dans Windows 10, les API d’hébergement du runtime JavaScript sont divisées en deux. Ces API prennent désormais en charge un moteur Microsoft Edge, dont les fonctionnalités de langue seront alignées avec le moteur Microsoft Edge «vivant» dans Microsoft Edge. Vous pouvez tirer parti de ces fonctionnalités à partir de vos applications de bureau ou du Windows Store afin de créer des méthodes passionnantes pour étendre votre application et exploiter les compétences Web modernes de votre base de code existante. Toutefois, étant donné qu’il existe de subtils différences entre les versions précédentes, vous devez tenir compte des points suivants lorsque vous ciblez le moteur Edge ou hérité.  

*   Votre application ne peut prendre en charge qu’une seule version de JsRT par processus.  
    
    Par exemple, vous ne pouvez pas créer d’exécutable du moteur Microsoft Edge, puis le runtime du moteur hérité et attendre qu’ils s’exécutent correctement dans le même processus. Ceci n’est pas pris en charge et peut entraîner un comportement non documenté, par exemple l’impossibilité de charger la deuxième DLL.  
    
*   Dans le cadre du ciblage du moteur Microsoft Edge, votre application peut acquérir de nouvelles fonctionnalités de manière inattendue lorsque la plateforme sous-jacente est mise à jour automatiquement.  
    
    Par exemple, le mode Internet Explorer 11 de l’ancien Runtime prend en charge les déclarations de variables de portée bloc, par exemple `let` et `const` . Si le comportement du contrôle de version automatique du moteur Microsoft Edge a été le même que celui de la norme auparavant, le code qui fonctionnait dans le mode Internet Explorer 10, qui ne disposait pas de règles de blocs-notes, a pu démarrer une erreur lors de la mise à niveau automatique de la plateforme. Cela doit être une considération lors du choix du modèle d’exécution à utiliser. Même si vous pensez que vous devez cibler le moteur Microsoft Edge, dans la mesure du possible, vous devez utiliser une structure de code JavaScript qui peut devenir non valide à l’avenir.  
    
*   JsRT pour le Windows Store prend uniquement en charge le moteur Microsoft Edge (chakra.dll). Les applications qui essaient de lier une API JsRT dans jscript9.dll ne pourront pas être certifiées.  
*   Il est essentiel de ne pas confondre la déclaration de la déclaration de `JsCreateRuntime` , `JsCreateContext` et `JsStartDebugging` entre les jscript9.dll et les chakra.dll, car cela entraînera une interéquilibrité de la pile.  
    
    Lorsque vous utilisez C et C++, vous recevez une erreur de l’éditeur de liens si vous essayez d’utiliser la déclaration incorrecte, tant que vous n’avez pas besoin d’appeler, `LoadLibrary` puis `GetProcAddress` . Il est possible que les développeurs .NET ne trouvent pas ce problème facilement et vérifient donc votre code lors de l’utilisation de cette fonctionnalité.  
    
## Voir également  

*   [Hébergement du runtime JavaScript](../javascript-runtime-hosting.md)
 