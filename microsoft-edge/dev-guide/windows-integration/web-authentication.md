---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Découvrez comment l’API d’authentification Web peut permettre aux applications Web d’utiliser Windows Hello et FIDO2 pour l’authentification des utilisateurs.
title: Guide de développement-authentification Web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: cb561ae4147a24489138263a83dd37bd6f599074
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565042"
---
# <span data-ttu-id="c8c2a-104">Authentification Web et Windows Hello</span><span class="sxs-lookup"><span data-stu-id="c8c2a-104">Web Authentication and Windows Hello</span></span>

<span data-ttu-id="c8c2a-105">L' [API d’authentification Web](https://w3c.github.io/webauthn) dans Microsoft Edge permet aux applications Web d’utiliser [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) et des [appareils FIDO2 externes](https://fidoalliance.org/fido2) pour l’authentification des utilisateurs, de sorte que vous et vos utilisateurs puissiez éviter les problèmes liés à la gestion des mots de passe (par exemple, tentatives de mot de passe, hameçonnage et journalisation de clé).</span><span class="sxs-lookup"><span data-stu-id="c8c2a-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span> <span data-ttu-id="c8c2a-106">La mise en œuvre de Microsoft Edge actuelle est basée sur la recommandation de candidat à la spécification d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span> **<span data-ttu-id="c8c2a-107">Cette rubrique vous montre comment tester l’authentification Windows Hello et FIDO2 avec Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>**

<span data-ttu-id="c8c2a-108">À l’aide de l’authentification Web, le serveur envoie une demande de texte brut au navigateur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="c8c2a-109">Lorsque Microsoft Edge est en mesure de vérifier l’utilisateur par le biais de Windows Hello ou d’un appareil FIDO2 externe, le système signe le défi avec une clé privée précédemment déployée pour cet utilisateur et l’envoie au serveur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="c8c2a-110">Si le serveur peut valider la signature à l’aide de la clé publique qu’il a pour cet utilisateur et vérifier que la demande est correcte, il peut authentifier l’utilisateur en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="c8c2a-111">Dans le cas d’un [chiffrement asymétrique](https://en.wikipedia.org/wiki/Public-key_cryptography) tel que celui-ci, la clé publique n’a pas d’importance et la clé privée n’est jamais partagée.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="c8c2a-112">Par ailleurs, la clé privée ne peut jamais être déplacée depuis des éléments sécurisés ou des systèmes modernes dotés d’un matériel de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="c8c2a-113">Il existe deux étapes de base pour l’utilisation de l’API d’authentification Web:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-113">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="c8c2a-114">1. Enregistrez votre utilisateur avec</span><span class="sxs-lookup"><span data-stu-id="c8c2a-114">1. Register your user with</span></span> `create`**

**<span data-ttu-id="c8c2a-115">2. authentifier votre utilisateur avec</span><span class="sxs-lookup"><span data-stu-id="c8c2a-115">2. Authenticate your user with</span></span> `get`**

<span data-ttu-id="c8c2a-116">Le Guide de développement suivant vous guidera tout au long du processus à l’aide de l' [exemple d’application Webauthn](https://github.com/MicrosoftEdge/webauthnsample).</span><span class="sxs-lookup"><span data-stu-id="c8c2a-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>

## <span data-ttu-id="c8c2a-117">Enregistrez votre utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-117">Register your user</span></span>

<span data-ttu-id="c8c2a-118">En tant que *fournisseur d’identité*, vous devez commencer par créer une authentification Web pour votre utilisateur à l’aide des informations d’identification Navigator. Credentials. **créer** une méthode.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-118">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the navigator.credentials.**create** method.</span></span> <span data-ttu-id="c8c2a-119">Avant d’enregistrer les informations d’identification de l’utilisateur sur votre serveur, vous devrez confirmer l’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="c8c2a-120">Pour cela, il suffit de lui envoyer un e-mail de confirmation ou de lui demander d’utiliser sa méthode de connexion traditionnelle.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>


<span data-ttu-id="c8c2a-121">La `create` méthode accepte les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-121">The `create` method takes the following parameters:</span></span>

 - **<span data-ttu-id="c8c2a-122">informations de la partie de confiance</span><span class="sxs-lookup"><span data-stu-id="c8c2a-122">relying party information</span></span>**

```javascript
    rp: {
        name: "WebAuthn Sample App",
        icon: "https://example.com/rpIcon.png"
    },
```

 - **<span data-ttu-id="c8c2a-123">informations de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-123">user account information</span></span>**

```javascript
    user: {
        id: stringToArrayBuffer("some.user.id"),
        name: "bob.smith@contoso.com",
        displayName: "Bob Smith",
        icon: "https://example.com/userIcon.png"
    },
```

 - **<span data-ttu-id="c8c2a-124">paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="c8c2a-124">crypto parameters</span></span>**

```javascript
    pubKeyCredParams: [
        {
            //External authenticators support the ES256 algorithm
            type: "public-key",
            alg: -7                 
        }, 
        {
            //Windows Hello supports the RS256 algorithm
            type: "public-key",
            alg: -257
        }
    ],
```

 - **<span data-ttu-id="c8c2a-125">paramètres de sélection de l’authentificateur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-125">authenticator selection parameters</span></span>**

```javascript
    authenticatorSelection: {
        //Select authenticators that support username-less flows
        requireResidentKey: true,
        //Select authenticators that have a second factor (e.g. PIN, Bio)
        userVerification: "required",
        //Selects between bound or detachable authenticators
        authenticatorAttachment: "platform"
    },
```

- **<span data-ttu-id="c8c2a-126">autres options</span><span class="sxs-lookup"><span data-stu-id="c8c2a-126">other options</span></span>**

```javascript
    //Select larger timeout values, as Microsoft Edge shows UI
    timeout: 50000,
    //an opaque challenge that the authenticator signs over
    challenge: challenge,
    //prevent re-registration by specifying existing credentials here
    excludeCredentials: [],
    //specifies whether you need an attestation statement
    attestation: "none" 
```

<span data-ttu-id="c8c2a-127">Vous pouvez utiliser les [paramètres de création des informations d’identification](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) pour configurer les informations d’identification que vous voulez créer.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-127">You can use [credential creation parameters](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span> <span data-ttu-id="c8c2a-128">En particulier, vous pouvez choisir de créer des informations d’identification Windows Hello en définissant sur `authenticatorAttachment` `platform` ou en itinérance sur un appareil FIDO2 externe en définissant `authenticatorAttachment` sur `cross-platform` .</span><span class="sxs-lookup"><span data-stu-id="c8c2a-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span> 

<span data-ttu-id="c8c2a-129">Lorsque vous utilisez la `create` méthode, Microsoft Edge demande d’abord à l’utilisateur de vérifier sa présence en numérisant son visage ou son empreinte digitale, en entrant un code confidentiel ou en effectuant une action sur un appareil FIDO2 externe.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span> <span data-ttu-id="c8c2a-130">Lorsque cette étape est terminée, l’authentificateur génère une paire de clés publique/privée et stocke la clé privée.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-130">Once this step is completed the authenticator will generate a public/private key pair and store the private key.</span></span> <span data-ttu-id="c8c2a-131">Ces informations d’identification sont créées par origine, par compte et ne peuvent pas être extraites, car elles sont stockées en toute sécurité sur l’appareil d’authentification.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span> 

<span data-ttu-id="c8c2a-132">La promesse qui en résulte renvoie un [objet d’attestation](https://w3c.github.io/webauthn/#sctn-attestation) qui représente les nouvelles informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn/#sctn-attestation) representing the new credential.</span></span> <span data-ttu-id="c8c2a-133">L’objet d’attestation contient la clé publique pour les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-133">The attestation object contains the public key for the credential.</span></span> <span data-ttu-id="c8c2a-134">Vous allez envoyer cet objet au serveur pour valider les authentifications à venir.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-134">You'll send this object to the server for validating future authentications.</span></span> <span data-ttu-id="c8c2a-135">Avant de revenir au serveur, vous devez coder les données brutes en base64.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>

**<span data-ttu-id="c8c2a-136">Client</span><span class="sxs-lookup"><span data-stu-id="c8c2a-136">Client</span></span>**

```javascript
<script>
    navigator.credentials.create({
        publicKey: createCredentialOptions
    }).then(rawAttestation => {
        var attestation = {
            id: base64encode(rawAttestation.rawId),
            clientDataJSON: arrayBufferToString(rawAttestation.response.clientDataJSON),
            attestationObject: base64encode(rawAttestation.response.attestationObject)
        };
        return rest_put("/credentials", attestation);
    })
</script>
```

<span data-ttu-id="c8c2a-137">Le serveur doit ensuite décoder l’objet d’attestation, effectuer des étapes de vérification, extraire la clé publique pour cette information d’identification et la stocker pour des authentifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span> <span data-ttu-id="c8c2a-138">La liste détaillée des étapes est disponible dans l' [algorithme d’inscription des informations d’identification](https://w3c.github.io/webauthn/#registering-a-new-credential) de la spécification webauthn.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn/#registering-a-new-credential) in the WebAuthn specification.</span></span>

**<span data-ttu-id="c8c2a-139">Serveur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-139">Server</span></span>**

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```

## <span data-ttu-id="c8c2a-140">Authentifier votre utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-140">Authenticate your user</span></span>

<span data-ttu-id="c8c2a-141">Une fois les informations d’identification créées sur le client, la prochaine fois que l’utilisateur tente de se connecter au site, il est possible de se connecter à l’aide de leurs informations d’identification Web plutôt qu’un mot de passe avec un appel de Navigator. Credentials. **obtenez**.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to navigator.credentials.**get**.</span></span>

<span data-ttu-id="c8c2a-142">La `get` méthode accepte la *demande* en tant que paramètre requis uniquement.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-142">The `get` method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="c8c2a-143">Le défi est une séquence opaque d’octets que le serveur enverra à un client pour se connecter à la clé privée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="c8c2a-144">Exemple:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-144">For example:</span></span>

**<span data-ttu-id="c8c2a-145">Serveur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-145">Server</span></span>**

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```

<span data-ttu-id="c8c2a-146">Après avoir récupéré une stimulation du serveur, vous devez appeler l’API Get avec les [options de demande d’informations d’identification](https://w3c.github.io/webauthn/#credentialrequestoptions-extension).</span><span class="sxs-lookup"><span data-stu-id="c8c2a-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn/#credentialrequestoptions-extension).</span></span> <span data-ttu-id="c8c2a-147">Microsoft Edge affiche une invite qui vérifie l’identité de l’utilisateur à l’aide de Windows Hello ou d’un appareil FIDO2 externe.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span> <span data-ttu-id="c8c2a-148">Une fois la vérification de l’utilisateur terminée, le défi sera signé dans l’appareil de plateforme sécurisée ou FIDO2 et la promesse sera renvoyée avec un [objet d’assertion](https://w3c.github.io/webauthn/#authenticatorassertionresponse) contenant la signature et d’autres métadonnées que vous pouvez envoyer au serveur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn/#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>

**<span data-ttu-id="c8c2a-149">Client</span><span class="sxs-lookup"><span data-stu-id="c8c2a-149">Client</span></span>**

```javascript
    var credentialRequestOptions = {
        //specifies which credential IDs are allowed to authenticate the user
        //if empty, any credential can authenticate the users
        allowCredentials: allowCredentials,
        //an opaque challenge that the authenticator signs over
        challenge: challenge,
        //Select larger timeout values, as Microsoft Edge shows UI
        timeout: 50000
    };

    navigator.credentials.get({
        publicKey: credentialRequestOptions
    }).then(rawAssertion => {
        var assertion = {
            id: base64encode(rawAssertion.rawId),
            clientDataJSON: arrayBufferToString(rawAssertion.response.clientDataJSON),
            userHandle: base64encode(rawAssertion.response.userHandle),
            signature: base64encode(rawAssertion.response.signature),
            authenticatorData: base64encode(rawAssertion.response.authenticatorData)
        };
        return rest_put("/assertion", assertion);
    })
```

<span data-ttu-id="c8c2a-150">Dès lors que vous recevez l’assertion sur le serveur, vous devrez valider la signature pour authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="c8c2a-151">Voici un exemple de code.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-151">The following is some sample code.</span></span>  <span data-ttu-id="c8c2a-152">Vous trouverez une liste détaillée des étapes dans l' [algorithme de vérification des affirmations](https://w3c.github.io/webauthn/#verifying-assertion) de la spécification webauthn.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn/#verifying-assertion) in the WebAuthn specification.</span></span>

**<span data-ttu-id="c8c2a-153">Serveur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-153">Server</span></span>**

```javascript
    var jwkToPem = require('jwk-to-pem')
    var crypto = require('crypto');

    ...

    // Using credential’s id attribute, look up the corresponding 
    // credential public key.
    var credential = await storage.Credentials.findOne({
        id: assertion.id
    });

    //Refer to sample to see how to verify client data and authenticator data

    ...

    //Using the credential public key from lookup, verify that sig is a valid
    //signature over the binary concatenation of authData and hash.
    var publicKey = credential.publicKeyJwk;
    var verify = (publicKey.kty === "RSA") ? crypto.createVerify('RSA-SHA256') : crypto.createVerify('sha256');
    verify.update(authData);
    verify.update(hash);
    if (!verify.verify(jwkToPem(publicKey), sig))
        throw new Error("Could not verify signature");

    //Verify signCount has increased or is zero 
    if (authenticatorData.signCount != 0 &&
        authenticatorData.signCount < credential.signCount) {
        throw new Error("Received signCount of " + authenticatorData.signCount +
            " expected signCount > " + credential.signCount);
    }
```

## <span data-ttu-id="c8c2a-154">Remarques sur l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c8c2a-154">Implementation notes</span></span>

### <span data-ttu-id="c8c2a-155">Plateformes prises en charge</span><span class="sxs-lookup"><span data-stu-id="c8c2a-155">Supported platforms</span></span>
- <span data-ttu-id="c8c2a-156">La version recommandée par le biais de l’API d’authentification Web peut être utilisée à partir de Microsoft Edge à partir de la version 17713 de EdgeHTML (version Insider Preview).</span><span class="sxs-lookup"><span data-stu-id="c8c2a-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 (Windows Insider Preview version 17713 and up).</span></span>
- <span data-ttu-id="c8c2a-157">La [version prédéfinie d’aperçu](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) de l’API d’authentification Web a été supprimée et n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) of the Web Authentication API has been removed and is no longer available.</span></span>
- <span data-ttu-id="c8c2a-158">L’API d’authentification Web n’est pas encore disponible pour les applications UWP et PWAs.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>
- <span data-ttu-id="c8c2a-159">Internet Explorer ne prend pas en charge l’API d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-159">Internet Explorer does not support the Web Authentication API.</span></span> 

### <span data-ttu-id="c8c2a-160">Authentificateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8c2a-160">Supported authenticators</span></span>
<span data-ttu-id="c8c2a-161">Dans Microsoft Edge, l’API d’authentification Web vous permet d’authentifier les utilisateurs dotés des technologies suivantes:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>
- <span data-ttu-id="c8c2a-162">**Windows Hello**, autorisant l’authentification par mot de passe sur un appareil avec le visage, les empreintes digitales ou le code confidentiel</span><span class="sxs-lookup"><span data-stu-id="c8c2a-162">**Windows Hello**, enabling passwordless on-device authentication with  face, fingerprint, or PIN</span></span>
- <span data-ttu-id="c8c2a-163">**FIDO2**, activation de l’authentification par un itinérance sans mot de passe avec un appareil amovible et une empreinte digitale ou un code confidentiel</span><span class="sxs-lookup"><span data-stu-id="c8c2a-163">**FIDO2**, enabling passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>
- <span data-ttu-id="c8c2a-164">**U2F**, qui permet d’authentifier en second facteur les sites Web non prêts pour le déplacement vers un modèle sans mot de passe.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-164">**U2F**, enabling strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>

### <span data-ttu-id="c8c2a-165">Considérations particulières pour Windows Hello</span><span class="sxs-lookup"><span data-stu-id="c8c2a-165">Special considerations for Windows Hello</span></span> 
<span data-ttu-id="c8c2a-166">Voici quelques points à noter lors de l’utilisation de l’authentificateur Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-166">A few things to note when using the Windows Hello authenticator:</span></span>
- <span data-ttu-id="c8c2a-167">Vous pouvez détecter si Windows Hello est disponible sur un PC en appelant l' `isUserVerifyingPlatformAuthenticatorAvailable` API.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span> <span data-ttu-id="c8c2a-168">En savoir plus sur cette API [ici](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable).</span><span class="sxs-lookup"><span data-stu-id="c8c2a-168">Learn more about this API [here](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>
- <span data-ttu-id="c8c2a-169">Lorsque vous créez une information d’identification pour Windows Hello, nous vous conseillons de définir pour `authenticatorAttachment` `platform` la meilleure utilisation possible de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
- <span data-ttu-id="c8c2a-170">Windows Hello ne prend en charge que RS256 (ALG-257) en tant qu’algorithme de clé publique.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-170">Windows Hello only supports RS256 (alg -257) as its public key algorithm.</span></span> <span data-ttu-id="c8c2a-171">Veillez à spécifier cet algorithme lors de la création d’une information d’identification.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-171">Be sure to specify this algorithm when creating a credential.</span></span>
- <span data-ttu-id="c8c2a-172">Pour recevoir une [instruction d’attestation du TPM](https://w3c.github.io/webauthn/#tpm-attestation), définissez l’attestation sur «direct» lors de l’appel de l' `create` API.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn/#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span> <span data-ttu-id="c8c2a-173">Le meilleur moyen d’attester.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-173">TPM attestation is a best effort.</span></span> <span data-ttu-id="c8c2a-174">Seuls les PC dotés du module de plateforme sécurisée 2,0 renverront une déclaration d’attestation du TPM, et le processus d’attestation peut échouer pour diverses raisons.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>
- <span data-ttu-id="c8c2a-175">Windows Hello utilise diverses méthodes pour protéger les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-175">Windows Hello employs a variety of ways to protect user credentials.</span></span> <span data-ttu-id="c8c2a-176">Vous pouvez vérifier la méthode utilisée pour protéger une information d’identification en consommant le champ [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) de l’objet d’attestation renvoyé lors de la création des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span> <span data-ttu-id="c8c2a-177">Voici la liste des AAGUIDs que Windows Hello peut retourner:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span> 
  - <span data-ttu-id="c8c2a-178">Authentificateurs logiciels sauvegardés</span><span class="sxs-lookup"><span data-stu-id="c8c2a-178">Software backed authenticators</span></span>
    - <span data-ttu-id="c8c2a-179">Authentificateur du logiciel Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-179">Windows Hello software authenticator:</span></span> `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`
    - <span data-ttu-id="c8c2a-180">Authentificateur logiciel Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-180">Windows Hello VBS software authenticator:</span></span> `6E96969E-A5CF-4AAD-9B56-305FE6C82795`
  - <span data-ttu-id="c8c2a-181">Module de plateforme sécurisée (TPM)</span><span class="sxs-lookup"><span data-stu-id="c8c2a-181">Trusted Platform Module (TPM) backed authenticators</span></span>
    - <span data-ttu-id="c8c2a-182">Authentificateur du matériel Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-182">Windows Hello hardware authenticator:</span></span> `08987058-CADC-4B81-B6E1-30DE50DCBE96`
    - <span data-ttu-id="c8c2a-183">Authentificateur matériel Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="c8c2a-183">Windows Hello VBS hardware authenticator:</span></span> `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`


### <span data-ttu-id="c8c2a-184">Surface d’API</span><span class="sxs-lookup"><span data-stu-id="c8c2a-184">API surface</span></span>
- <span data-ttu-id="c8c2a-185">Microsoft Edge dispose de la version complète de la version recommandée de la norme de base de connaissances de base en matière d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>
- <span data-ttu-id="c8c2a-186">L' [extension AppID](https://w3c.github.io/webauthn/#sctn-appid-extension) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-186">The [AppID extension](https://w3c.github.io/webauthn/#sctn-appid-extension) is supported.</span></span> 
- <span data-ttu-id="c8c2a-187">Aucune autre extension n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-187">No other extensions are supported.</span></span>


## <span data-ttu-id="c8c2a-188">Démos</span><span class="sxs-lookup"><span data-stu-id="c8c2a-188">Demos</span></span>

[<span data-ttu-id="c8c2a-189">Exemple de code pour le client et le serveur</span><span class="sxs-lookup"><span data-stu-id="c8c2a-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)

[<span data-ttu-id="c8c2a-190">Démo de Windows Hello test</span><span class="sxs-lookup"><span data-stu-id="c8c2a-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net/)

## <span data-ttu-id="c8c2a-191">Spécifier</span><span class="sxs-lookup"><span data-stu-id="c8c2a-191">Specification</span></span>

[<span data-ttu-id="c8c2a-192">Authentification Web: API d’accès aux informations d’identification de la clé publique</span><span class="sxs-lookup"><span data-stu-id="c8c2a-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn/)
