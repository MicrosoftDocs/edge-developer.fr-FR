---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Découvrez comment l’API d’authentification Web peut permettre aux applications Web d’utiliser Windows Hello et FIDO2 pour l’authentification des utilisateurs.
title: Authentification Web-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 07f1de47156f43ff4726e8907a123c2cb1afc337
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233064"
---
# Authentification Web et Windows Hello  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

L' [API d’authentification Web](https://w3c.github.io/webauthn) dans Microsoft Edge permet aux applications Web d’utiliser [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) et des [appareils FIDO2 externes](https://fidoalliance.org/fido2) pour l’authentification des utilisateurs, de sorte que vous et vos utilisateurs puissiez éviter les problèmes liés à la gestion des mots de passe (par exemple, tentatives de mot de passe, hameçonnage et journalisation de clé).  La mise en œuvre de Microsoft Edge actuelle est basée sur la recommandation de candidat à la spécification d’authentification Web.  

> [!IMPORTANT]
> Cette rubrique vous montre comment tester l’authentification Windows Hello et FIDO2 avec Microsoft Edge.  

À l’aide de l’authentification Web, le serveur envoie une demande de texte brut au navigateur.  Lorsque Microsoft Edge est en mesure de vérifier l’utilisateur par le biais de Windows Hello ou d’un appareil FIDO2 externe, le système signe le défi avec une clé privée précédemment déployée pour cet utilisateur et l’envoie au serveur.  Si le serveur peut valider la signature à l’aide de la clé publique qu’il a pour cet utilisateur et vérifier que la demande est correcte, il peut authentifier l’utilisateur en toute sécurité.  Dans le cas d’un [chiffrement asymétrique](https://en.wikipedia.org/wiki/Public-key_cryptography) tel que celui-ci, la clé publique n’a pas d’importance et la clé privée n’est jamais partagée.  Par ailleurs, la clé privée ne peut jamais être déplacée depuis des éléments sécurisés ou des systèmes modernes dotés d’un matériel de module de plateforme sécurisée.  

Il existe deux étapes de base pour l’utilisation de l’API d’authentification Web:  

1.  Enregistrez votre utilisateur avec `create`  
1.  Authentifier votre utilisateur avec `get`  

Le Guide de développement suivant vous guidera tout au long du processus à l’aide de l' [exemple d’application Webauthn](https://github.com/MicrosoftEdge/webauthnsample).  

## Enregistrez votre utilisateur  

En tant que fournisseur d’identité, vous devez commencer par créer une authentification Web pour votre utilisateur à l’aide de la `navigator.credentials.create` méthode.  Avant d’enregistrer les informations d’identification de l’utilisateur sur votre serveur, vous devrez confirmer l’identité de l’utilisateur.  Pour cela, il suffit de lui envoyer un e-mail de confirmation ou de lui demander d’utiliser sa méthode de connexion traditionnelle.  

La `create` méthode accepte les paramètres suivants:  

:::row:::
   :::column span="1":::
      **informations de la partie de confiance**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      rp: {
          name: "WebAuthn Sample App",
          icon: "https://example.com/rpIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **informations de compte d’utilisateur**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      user: {
          id: stringToArrayBuffer("some.user.id"),
          name: "bob.smith@contoso.com",
          displayName: "Bob Smith",
          icon: "https://example.com/userIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **paramètres de chiffrement**  
   :::column-end:::
   :::column span="3":::
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
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **paramètres de sélection de l’authentificateur**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      authenticatorSelection: {
          //Select authenticators that support username-less flows
          requireResidentKey: true,
          //Select authenticators that have a second factor (such as PIN, Bio)
          userVerification: "required",
          //Selects between bound or detachable authenticators
          authenticatorAttachment: "platform"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **autres options**  
   :::column-end:::
   :::column span="3":::
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
   :::column-end:::
:::row-end:::  

Vous pouvez utiliser les [paramètres de création des informations d’identification](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) pour configurer les informations d’identification que vous voulez créer.  En particulier, vous pouvez choisir de créer des informations d’identification Windows Hello en définissant sur `authenticatorAttachment` `platform` ou en itinérance sur un appareil FIDO2 externe en définissant `authenticatorAttachment` sur `cross-platform` .  

Lorsque vous utilisez la `create` méthode, Microsoft Edge demande d’abord à l’utilisateur de vérifier sa présence en numérisant son visage ou son empreinte digitale, en entrant un code confidentiel ou en effectuant une action sur un appareil FIDO2 externe.  Une fois cette étape terminée, l’authentificateur génère une paire de clés publicprivate et stocke la clé privée.  Ces informations d’identification sont créées par origine, par compte et ne peuvent pas être extraites, car elles sont stockées en toute sécurité sur l’appareil d’authentification.  

La promesse qui en résulte renvoie un [objet d’attestation](https://w3c.github.io/webauthn#sctn-attestation) qui représente les nouvelles informations d’identification.  L’objet d’attestation contient la clé publique pour les informations d’identification.  Vous allez envoyer cet objet au serveur pour valider les authentifications à venir.  Avant de revenir au serveur, vous devez coder les données brutes en base64.  

**Client**  

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

Le serveur doit ensuite décoder l’objet d’attestation, effectuer des étapes de vérification, extraire la clé publique pour cette information d’identification et la stocker pour des authentifications ultérieures.  La liste détaillée des étapes est disponible dans l' [algorithme d’inscription des informations d’identification](https://w3c.github.io/webauthn#registering-a-new-credential) de la spécification webauthn.  

**Serveur**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## Authentifier votre utilisateur  

Une fois les informations d’identification créées sur le client, la prochaine fois que l’utilisateur tente de se connecter au site, vous pouvez l’utiliser pour vous connecter à l’aide de leurs informations d’identification Web plutôt qu’un mot de passe avec un appel à `navigator.credentials.get` .  

La `get` méthode accepte la demande en tant que paramètre requis uniquement.  Le défi est une séquence opaque d’octets que le serveur enverra à un client pour se connecter à la clé privée de l’utilisateur.  Par exemple:  

**Serveur**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

Après avoir récupéré une stimulation du serveur, vous devez appeler l’API Get avec les [options de demande d’informations d’identification](https://w3c.github.io/webauthn#credentialrequestoptions-extension).  Microsoft Edge affiche une invite qui vérifie l’identité de l’utilisateur à l’aide de Windows Hello ou d’un appareil FIDO2 externe.  Une fois la vérification de l’utilisateur terminée, le défi sera signé dans l’appareil de plateforme sécurisée ou FIDO2 et la promesse sera renvoyée avec un [objet d’assertion](https://w3c.github.io/webauthn#authenticatorassertionresponse) contenant la signature et d’autres métadonnées que vous pouvez envoyer au serveur.  

**Client**  

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

Dès lors que vous recevez l’assertion sur le serveur, vous devrez valider la signature pour authentifier l’utilisateur.  Voici un exemple de code.  Vous trouverez une liste détaillée des étapes dans l' [algorithme de vérification des affirmations](https://w3c.github.io/webauthn#verifying-assertion) de la spécification webauthn.  

**Serveur**  

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

## Remarques sur l’implémentation  

### Plateformes prises en charge  

*   La version recommandée par le biais de l’API d’authentification Web peut être utilisée à partir de Microsoft Edge, à partir de la version 17713 de Windows Insider Preview (ou une version ultérieure).  
*   La [version prédéfinie d’aperçu](https://blogs.windows.com/msedgedev/2016/04/12) de l’API d’authentification Web a été supprimée et n’est plus disponible.  
*   L’API d’authentification Web n’est pas encore disponible pour les applications UWP et PWAs.  
*   Internet Explorer ne prend pas en charge l’API d’authentification Web.  

### Authentificateurs pris en charge  

Dans Microsoft Edge, l’API d’authentification Web vous permet d’authentifier les utilisateurs dotés des technologies suivantes:  

*   **Windows Hello**  Autorise l’authentification par mot de passe sur un appareil avec le visage, les empreintes digitales ou le code confidentiel.  
*   **FIDO2**  Active l’authentification par mot de passe avec un appareil amovible et une empreinte digitale ou un code confidentiel  
*   **U2F**  Autorise l’authentification en second facteur pour les sites Web qui ne sont pas prêts à être migrés vers un modèle sans mot de passe.  

### Considérations particulières pour Windows Hello  

Voici quelques points à noter lors de l’utilisation de l’authentificateur Windows Hello:  

*   Vous pouvez détecter si Windows Hello est disponible sur un PC en appelant l' `isUserVerifyingPlatformAuthenticatorAvailable` API.  En savoir plus sur cette API [ici](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).  
*   Lorsque vous créez une information d’identification pour Windows Hello, nous vous conseillons de définir pour `authenticatorAttachment` `platform` la meilleure utilisation possible de l’utilisateur.
*   Windows Hello ne prend en charge que RS256 \ (ALG-257 \) en tant qu’algorithme de clé publique.  Veillez à spécifier cet algorithme lors de la création d’une information d’identification.  
*   Pour recevoir une [instruction d’attestation du TPM](https://w3c.github.io/webauthn#tpm-attestation), définissez l’attestation sur «direct» lors de l’appel de l' `create` API.  Le meilleur moyen d’attester.  Seuls les PC dotés du module de plateforme sécurisée 2,0 renverront une déclaration d’attestation du TPM, et le processus d’attestation peut échouer pour diverses raisons.  
*   Windows Hello utilise diverses méthodes pour protéger les informations d’identification de l’utilisateur.  Vous pouvez vérifier la méthode utilisée pour protéger une information d’identification en consommant le champ [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) de l’objet d’attestation renvoyé lors de la création des informations d’identification.  Voici la liste des AAGUIDs que Windows Hello peut retourner:   
    *   Authentificateurs logiciels sauvegardés  
        *   Authentificateur du logiciel Windows Hello:  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   Authentificateur logiciel Windows Hello VBS:  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   Module de plateforme sécurisée (TPM)-authentificateurs sauvegardés  
        *   Authentificateur du matériel Windows Hello:  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   Authentificateur matériel Windows Hello VBS:  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### Surface d’API  

*   Microsoft Edge dispose de la version complète de la version recommandée de la norme de base de connaissances de base en matière d’authentification Web.  
*   L' [extension AppID](https://w3c.github.io/webauthn#sctn-appid-extension) est prise en charge.  
*   Aucune autre extension n’est prise en charge.  

## Démos  

[Exemple de code pour le client et le serveur](https://github.com/MicrosoftEdge/webauthnsample)  

[Démo de Windows Hello test](https://webauthnsample.azurewebsites.net)  

## Spécifier  

[Authentification Web: API d’accès aux informations d’identification de la clé publique](http://w3c.github.io/webauthn)  
