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
# <span data-ttu-id="6fbac-104">Authentification Web et Windows Hello</span><span class="sxs-lookup"><span data-stu-id="6fbac-104">Web authentication and Windows Hello</span></span>

<span data-ttu-id="6fbac-105">L’API d’authentification Web (anciennement de la *2,0* ) dans Microsoft Edge permet aux applications Web d’utiliser la biométrie [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) pour l’authentification des utilisateurs, afin que vous et vos utilisateurs puissiez éviter les problèmes liés à la gestion des mots de passe, y compris la recherche de mot de passe, les tentatives de hameçonnage et de journalisation.</span><span class="sxs-lookup"><span data-stu-id="6fbac-105">The Web Authentication (formerly *FIDO 2.0* ) API in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometrics for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and keylogging attacks.</span></span> <span data-ttu-id="6fbac-106">L’implémentation actuelle de Microsoft Edge (*MS-* préfixé) est basée sur un brouillon antérieur de la spécification d’authentification Web et est susceptible de changer dans le futur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-106">The current Microsoft Edge (*ms-* prefixed) implementation is based on an earlier draft of the Web Authentication specification and is likely to change in the future.</span></span> **<span data-ttu-id="6fbac-107">Cette rubrique vous montre comment tester l’authentification de Windows Hello avec Microsoft Edge, tout en préillustrant votre code par rapport aux mises à jour du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-107">This topic will show you how to try out Windows Hello authentication with Microsoft Edge while also future-proofing your code against browser updates.</span></span>**

<span data-ttu-id="6fbac-108">L’API d’authentification Web est une norme émergeante, mise en place par l' [Alliance](https://fidoalliance.org/) de la côte à côte, qui permet d’offrir une méthode d’authentification Web compatible avec Windows Hello et d’autres appareils biométriques dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="6fbac-108">The Web Authentication API is an emerging standard put forth by the [FIDO Alliance](https://fidoalliance.org/) with the aim of providing an interoperable way of doing web authentication using Windows Hello and other biometric devices across browsers.</span></span> <span data-ttu-id="6fbac-109">La spécification d’authentification Web définit deux scénarios d’authentification: moins le mot de passe et deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="6fbac-109">The Web Authentication specification defines two authentication scenarios: password-less and two factor.</span></span> <span data-ttu-id="6fbac-110">Dans le cas contraire du mot de passe, l’utilisateur n’a pas besoin de se connecter à la page Web à l’aide d’un nom d’utilisateur ou d’un mot de passe, il peut se connecter uniquement à l’aide de Windows Hello.</span><span class="sxs-lookup"><span data-stu-id="6fbac-110">In the password-less case, the user does not need to log into the web page using a user name or password – they can login solely using Windows Hello.</span></span> <span data-ttu-id="6fbac-111">Dans le cas de deux facteurs, l’utilisateur se connecte généralement en utilisant un nom d’utilisateur et un mot de passe, mais Windows Hello est utilisé comme second contrôle pour renforcer l’authentification globale.</span><span class="sxs-lookup"><span data-stu-id="6fbac-111">In the two factor case, the user logs in normally using a username and password, but Windows Hello is used as a second factor check to make the overall authentication stronger.</span></span>

<span data-ttu-id="6fbac-112">À l’aide de l’authentification Web combinée avec Windows Hello, le serveur envoie une demande de texte brut au navigateur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-112">Using Web Authentication combined with Windows Hello, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="6fbac-113">Lorsque Microsoft Edge est en mesure de vérifier l’utilisateur par le biais de Windows Hello, le système signe le défi avec une clé privée précédemment déployée pour cet utilisateur et l’envoie au serveur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-113">Once Microsoft Edge is able to verify the user through Windows Hello, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="6fbac-114">Si le serveur peut valider la signature à l’aide de la clé publique qu’il a pour cet utilisateur et vérifier que la demande est correcte, il peut authentifier l’utilisateur en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6fbac-114">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="6fbac-115">Dans le cas d’un [chiffrement asymétrique](https://en.wikipedia.org/wiki/Public-key_cryptography) tel que celui-ci, la clé publique n’a pas d’importance et la clé privée n’est jamais partagée.</span><span class="sxs-lookup"><span data-stu-id="6fbac-115">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="6fbac-116">Par ailleurs, la clé privée ne peut jamais être déplacée vers des systèmes modernes dotés d’un matériel de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6fbac-116">Furthermore, the private key can never be moved from modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="6fbac-117">Il existe deux étapes de base pour l’utilisation de l’API d’authentification Web:</span><span class="sxs-lookup"><span data-stu-id="6fbac-117">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="6fbac-118">1. Enregistrez votre utilisateur avec</span><span class="sxs-lookup"><span data-stu-id="6fbac-118">1. Register your user with</span></span> `makeCredential`**

**<span data-ttu-id="6fbac-119">2. authentifier votre utilisateur avec</span><span class="sxs-lookup"><span data-stu-id="6fbac-119">2. Authenticate your user with</span></span> `getAssertion`**

<span data-ttu-id="6fbac-120">Les éléments suivants vous guident dans le processus à l’aide du [Polyfill. js. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)recommandé.</span><span class="sxs-lookup"><span data-stu-id="6fbac-120">The following will walk you through this flow using the recommended [Webauthn.js polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span></span> <span data-ttu-id="6fbac-121">Le [code complet](https://github.com/adrianba/fido-snippets/) est disponible pour cette démonstration du serveur et du client.</span><span class="sxs-lookup"><span data-stu-id="6fbac-121">The [complete code](https://github.com/adrianba/fido-snippets/) is available for this server and client side demo.</span></span> <span data-ttu-id="6fbac-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [php](https://github.com/adrianba/fido-snippets/tree/master/php)et [nœud. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) versions côté serveur sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="6fbac-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php), and [Node.JS](https://github.com/adrianba/fido-snippets/tree/master/nodejs) server side versions are available.</span></span>

## <span data-ttu-id="6fbac-123">Enregistrez votre utilisateur</span><span class="sxs-lookup"><span data-stu-id="6fbac-123">Register your user</span></span>

<span data-ttu-id="6fbac-124">En tant que *fournisseur d’identité*, vous devez commencer par créer une authentification Web pour votre utilisateur à l’aide de la fenêtre. webauthn. méthode **makeCredential** .</span><span class="sxs-lookup"><span data-stu-id="6fbac-124">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the window.webauthn.**makeCredential** method.</span></span> <span data-ttu-id="6fbac-125">Avant d’enregistrer les informations d’identification de l’utilisateur sur votre serveur, vous devrez confirmer l’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-125">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="6fbac-126">Pour cela, il suffit de lui envoyer un e-mail de confirmation ou de lui demander d’utiliser sa méthode de connexion traditionnelle.</span><span class="sxs-lookup"><span data-stu-id="6fbac-126">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>

<span data-ttu-id="6fbac-127">La méthode makeCredential accepte les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="6fbac-127">The makeCredential method takes the following parameters:</span></span>
 - **<span data-ttu-id="6fbac-128">informations de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6fbac-128">user account information</span></span>**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **<span data-ttu-id="6fbac-129">paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="6fbac-129">crypto parameters</span></span>**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

<span data-ttu-id="6fbac-130">La promesse qui en résulte renvoie un objet qui représente les informations d’identification que vous avez ensuite renvoyées au serveur pour valider les authentifications ultérieures:</span><span class="sxs-lookup"><span data-stu-id="6fbac-130">The resulting promise returns an object representing the credential that you then send back to the server for validating future authentications:</span></span>

**<span data-ttu-id="6fbac-131">Client</span><span class="sxs-lookup"><span data-stu-id="6fbac-131">Client</span></span>**

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

<span data-ttu-id="6fbac-132">Lorsque vous utilisez la méthode makeCredential, Microsoft Edge vous demande d’abord à Windows Hello d’utiliser l’identification par visage ou empreinte digitale pour vérifier que l’utilisateur est le même que celui connecté au compte Windows.</span><span class="sxs-lookup"><span data-stu-id="6fbac-132">When you use the makeCredential method, Microsoft Edge will first ask Windows Hello to use face or fingerprint identification to verify that the user is the same user as the one logged into the Windows account.</span></span> <span data-ttu-id="6fbac-133">Une fois cette étape terminée, Microsoft Passport génère une paire de clés publique/privée et stocke la clé privée dans le module de plateforme sécurisée (TPM), le matériel du processeur de chiffrement dédié utilisé pour stocker les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="6fbac-133">Once this step is completed, Microsoft Passport will generate a public/private key pair and store the private key in the Trusted Platform Module (TPM), the dedicated crypto processor hardware used to store credentials.</span></span> <span data-ttu-id="6fbac-134">Si l’utilisateur ne dispose pas d’un appareil de plateforme sécurisée, ces clés seront stockées dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="6fbac-134">If the user doesn’t have a TPM enabled device, these keys will be stored in software.</span></span> <span data-ttu-id="6fbac-135">Ces informations d’identification sont créées par origine, par compte Windows et ne seront pas itinérantes, car elles sont liées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6fbac-135">These credentials are created per origin, per Windows account, and will not be roamed because they are tied to the device.</span></span> <span data-ttu-id="6fbac-136">Cela signifie que vous devez veiller à ce que l’utilisateur s’inscrit à utiliser Windows Hello pour chaque appareil qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="6fbac-136">This means that you’ll need to make sure the user registers to use Windows Hello for every device they use.</span></span>

## <span data-ttu-id="6fbac-137">Authentifier votre utilisateur</span><span class="sxs-lookup"><span data-stu-id="6fbac-137">Authenticate your user</span></span>

<span data-ttu-id="6fbac-138">Une fois les informations d’identification créées sur le client, la prochaine fois que l’utilisateur tente de se connecter au site, vous pouvez l’utiliser pour vous connecter à l’aide de Windows Hello au lieu d’un mot de passe avec un appel à Window. webauthn. **getAssertion**.</span><span class="sxs-lookup"><span data-stu-id="6fbac-138">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using Windows Hello instead of a password with a call to window.webauthn.**getAssertion**.</span></span>

<span data-ttu-id="6fbac-139">La méthode getAssertion accepte la *demande* en tant que paramètre requis uniquement.</span><span class="sxs-lookup"><span data-stu-id="6fbac-139">The getAssertion method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="6fbac-140">Le défi correspond à la quantité générée de manière aléatoire que le serveur envoie à un client pour signer avec la clé privée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-140">The challenge is the randomly generated quantity that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="6fbac-141">Exemple:</span><span class="sxs-lookup"><span data-stu-id="6fbac-141">For example:</span></span>

**<span data-ttu-id="6fbac-142">Serveur</span><span class="sxs-lookup"><span data-stu-id="6fbac-142">Server</span></span>**

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

<span data-ttu-id="6fbac-143">Une fois l’appel getAssertion exécuté, Microsoft Edge affiche l’invite Windows Hello, qui vérifie l’identité de l’utilisateur à l’aide d’une biométrie.</span><span class="sxs-lookup"><span data-stu-id="6fbac-143">Once the getAssertion call is made, Microsoft Edge will show the Windows Hello prompt, which will verify the identity of the user using biometrics.</span></span> <span data-ttu-id="6fbac-144">Après vérification de l’utilisateur, le défi sera signé dans le TPM et la promesse sera renvoyée avec un objet d’assertion contenant la signature et d’autres métadonnées que vous pouvez envoyer au serveur:</span><span class="sxs-lookup"><span data-stu-id="6fbac-144">After the user is verified, the challenge will be signed within the TPM and the promise will return with an assertion object that contains the signature and other metadata for you to send to the server:</span></span>

**<span data-ttu-id="6fbac-145">Client</span><span class="sxs-lookup"><span data-stu-id="6fbac-145">Client</span></span>**

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

<span data-ttu-id="6fbac-146">Dès lors que vous recevez l’assertion sur le serveur, vous devrez valider la signature pour authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6fbac-146">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="6fbac-147">Par exemple (dans node. JS):</span><span class="sxs-lookup"><span data-stu-id="6fbac-147">For example (in Node.JS):</span></span>

**<span data-ttu-id="6fbac-148">Serveur</span><span class="sxs-lookup"><span data-stu-id="6fbac-148">Server</span></span>**

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

## <span data-ttu-id="6fbac-149">Différences entre Microsoft Edge et la spécification</span><span class="sxs-lookup"><span data-stu-id="6fbac-149">Differences between Microsoft Edge and the spec</span></span>

> [!NOTE]
> <span data-ttu-id="6fbac-150">Lorsque vous évaluez l’API d’authentification Web avec Windows Hello dans Microsoft Edge, nous vous conseillons d’utiliser le polyremplissage de webauthn. js, comme illustré ci-dessus, pour éviter de tenir compte des différences répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="6fbac-150">When trying out the Web Authentication API with Windows Hello in Microsoft Edge, we recommend using the Webauthn.js polyfill as shown above to avoid having to account for the discrepancies listed here.</span></span> <span data-ttu-id="6fbac-151">Nous allons mettre à jour ce polyfill pour chaque version majeure publiée de la spécification.</span><span class="sxs-lookup"><span data-stu-id="6fbac-151">We'll update this polyfill for every major published version of the specification.</span></span>


<span data-ttu-id="6fbac-152">L’implémentation actuelle de Microsoft Edge est basée sur un brouillon antérieur de la spécification d’authentification Web et est susceptible de changer dans les versions ultérieures, et à mesure que la spec évolue.</span><span class="sxs-lookup"><span data-stu-id="6fbac-152">The current Microsoft Edge implementation is based on an earlier draft of the Web Authentication specification and is likely to change in future builds and as the spec evolves.</span></span> <span data-ttu-id="6fbac-153">Les différences actuelles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="6fbac-153">The current differences include:</span></span>

- <span data-ttu-id="6fbac-154">Les API Microsoft Edge sont MS-préfixé.</span><span class="sxs-lookup"><span data-stu-id="6fbac-154">Microsoft Edge APIs are MS- prefixed.</span></span>
- <span data-ttu-id="6fbac-155">Microsoft Edge ne prend pas encore en charge les informations d’identification externes telles que les clés USB ou les appareils Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="6fbac-155">Microsoft Edge does not yet support external credentials like USB keys or Bluetooth devices.</span></span> <span data-ttu-id="6fbac-156">L’API actuelle est limitée aux informations d’identification incorporées stockées dans le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6fbac-156">The current API is limited to embedded credentials stored in the TPM.</span></span>
- <span data-ttu-id="6fbac-157">Le compte d’utilisateur Windows actuellement connecté doit être configuré de manière à prendre en charge au moins un code confidentiel, et de préférence au visage ou à l’empreinte digitale biométriques.</span><span class="sxs-lookup"><span data-stu-id="6fbac-157">The currently logged in Windows user account must be configured to support at least a PIN, and preferably face or fingerprint biometrics.</span></span> <span data-ttu-id="6fbac-158">Cela permet de s’assurer que Windows peut authentifier l’accès au module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6fbac-158">This is to ensure that Windows can authenticate the access to the TPM.</span></span>
- <span data-ttu-id="6fbac-159">L’implémentation de Microsoft Edge ne prend pas encore en charge l’interface de sélecteur de compte.</span><span class="sxs-lookup"><span data-stu-id="6fbac-159">The Microsoft Edge implementation does not yet support the account picker experience.</span></span>
- <span data-ttu-id="6fbac-160">Un deuxième paramètre de *filtre* spécifiant l’ID d’information d’identification est actuellement requis pour les appels à msCredentials. [getAssertion](https://msdn.microsoft.com/library/mt697640).</span><span class="sxs-lookup"><span data-stu-id="6fbac-160">A second *filters* parameter specifying the credential id is currently required for calls to msCredentials.[getAssertion](https://msdn.microsoft.com/library/mt697640).</span></span> <span data-ttu-id="6fbac-161">Par exemple, vous devez stocker vos informations d’identification d’informations d’identification dans le stockage local sur le client, soit dans indexDB, soit dans localStorage lorsque vous effectuez vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="6fbac-161">As such, you’ll need to store your credential ID information in local storage on the client, either in indexDB or localStorage when making your credential.</span></span> <span data-ttu-id="6fbac-162">Si un utilisateur supprime son historique de navigation, y compris le stockage local, il devra le réenregistrer pour utiliser Windows Hello lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="6fbac-162">If a user deletes their browsing history, including local storage, they will need to re-register to use Windows Hello the next time they log in.</span></span>
- <span data-ttu-id="6fbac-163">Microsoft Edge ne prend pas en charge toutes les options du brouillon de spécification d’authentification Web actuel, telles que les extensions ou les délais d’expiration.</span><span class="sxs-lookup"><span data-stu-id="6fbac-163">Microsoft Edge does not support all of the options in the current Web Authentication specification draft, such as extensions or timeouts.</span></span>

<span data-ttu-id="6fbac-164">À ce stade, les différences relatives aux spécificités de Microsoft Edge sont indiquées dans les définitions de Spec d’authentification Web suivantes:</span><span class="sxs-lookup"><span data-stu-id="6fbac-164">On that last point, the specific Microsoft Edge differences are noted in the following Web Authentication spec definitions:</span></span>

### <span data-ttu-id="6fbac-165">Spécifications du W3C</span><span class="sxs-lookup"><span data-stu-id="6fbac-165">W3C spec</span></span>

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



## <span data-ttu-id="6fbac-166">Informations de référence sur les API</span><span class="sxs-lookup"><span data-stu-id="6fbac-166">API Reference</span></span>

[<span data-ttu-id="6fbac-167">MSCredentials</span><span class="sxs-lookup"><span data-stu-id="6fbac-167">MSCredentials</span></span>](https://msdn.microsoft.com/library/mt697639)

[<span data-ttu-id="6fbac-168">makeCredential</span><span class="sxs-lookup"><span data-stu-id="6fbac-168">makeCredential</span></span>](https://msdn.microsoft.com/library/mt697641)

[<span data-ttu-id="6fbac-169">getAssertion</span><span class="sxs-lookup"><span data-stu-id="6fbac-169">getAssertion</span></span>](https://msdn.microsoft.com/library/mt697640)

## <span data-ttu-id="6fbac-170">Démos</span><span class="sxs-lookup"><span data-stu-id="6fbac-170">Demos</span></span>

[<span data-ttu-id="6fbac-171">Exemples de code client et serveur</span><span class="sxs-lookup"><span data-stu-id="6fbac-171">Client and server code samples</span></span>](https://github.com/adrianba/fido-snippets/)

[<span data-ttu-id="6fbac-172">Polyremplissage de webauthn. js</span><span class="sxs-lookup"><span data-stu-id="6fbac-172">Webauthn.js polyfill</span></span>](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[<span data-ttu-id="6fbac-173">Démo de Windows Hello test</span><span class="sxs-lookup"><span data-stu-id="6fbac-173">Windows Hello Test Drive demo</span></span>](https://testdrive-fido.azurewebsites.net/)

## <span data-ttu-id="6fbac-174">Spécifier</span><span class="sxs-lookup"><span data-stu-id="6fbac-174">Specification</span></span>

[<span data-ttu-id="6fbac-175">Authentification Web: API Web permettant d’accéder aux informations d’identification étendues 1</span><span class="sxs-lookup"><span data-stu-id="6fbac-175">Web Authentication: A Web API for accessing scoped credentials 1</span></span>](http://w3c.github.io/webauthn/)  
