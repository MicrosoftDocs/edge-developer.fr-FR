---
description: Émuler les authentifiés et déboguer WebAuthn dans Microsoft Edge DevTools.
title: Émuler les authentifiés et déboguer WebAuthn dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d5eeedfaa98e56bbba81634685a223844803a1ad
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564034"
---
# <a name="emulate-authenticators-and-debug-webauthn-in-microsoft-edge-devtools"></a>Émuler les authentifiés et déboguer WebAuthn dans Microsoft Edge DevTools  

Au lieu de déboguer l’authentification Web dans votre site web ou votre application avec des authentifiés physiques, utilisez l’outil **WebAuthn** dans Microsoft Edge DevTools pour créer des authentifiés virtuels logiciels et interagir avec eux.  

## <a name="before-you-begin"></a>Avant de commencer  

Un excellent point de départ avec l’authentification web est la spécification de [l’API d’authentification web.][GithubW3cWebauthn]  

## <a name="set-up-the-webauthn-tool"></a>Configurer l’outil WebAuthn  

1.  Accédez à une page web qui utilise WebAuthn, telle que le site web de démonstration suivant.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Connectez-vous au site web.  
1.  [Ouvrez DevTools][DevtoolsGuideChromiumOpen].  
1.  Pour ouvrir **l’outil WebAuthn,** choisissez l’icône Personnaliser et contrôler **DevTools** \( \) > `...` **outils**  >  **WebAuthn**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Outil WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       **Outil WebAuthn**  
    :::image-end:::  
    
1.  Dans **l’outil WebAuthn,** activez la case à cocher Activer l’environnement **d’authentifier** virtuel.  
1.  Une fois activée, une nouvelle section nommée **Nouvel authentifié** s’affiche.  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Activer l’environnement d’authentifier virtuel" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Activer l’environnement d’authentifier virtuel**  
    :::image-end:::  
    
1.  Dans la section **Nouvel authentifié,** configurez les options suivantes.  
    
    | Option | Valeur | Détails |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | Protocole utilisé par l’authentateur virtuel pour l’encodage et le décodage |  
    | `Transport` |   `usb`, `nfc` `ble` ou `internal` | L’authentifié virtuel simule le transport sélectionné pour communiquer avec les clients afin d’obtenir une assertion pour une identification spécifique.  Pour plus d’informations, [accédez à l Authenticator éumération de transport][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Activer \(ou désactiver\) à l’aide de la case à cocher | Activer si votre application web s’appuie sur des clés résidentes \(également appelées informations d’identification découvrables côté client\).  Pour plus d’informations, accédez à [l’éumération des conditions requises de la clé résidente.][GithubW3cWebauthnEnumResidentkeyrequirement] |  
    | `Supports user verification` | Activer \(ou désactiver\) à l’aide de la case à cocher | Activer si votre application web s’appuie sur l’autorisation locale à l’aide de modalités de mouvement telles que l’entrée tactile, le code confidentiel, l’entrée de mot de passe ou la reconnaissance biométrique.  Pour plus d’informations, accédez à [Vérification de l’utilisateur][GithubW3cWebauthnEnumUserverification] |  
    
1.  Choisissez le **bouton** Ajouter.  
1.  Une nouvelle section de votre authentifié nouvellement créé s’affiche.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
La **section Authenticator** comprend une table **Credentials.**  La table est vide jusqu’à ce qu’une informations d’identification soit inscrite auprès de l’authentifié.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Aucune informations d’identification" lightbox="../media/webauthn-no-cred.msft.png":::
   Aucune informations d’identification  
:::image-end:::  

## <a name="register-a-new-credential"></a>Enregistrer de nouvelles informations d’identification  

Pour inscrire de nouvelles informations d’identification, effectuer les étapes suivantes.  Pour plus d’informations sur les fonctionnalités de [l’API][GithubW3cWebauthn] d’authentification web lors de l’inscription d’une nouvelle information d’identification, accédez à [Créer une nouvelle information d’identification.][GithubW3cWebauthnSctnCreatecredential]  

1.  Sur le site web de démonstration, **sélectionnez Enregistrer les nouvelles informations d’identification.**  
1.  De nouvelles informations d’identification sont désormais ajoutées à la table **Credentials** de l’outil WebAuthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Afficher les informations d’identification" lightbox="../media/webauthn-view-cred.msft.png":::
       Afficher les informations d’identification  
    :::image-end:::  
    
Sur le site web de démonstration, sélectionnez le **bouton Authentifier.**  Vérifiez que le nombre [de signatures][GithubW3cWebauthnSctnSignCounter] des informations d’identification dans la table **Credentials** a augmenté de 1, ce qui marque une opération [d’authentificationGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] réussie.  

## <a name="export-and-remove-credentials"></a>Exporter et supprimer des informations d’identification  

Pour exporter ou supprimer des informations d’identification, sélectionnez le bouton **Exporter** **ou** Supprimer.  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exporter ou supprimer des informations d’identification" lightbox="../media/webauthn-export-remove.msft.png":::
   Exporter ou supprimer des informations d’identification  
:::image-end:::  

## <a name="rename-an-authenticator"></a>Renommer un authentifié  

Pour renommer un authentifié, effectuer les étapes suivantes.  

1.  En de côté du nom de l’authentifié, sélectionnez **le bouton** Modifier.  
1.  Modifiez le nom, puis choisissez **Entrée** pour enregistrer les modifications.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Renommer un authentifié" lightbox="../media/webauthn-rename.msft.png":::
   Renommer un authentifié  
:::image-end:::  

## <a name="set-the-active-authenticator"></a>Définir l’authentifié actif  

Un authentifié nouvellement créé est automatiquement activé.  Pour utiliser un autre authentifié virtuel, choisissez la **radio active** en côté de l’authentifié.  

> [!NOTE]
> DevTools prend en charge un seul authentifié virtuel actif à tout moment.  Si vous supprimez l’authentifié actif, un autre authentifié n’est pas activé automatiquement.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Définir l’authentifié actif" lightbox="../media/webauthn-set-active.msft.png":::
   Définir l’authentifié actif  
:::image-end:::  

## <a name="remove-a-virtual-authenticator"></a>Supprimer un authentifié virtuel  

Pour supprimer un authentifié virtuel, à côté de l’authentifié, choisissez le **bouton** Supprimer.  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Supprimer l’authentifié" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Supprimer l’authentifié  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Démonstration Webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Client to Authenticator Protocol (CTAP) | fido alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Vue d’ensemble du facteur 2nd universel (U2F) | fido alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Authentification web : API permettant d’accéder aux informations d’identification de clé publique de niveau 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Opération authenticatorGetAssertion - Authentification web : API permettant d’accéder aux informations d’identification de clé publique niveau 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Transport Enumeration (enum AuthenticatorTransport) : Authentification web : API permettant d’accéder aux informations d’identification de clé publique niveau 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Resident Key Requirement Enumeration (enum ResidentKeyRequirement) - Web Authentication: An API for accessing Public Key Credentials Level 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Vérification de l’utilisateur - Authentification web : API permettant d’accéder aux informations d’identification de clé publique de niveau 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential’s [[Create]](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considérations sur le compteur de signature - Authentification web : API permettant d’accéder aux informations d’identification de clé publique niveau 2 | GitHub"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
