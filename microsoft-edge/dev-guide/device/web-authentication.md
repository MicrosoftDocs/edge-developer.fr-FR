---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Découvrez comment l’API d’authentification Web peut être utilisée pour permettre aux applications Web d’utiliser la biométrie Windows Hello pour l’authentification des utilisateurs.
title: Guide de développement-authentification Web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: c49d181633ae1b2b35aa0f88287841d28e806f44
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564697"
---
# Authentification Web et Windows Hello

L’API d’authentification Web (anciennement de la *2,0* ) dans Microsoft Edge permet aux applications Web d’utiliser la biométrie [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) pour l’authentification des utilisateurs, afin que vous et vos utilisateurs puissiez éviter les problèmes liés à la gestion des mots de passe, y compris la recherche de mot de passe, les tentatives de hameçonnage et de journalisation. L’implémentation actuelle de Microsoft Edge (*MS-* préfixé) est basée sur un brouillon antérieur de la spécification d’authentification Web et est susceptible de changer dans le futur. **Cette rubrique vous montre comment tester l’authentification de Windows Hello avec Microsoft Edge, tout en préillustrant votre code par rapport aux mises à jour du navigateur.**

L’API d’authentification Web est une norme émergeante, mise en place par l' [Alliance](https://fidoalliance.org/) de la côte à côte, qui permet d’offrir une méthode d’authentification Web compatible avec Windows Hello et d’autres appareils biométriques dans les navigateurs. La spécification d’authentification Web définit deux scénarios d’authentification: moins le mot de passe et deux facteurs. Dans le cas contraire du mot de passe, l’utilisateur n’a pas besoin de se connecter à la page Web à l’aide d’un nom d’utilisateur ou d’un mot de passe, il peut se connecter uniquement à l’aide de Windows Hello. Dans le cas de deux facteurs, l’utilisateur se connecte généralement en utilisant un nom d’utilisateur et un mot de passe, mais Windows Hello est utilisé comme second contrôle pour renforcer l’authentification globale.

À l’aide de l’authentification Web combinée avec Windows Hello, le serveur envoie une demande de texte brut au navigateur. Lorsque Microsoft Edge est en mesure de vérifier l’utilisateur par le biais de Windows Hello, le système signe le défi avec une clé privée précédemment déployée pour cet utilisateur et l’envoie au serveur. Si le serveur peut valider la signature à l’aide de la clé publique qu’il a pour cet utilisateur et vérifier que la demande est correcte, il peut authentifier l’utilisateur en toute sécurité. Dans le cas d’un [chiffrement asymétrique](https://en.wikipedia.org/wiki/Public-key_cryptography) tel que celui-ci, la clé publique n’a pas d’importance et la clé privée n’est jamais partagée. Par ailleurs, la clé privée ne peut jamais être déplacée vers des systèmes modernes dotés d’un matériel de module de plateforme sécurisée.

Il existe deux étapes de base pour l’utilisation de l’API d’authentification Web:

**1. Enregistrez votre utilisateur avec `makeCredential`**

**2. authentifier votre utilisateur avec `getAssertion`**

Les éléments suivants vous guident dans le processus à l’aide du [Polyfill. js. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)recommandé. Le [code complet](https://github.com/adrianba/fido-snippets/) est disponible pour cette démonstration du serveur et du client. [C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [php](https://github.com/adrianba/fido-snippets/tree/master/php)et [nœud. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) versions côté serveur sont disponibles.

## Enregistrez votre utilisateur

En tant que *fournisseur d’identité*, vous devez commencer par créer une authentification Web pour votre utilisateur à l’aide de la fenêtre. webauthn. méthode **makeCredential** . Avant d’enregistrer les informations d’identification de l’utilisateur sur votre serveur, vous devrez confirmer l’identité de l’utilisateur. Pour cela, il suffit de lui envoyer un e-mail de confirmation ou de lui demander d’utiliser sa méthode de connexion traditionnelle.

La méthode makeCredential accepte les paramètres suivants:
 - **informations de compte d’utilisateur**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **paramètres de chiffrement**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

La promesse qui en résulte renvoie un objet qui représente les informations d’identification que vous avez ensuite renvoyées au serveur pour valider les authentifications ultérieures:

**Client**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var email = '<%=user.email%>';
    var name = '<%=user.name%>';

    webauthn.makeCredential(userAccountInformation, cryptoParams)
        .then(function (creds) {
            document.getElementById('form-id').value = creds.credential.id;
            document.getElementById('form-pk').value = JSON.stringify(creds.publicKey);
            document.getElementById('form-email').value = email;
            document.getElementById('form-name').value = name;
            document.getElementById('theform').submit();
        }).catch(function (err) {
            // No acceptable authenticator or user refused consent. Handle appropriately.
            alert(err);
        });
</script>
```

Lorsque vous utilisez la méthode makeCredential, Microsoft Edge vous demande d’abord à Windows Hello d’utiliser l’identification par visage ou empreinte digitale pour vérifier que l’utilisateur est le même que celui connecté au compte Windows. Une fois cette étape terminée, Microsoft Passport génère une paire de clés publique/privée et stocke la clé privée dans le module de plateforme sécurisée (TPM), le matériel du processeur de chiffrement dédié utilisé pour stocker les informations d’identification. Si l’utilisateur ne dispose pas d’un appareil de plateforme sécurisée, ces clés seront stockées dans le logiciel. Ces informations d’identification sont créées par origine, par compte Windows et ne seront pas itinérantes, car elles sont liées à l’appareil. Cela signifie que vous devez veiller à ce que l’utilisateur s’inscrit à utiliser Windows Hello pour chaque appareil qu’il utilise.

## Authentifier votre utilisateur

Une fois les informations d’identification créées sur le client, la prochaine fois que l’utilisateur tente de se connecter au site, vous pouvez l’utiliser pour vous connecter à l’aide de Windows Hello au lieu d’un mot de passe avec un appel à Window. webauthn. **getAssertion**.

La méthode getAssertion accepte la *demande* en tant que paramètre requis uniquement. Le défi correspond à la quantité générée de manière aléatoire que le serveur envoie à un client pour signer avec la clé privée de l’utilisateur. Exemple:

**Serveur**

```
var crypto = require('crypto');

Strategy.prototype.generateChallenge = function() {
    return this.generateVerifiableString(crypto.randomBytes(32));
};

Strategy.prototype.generateVerifiableString = function(data) {
    // Create cipher using secret
    var d = new Buffer(data);
    var c = crypto.createCipher('aes192',new Buffer(this._secret));

    // Encrypt data
    c.update(d);

    // Hash results of encrypting data
    var hash = crypto.createHash('sha256');
    hash.update(c.final());

    // Combine original data with hash
    return d.toString('hex') + string_separator + hash.digest('hex');
};
```

Une fois l’appel getAssertion exécuté, Microsoft Edge affiche l’invite Windows Hello, qui vérifie l’identité de l’utilisateur à l’aide d’une biométrie. Après vérification de l’utilisateur, le défi sera signé dans le TPM et la promesse sera renvoyée avec un objet d’assertion contenant la signature et d’autres métadonnées que vous pouvez envoyer au serveur:

**Client**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var challenge = '<%=challenge%>';

    webauthn.getAssertion(challenge)
    .then(function(assertion) {
      document.getElementById("form-id").value = assertion.credential.id;
      document.getElementById("form-type").value = assertion.credential.type;
      document.getElementById("form-data").value = assertion.clientData;
      document.getElementById("form-sig").value = assertion.signature;
      document.getElementById("form-authnr").value = assertion.authenticatorData;
      document.getElementById("form-challenge").value = challenge;
      document.getElementById("theform").submit();
    })
    .catch(function(err) {
      if(err && err.name) {
        document.getElementById("form-err").value = err.name;
      } else {
        document.getElementById("form-err").value = "unknown";
      }
      document.getElementById("theform").submit();
    });

</script>
```

Dès lors que vous recevez l’assertion sur le serveur, vous devrez valider la signature pour authentifier l’utilisateur. Par exemple (dans node. JS):

**Serveur**

```
var jwkToPem = require('jwk-to-pem')
var crypto = require('crypto');

var fidoAuthenticator = {
     validateSignature: function (publicKey, clientData, authnrData, signature, challenge) {
         // Make sure the challenge in the client data
         // matches the expected challenge
         var c = new Buffer(clientData, 'base64');
         var cc = JSON.parse(c.toString().replace(/\0/g,''));
         if(cc.challenge != challenge) return false;

         // Hash data with sha256
         const hash = crypto.createHash('sha256');
         hash.update(c);
         var h = hash.digest();

         // Verify signature is correct for authnrData + hash
         var verify = crypto.createVerify('RSA-SHA256');
         verify.update(new Buffer(authnrData,'base64'));
         verify.update(h);
         return verify.verify(jwkToPem(JSON.parse(publicKey)), signature, 'base64');
     }
};   
```

## Différences entre Microsoft Edge et la spécification

> [!NOTE]
> Lorsque vous évaluez l’API d’authentification Web avec Windows Hello dans Microsoft Edge, nous vous conseillons d’utiliser le polyremplissage de webauthn. js, comme illustré ci-dessus, pour éviter de tenir compte des différences répertoriées ici. Nous allons mettre à jour ce polyfill pour chaque version majeure publiée de la spécification.


L’implémentation actuelle de Microsoft Edge est basée sur un brouillon antérieur de la spécification d’authentification Web et est susceptible de changer dans les versions ultérieures, et à mesure que la spec évolue. Les différences actuelles sont les suivantes:

- Les API Microsoft Edge sont MS-préfixé.
- Microsoft Edge ne prend pas encore en charge les informations d’identification externes telles que les clés USB ou les appareils Bluetooth. L’API actuelle est limitée aux informations d’identification incorporées stockées dans le module de plateforme sécurisée.
- Le compte d’utilisateur Windows actuellement connecté doit être configuré de manière à prendre en charge au moins un code confidentiel, et de préférence au visage ou à l’empreinte digitale biométriques. Cela permet de s’assurer que Windows peut authentifier l’accès au module de plateforme sécurisée.
- L’implémentation de Microsoft Edge ne prend pas encore en charge l’interface de sélecteur de compte.
- Un deuxième paramètre de *filtre* spécifiant l’ID d’information d’identification est actuellement requis pour les appels à msCredentials. [getAssertion](https://msdn.microsoft.com/library/mt697640). Par exemple, vous devez stocker vos informations d’identification d’informations d’identification dans le stockage local sur le client, soit dans indexDB, soit dans localStorage lorsque vous effectuez vos informations d’identification. Si un utilisateur supprime son historique de navigation, y compris le stockage local, il devra le réenregistrer pour utiliser Windows Hello lors de sa prochaine connexion.
- Microsoft Edge ne prend pas en charge toutes les options du brouillon de spécification d’authentification Web actuel, telles que les extensions ou les délais d’expiration.

À ce stade, les différences relatives aux spécificités de Microsoft Edge sont indiquées dans les définitions de Spec d’authentification Web suivantes:

### Spécifications du W3C

```
partial interface Window {
    readonly attribute WebAuthentication webauthn; // msCredentials
};

interface WebAuthentication { // MSCredentials
    Promise <ScopedCredentialInfo> makeCredential (
        Account                                 accountInformation,
        sequence <ScopedCredentialParameters>   cryptoParameters,
        DOMString                               attestationChallenge, // Optional in Microsoft Edge
        optional unsigned long                  credentialTimeoutSeconds, // Not yet supported
        optional sequence <Credential>          blacklist, // Not yet supported
        optional WebAuthnExtensions             credentialExtensions // Not yet supported
    );

    Promise <WebAuthnAssertion> getAssertion (
        DOMString                        assertionChallenge,
        optional unsigned long           assertionTimeoutSeconds, // Not yet supported
        optional sequence <Credential>   whitelist, // Not yet supported
        optional WebAuthnExtensions      assertionExtensions // Not yet supported
    );
};

interface ScopedCredentialInfo { // MSAssertion
    readonly attribute Credential           credential;
    readonly attribute any                  publicKey;
    readonly attribute AttestationStatement attestation;
};

dictionary Account { // MSAccountInfo
    required DOMString rpDisplayName;
    required DOMString displayName;
    DOMString          name; // Not yet supported
    DOMString          id; // Not yet supported
    DOMString          imageUri; // Not yet supported
};

dictionary ScopedCredentialParameters { // MSCredentialParameters
    required CredentialType        type;
    required AlgorithmIdentifier   algorithm;
};

enum CredentialType { // MSCredentialType
    "ScopedCred" // Must be "FIDO_2_0" in Microsoft Edge
};

interface Credential { // MSCredentialSpec
    readonly attribute CredentialType type;
    readonly attribute DOMString      id;
};

dictionary WebAuthnExtensions { // Not supported
};
```



## Informations de référence sur les API

[MSCredentials](https://msdn.microsoft.com/library/mt697639)

[makeCredential](https://msdn.microsoft.com/library/mt697641)

[getAssertion](https://msdn.microsoft.com/library/mt697640)

## Démos

[Exemples de code client et serveur](https://github.com/adrianba/fido-snippets/)

[Polyremplissage de webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[Démo de Windows Hello test](https://testdrive-fido.azurewebsites.net/)

## Spécifier

[Authentification Web: API Web permettant d’accéder aux informations d’identification étendues 1](http://w3c.github.io/webauthn/)  
