---
description: Les erreurs JavaScript sont signalées par les outils de développement et déboguer chacune d’elles dans la console
title: Suivi des erreurs à l’aide de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483410"
---
# <a name="debug-errors-reported-in-console"></a>Erreurs de débogage signalées dans la console  

La première expérience que vous avez avec la **console est** probablement une erreur dans un script.  Pour l’essayer, accédez à [l’erreur JavaScript signalée dans l’outil console.][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]  

Si vous ouvrez DevTools dans le navigateur, un bouton en haut à droite affiche une erreur pour la page web.  
Choisissez le bouton pour vous aider à vous rendre sur la **console** et vous donner plus d’informations sur l’erreur.  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools fournit des informations détaillées sur l’erreur dans la console" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools fournit des informations détaillées sur l’erreur dans la **console**  
:::image-end:::  

À partir des informations, vous pouvez collecter que l’erreur se trouve sur la ligne 16 du `error.html` fichier.  Si vous choisissez le lien à droite de la console, il vous permet d’utiliser l’outil Sources et met en évidence la ligne de `error.html:16` code avec **** l’erreur. ****  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="L’outil Sources met en évidence la ligne de code à l’origine de l’erreur" lightbox="../media/console-debug-displays-in-sources.msft.png":::
   **L’outil Sources** met en évidence la ligne de code à l’origine de l’erreur  
:::image-end:::  

Le script tente d’obtenir le premier élément du document et `h2` de peindre une bordure rouge autour de celui-ci.  Mais aucun `h2` élément n’existe, le script échoue.  

## <a name="find-and-debug-network-issues"></a>Rechercher et déboguer des problèmes réseau  

Les autres erreurs que la **console** signale sont des erreurs réseau.  Pour l’afficher en action, accédez à l’erreur [réseau signalée dans la console.][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="La console affiche un réseau et une erreur JavaScript" lightbox="../media/console-debug-network-error.msft.png":::
   **La console** affiche un réseau et une erreur JavaScript  
:::image-end:::  

Le tableau `loading` s’affiche, mais rien ne change sur la page web, car les données ne sont jamais récupérées.  Dans la **console,** les deux erreurs suivantes se sont produites.  

*   Erreur réseau qui commence par la `GET` méthode HTTP suivie d’un URI.  
*   Une `Uncaught (in promise) TypeError: data.forEach is not a function` erreur.  
    
Si vous choisissez le `network-error.html:40` lien dans la **console,** DevTools vous permet d’utiliser l’outil **Sources.**  La ligne de code problématique est mise en surbrillant et suivie d’un `error` bouton \( `x` \).  Pour afficher le `Failed to load resource: the server responded with a status of 404 ()` message d’erreur, choisissez le bouton **d’erreur** `x` \( \).  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Choisissez le lien vers la page web et le code dans lequel l’erreur se produit ouvre l’outil Sources" lightbox="../media/console-debug-network-error-code-line.msft.png":::
         Choisissez le lien vers la page web et le code dans lequel l’erreur se produit ouvre **l’outil Sources**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Pour rechercher l’erreur dans JavaScript, utilisez l’outil Sources" lightbox="../media/console-debug-network-error-sources.msft.png":::
         Pour rechercher l’erreur dans JavaScript, utilisez **l’outil Sources**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Dans l’exemple, l’erreur vous informe que l’URL demandée est in trouvée.  Ensuite, terminez les actions suivantes pour ouvrir **l’outil** Réseau.  

1.  Ouvrez la **console.**  
1.  Choisissez l’URI associé à l’erreur.  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="La console affiche un code d’état HTTP de l’erreur après qu’une ressource n’est pas chargée" lightbox="../media/console-debug-network-error-url.msft.png":::
   **La console** affiche un code d’état HTTP de l’erreur après qu’une ressource n’est pas chargée  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="L’outil Réseau affiche plus d’informations sur la demande qui a échoué" lightbox="../media/console-debug-network-error-network.msft.png":::
           **L’outil** Réseau affiche plus d’informations sur la demande qui a échoué  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="L’inspection des en-têtes dans l’outil Réseau peut donner plus d’informations" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           L’inspection des en-têtes dans **l’outil** Réseau peut donner plus d’informations  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

Quel était le problème ?  Deux barres obliques \( `//` \) se produisent dans l’URI demandé après le `repos` mot.  Ouvrez **l’outil Sources** et inspectez la ligne 26.  Une barre oblique finale \( \) se produit à la fin de `/` l’URI de base.  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="L’outil Sources affiche la ligne de code avec l’erreur" lightbox="../media/console-debug-network-error-code-error.msft.png":::
   **L’outil Sources** affiche la ligne de code avec l’erreur  
:::image-end:::  

Pour passer en revue aucune erreur dans la **console,** accédez à [Erreur réseau fixe signalée dans la console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="L’exemple sans erreur charge les informations de GitHub et les affiche" lightbox="../media/console-debug-network-error-fixed.msft.png":::
   L’exemple sans erreur charge les informations de GitHub et les affiche  
:::image-end:::  

Veillez à fournir des techniques de codage conviviales pour éviter les expériences utilisateur précédentes.  Assurez-vous également que votre code capture les erreurs et affiche chacune d’elles dans la **console.**  Accédez au [rapport d’erreurs réseau dans la console et l’interface][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] utilisateur et examinez les éléments suivants.  

*   Fournissez une interface utilisateur à l’utilisateur pour qu’un problème se soit passé.  
*   Dans la **console,** fournissez des informations utiles sur l’erreur réseau à partir de votre code.  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Exemple qui capture et signale les erreurs" lightbox="../media/console-debug-network-error-report.msft.png":::
   Exemple qui capture et signale les erreurs  
:::image-end:::  

L’extrait de code suivant capture et signale les erreurs à l’aide de la `handleErrors` méthode, en particulier la `throw Error` ligne.  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a>Créer des erreurs et des suivis dans la console

Outre l’exemple de la section précédente, vous pouvez également créer différentes erreurs et problèmes de `throw Error` suivi dans la **console.**  
Pour afficher deux messages d’erreur créés dans la **console,** accédez à Création de rapports d’erreurs et [d’assertions dans la console.][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Messages d’erreur créés à partir de la console" lightbox="../media/console-debug-error-assert.msft.png":::
   Messages d’erreur créés à partir de la **console**  
:::image-end:::  

L’extrait de code suivant a été utilisé dans l’exemple précédent.  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

Vous avez trois fonctions qui se demandent l’une l’autre successivement.  

*   `first()`  
*   `second()`  
*   `third()`  
    
Chacun envoie un `name` argument à l’autre.  Dans la fonction, vous vérifiez si l’argument existe et, si ce n’est pas le cas, vous enregistrez une erreur qui `third()` `name` n’est pas définie.  Si `name` elle est définie, vous utilisez la méthode pour vérifier si `assert()` `name` l’argument a une longueur de moins de huit lettres.  Vous demandez la `first()` fonction trois fois, avec les paramètres suivants.  

*   Aucun argument qui déclenche la `console.error()` méthode dans la `third()` fonction.  
*   Le terme en tant que paramètre de la fonction ne provoque pas d’erreur, car l’argument existe et est `Console` plus court que huit `first()` `name` lettres.  
*   L’expression en tant que paramètre pour fonctionner entraîne le signalement d’une erreur par la méthode, car le paramètre `Microsoft Edge Canary` est plus de huit `first()` `console.assert()` lettres.  
    
Utilisez la méthode `console.assert()` pour créer des rapports d’erreurs conditionnelles.  Les deux exemples suivants ont le même résultat, mais l’un d’entre vous a besoin d’une `if{}` instruction supplémentaire.  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> Les deuxième et troisième lignes du code effectuent le même test.  Étant donné que l’assertion doit enregistrer un résultat négatif, vous devez la tester `x < 40` dans la cas et pour `if` `x >= 40` l’assertion.  

Si vous ne savez pas quelle fonction demande une autre fonction, utilisez la méthode pour suivre les fonctions qui sont `console.trace()` demandées pour obtenir la fonction actuelle.  Pour afficher le suivi dans la **console,** accédez à [Création de suivis dans la console.][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

Le résultat est un suivi à afficher qui est nommé, puis dans le `here()` `there()` deuxième exemple `everywhere()` qu’il est nommé `everywhere()` .  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Suivi créé à partir de la console" lightbox="../media/console-debug-trace.msft.png":::
   Suivi créé à partir de la **console**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Erreur JavaScript signalée dans l’outil console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Création de rapports d’erreurs et d’assertions dans console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Erreur réseau signalée dans console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "Erreur réseau corrigée signalée dans console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Rapport d’erreurs réseau dans la console et l’interface | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Création de suivis dans la console | GitHub"  
