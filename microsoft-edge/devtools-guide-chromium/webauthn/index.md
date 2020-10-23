---
description: Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools.
title: Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6727e9aeea1a51689a80570a2f1c9df880a8c9db
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134046"
---
# Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools  

Au lieu de déboguer l’authentification Web de votre site Web ou de votre application à l’aide d’authentificateurs physiques, utilisez l’outil **Webauthn** dans Microsoft Edge devtools pour créer des authentificateurs virtuels logiciels et interagir avec eux.  

## Avant de commencer  

Le bon endroit où vous pouvez commencer à utiliser l’authentification Web est l' [API d’authentification Web][GithubW3cWebauthn].  

## Configurer l’outil webauthn  

1.  Accédez à une page Web qui utilise webauthn, comme le site Web de démonstration suivant.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Connectez-vous au site Web.  
1.  [Ouvrez devtools][DevtoolsGuideChromiumOpen].  
1.  Pour ouvrir l’outil **webauthn** , sélectionnez l’icône **personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **webauth**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       Outil **Webauthn**  
    :::image-end:::  
    
1.  Dans l’outil **Webauthn** , activez la case à cocher en regard de **activer l’environnement d’authentificateur virtuel**.  
1.  Après activation, une nouvelle section nommée **nouvel authentificateur** est affichée.  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Activer l’environnement d’authentificateur virtuel**  
    :::image-end:::  
    
1.  Dans la section **nouvel authentificateur** , configurez les options suivantes.  
    
    | Option | Valeur | Détails |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | Protocole utilisé par l’authentificateur virtuel pour le codage et le décodage |  
    | `Transport` |   `usb`, `nfc` ,, `ble` ou `internal` | L’authentificateur virtuel simule le transport sélectionné pour communiquer avec les clients afin d’obtenir une assertion pour une information d’identification spécifique.  Pour plus d’informations, accédez à l' [énumération de transport d’authentificateur][GithubW3cWebauthnEnumTransport] . |  
    |  `Supports resident keys` | Activez \ (ou désactivez) à l’aide de la case à cocher | Activez la fonction si votre application Web repose sur les clés résidentes \ (également appelées informations d’identification pour la détection sur le client).  Pour plus d’informations, accédez à l' [énumération des besoins en clé résidente][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Activez \ (ou désactivez) à l’aide de la case à cocher | Activez cette case à costar si votre application Web repose sur une autorisation locale à l’aide de modalités de geste telles que l’interaction tactile, le code confidentiel ou la reconnaissance biométrique.  Pour plus d’informations, accédez à [vérification utilisateur][GithubW3cWebauthnEnumUserverification] . |  
    
1.  Cliquez sur le bouton **Ajouter** .  
1.  Une nouvelle section de votre authentificateur nouvellement créé s’affiche.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-authenticator.msft.png":::
       Authentificateur  
    :::image-end:::  
    
La section **authentificateur** inclut une table **Credentials** .  Le tableau est vide tant qu’aucune information d’identification n’est inscrite auprès de l’authentificateur.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-no-cred.msft.png":::
   Aucune information d’identification  
:::image-end:::  

## Enregistrer une nouvelle information d’identification  

Pour enregistrer une nouvelle information d’identification, procédez comme suit.  Pour plus d’informations sur ce que fait l' [API d’authentification Web][GithubW3cWebauthn] lors de l’inscription d’une nouvelle information d’identification, accédez à [créer une nouvelle information d’identification][GithubW3cWebauthnSctnCreatecredential].  

1.  Sur le site Web de démonstration, choisissez **enregistrer les nouvelles informations d’identification**.  
1.  Une nouvelle information d’identification est désormais ajoutée à la table **informations d’identification** de l’outil webauthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-view-cred.msft.png":::
       Afficher les informations d’identification  
    :::image-end:::  
    
Sur le site Web de démonstration, sélectionnez le bouton **authentifier** .  Vérifiez que le [nombre de signes][GithubW3cWebauthnSctnSignCounter] d’informations d’identification figurant dans la table **Credentials** augmentait de 1, ce qui marque une opération [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] réussie.  

## Exporter et supprimer des informations d’identification  

Pour exporter ou supprimer des informations d’identification, cliquez sur le bouton **Exporter** ou **supprimer** .  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-export-remove.msft.png":::
   Exporter ou supprimer des informations d’identification  
:::image-end:::  

## Renommer un authentificateur  

Pour renommer un authentificateur, procédez comme suit.  

1.  En regard du nom de l’authentificateur, sélectionnez le bouton **modifier** .  
1.  Modifiez le nom, puis appuyez sur **entrée** pour enregistrer les modifications.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-rename.msft.png":::
   Renommer un authentificateur  
:::image-end:::  

## Définir l’authentificateur actif  

Un authentificateur nouvellement créé est automatiquement activé.  Pour utiliser un autre authentificateur virtuel, sélectionnez la case d’option **active** en regard de l’authentificateur.  

> [!NOTE]
> DevTools ne prend en charge qu’un seul authentificateur virtuel actif à tout moment.  Si vous supprimez l’authentificateur actif, un autre authentificateur n’est pas activé automatiquement.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-set-active.msft.png":::
   Définir l’authentificateur actif  
:::image-end:::  

## Supprimer un authentificateur virtuel  

Pour supprimer un authentificateur virtuel, en regard de l’authentificateur, cliquez sur le bouton **supprimer** .  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Supprimer l’authentificateur  
:::image-end:::  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Démonstration webauth Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocole client to Authenticator (CTAP) | notre Alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Vue d’ensemble du 2ème facteur (U2F) notre Alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Authentification Web: API d’accès aux informations d’identification de la clé publique niveau 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Opération authenticatorGetAssertion-Web Authentication: API d’accès aux informations d’identification de la clé publique niveau 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Enumeration de transport Authenticator (énum AuthenticatorTransport)-authentification Web: API d’accès aux informations d’identification de la clé publique niveau 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Énumération des conditions de clé résidentes (énum ResidentKeyRequirement)-authentification Web: API d’accès aux informations d’identification de la clé publique niveau 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Vérification de l’utilisateur-authentification Web: API d’accès aux informations d’identification de la clé publique niveau 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Créer une nouvelle information d’identification-PublicKeyCredential [[création]] (Origin, options, sameOriginWithAncestors) méthode-authentification Web: API d’accès aux informations d’identification de la clé publique niveau 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considérations relatives aux compteurs de signature-authentification Web: API d’accès aux informations d’identification de la clé publique niveau 2 | GitHub"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
