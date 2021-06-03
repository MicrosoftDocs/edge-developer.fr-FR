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
# <a name="emulate-authenticators-and-debug-webauthn-in-microsoft-edge-devtools"></a><span data-ttu-id="ca956-104">Émuler les authentifiés et déboguer WebAuthn dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ca956-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ca956-105">Au lieu de déboguer l’authentification Web dans votre site web ou votre application avec des authentifiés physiques, utilisez l’outil **WebAuthn** dans Microsoft Edge DevTools pour créer des authentifiés virtuels logiciels et interagir avec eux.</span><span class="sxs-lookup"><span data-stu-id="ca956-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="ca956-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ca956-106">Before you begin</span></span>  

<span data-ttu-id="ca956-107">Un excellent point de départ avec l’authentification web est la spécification de [l’API d’authentification web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="ca956-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <a name="set-up-the-webauthn-tool"></a><span data-ttu-id="ca956-108">Configurer l’outil WebAuthn</span><span class="sxs-lookup"><span data-stu-id="ca956-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="ca956-109">Accédez à une page web qui utilise WebAuthn, telle que le site web de démonstration suivant.</span><span class="sxs-lookup"><span data-stu-id="ca956-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="ca956-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="ca956-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="ca956-111">Connectez-vous au site web.</span><span class="sxs-lookup"><span data-stu-id="ca956-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="ca956-112">[Ouvrez DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="ca956-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="ca956-113">Pour ouvrir **l’outil WebAuthn,** choisissez l’icône Personnaliser et contrôler **DevTools** \( \) > `...` **outils**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="ca956-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Outil WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="ca956-115">**Outil WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="ca956-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca956-116">Dans **l’outil WebAuthn,** activez la case à cocher Activer l’environnement **d’authentifier** virtuel.</span><span class="sxs-lookup"><span data-stu-id="ca956-116">In the **WebAuthn** tool, turn on **Enable virtual authenticator environment** checkbox.</span></span>  
1.  <span data-ttu-id="ca956-117">Une fois activée, une nouvelle section nommée **Nouvel authentifié** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ca956-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Activer l’environnement d’authentifier virtuel" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="ca956-119">Activer l’environnement d’authentifier virtuel</span><span class="sxs-lookup"><span data-stu-id="ca956-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="ca956-120">Dans la section **Nouvel authentifié,** configurez les options suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca956-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="ca956-121">Option</span><span class="sxs-lookup"><span data-stu-id="ca956-121">Option</span></span> | <span data-ttu-id="ca956-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca956-122">Value</span></span> | <span data-ttu-id="ca956-123">Détails</span><span class="sxs-lookup"><span data-stu-id="ca956-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="ca956-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="ca956-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="ca956-125">Protocole utilisé par l’authentateur virtuel pour l’encodage et le décodage</span><span class="sxs-lookup"><span data-stu-id="ca956-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="ca956-126">, `nfc` `ble` ou</span><span class="sxs-lookup"><span data-stu-id="ca956-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="ca956-127">L’authentifié virtuel simule le transport sélectionné pour communiquer avec les clients afin d’obtenir une assertion pour une identification spécifique.</span><span class="sxs-lookup"><span data-stu-id="ca956-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="ca956-128">Pour plus d’informations, [accédez à l Authenticator éumération de transport][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="ca956-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="ca956-129">Activer \(ou désactiver\) à l’aide de la case à cocher</span><span class="sxs-lookup"><span data-stu-id="ca956-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="ca956-130">Activer si votre application web s’appuie sur des clés résidentes \(également appelées informations d’identification découvrables côté client\).</span><span class="sxs-lookup"><span data-stu-id="ca956-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="ca956-131">Pour plus d’informations, accédez à [l’éumération des conditions requises de la clé résidente.][GithubW3cWebauthnEnumResidentkeyrequirement]</span><span class="sxs-lookup"><span data-stu-id="ca956-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="ca956-132">Activer \(ou désactiver\) à l’aide de la case à cocher</span><span class="sxs-lookup"><span data-stu-id="ca956-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="ca956-133">Activer si votre application web s’appuie sur l’autorisation locale à l’aide de modalités de mouvement telles que l’entrée tactile, le code confidentiel, l’entrée de mot de passe ou la reconnaissance biométrique.</span><span class="sxs-lookup"><span data-stu-id="ca956-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="ca956-134">Pour plus d’informations, accédez à [Vérification de l’utilisateur][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="ca956-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="ca956-135">Choisissez le **bouton** Ajouter.</span><span class="sxs-lookup"><span data-stu-id="ca956-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="ca956-136">Une nouvelle section de votre authentifié nouvellement créé s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ca956-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="ca956-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="ca956-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ca956-139">La **section Authenticator** comprend une table **Credentials.**</span><span class="sxs-lookup"><span data-stu-id="ca956-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="ca956-140">La table est vide jusqu’à ce qu’une informations d’identification soit inscrite auprès de l’authentifié.</span><span class="sxs-lookup"><span data-stu-id="ca956-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Aucune informations d’identification" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="ca956-142">Aucune informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ca956-142">No credentials</span></span>  
:::image-end:::  

## <a name="register-a-new-credential"></a><span data-ttu-id="ca956-143">Enregistrer de nouvelles informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ca956-143">Register a new credential</span></span>  

<span data-ttu-id="ca956-144">Pour inscrire de nouvelles informations d’identification, effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca956-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="ca956-145">Pour plus d’informations sur les fonctionnalités de [l’API][GithubW3cWebauthn] d’authentification web lors de l’inscription d’une nouvelle information d’identification, accédez à [Créer une nouvelle information d’identification.][GithubW3cWebauthnSctnCreatecredential]</span><span class="sxs-lookup"><span data-stu-id="ca956-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="ca956-146">Sur le site web de démonstration, **sélectionnez Enregistrer les nouvelles informations d’identification.**</span><span class="sxs-lookup"><span data-stu-id="ca956-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="ca956-147">Une nouvelle informations d’identification est désormais ajoutée à la table **Credentials** de l’outil WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="ca956-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Afficher les informations d’identification" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="ca956-149">Afficher les informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ca956-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ca956-150">Sur le site web de démonstration, sélectionnez le **bouton Authentifier.**</span><span class="sxs-lookup"><span data-stu-id="ca956-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="ca956-151">Vérifiez que le nombre [de signatures][GithubW3cWebauthnSctnSignCounter] des informations d’identification dans la table **Credentials** a augmenté de 1, ce qui marque une opération [d’authentificationGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] réussie.</span><span class="sxs-lookup"><span data-stu-id="ca956-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <a name="export-and-remove-credentials"></a><span data-ttu-id="ca956-152">Exporter et supprimer des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ca956-152">Export and remove credentials</span></span>  

<span data-ttu-id="ca956-153">Pour exporter ou supprimer des informations d’identification, sélectionnez le bouton **Exporter** **ou** Supprimer.</span><span class="sxs-lookup"><span data-stu-id="ca956-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exporter ou supprimer des informations d’identification" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="ca956-155">Exporter ou supprimer des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ca956-155">Export or remove a credential</span></span>  
:::image-end:::  

## <a name="rename-an-authenticator"></a><span data-ttu-id="ca956-156">Renommer un authentifié</span><span class="sxs-lookup"><span data-stu-id="ca956-156">Rename an authenticator</span></span>  

<span data-ttu-id="ca956-157">Pour renommer un authentifié, effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca956-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="ca956-158">En de côté du nom de l’authentifié, sélectionnez **le bouton** Modifier.</span><span class="sxs-lookup"><span data-stu-id="ca956-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="ca956-159">Modifiez le nom, puis choisissez **Entrée** pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="ca956-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Renommer un authentifié" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="ca956-161">Renommer un authentifié</span><span class="sxs-lookup"><span data-stu-id="ca956-161">Rename an authenticator</span></span>  
:::image-end:::  

## <a name="set-the-active-authenticator"></a><span data-ttu-id="ca956-162">Définir l’authentifié actif</span><span class="sxs-lookup"><span data-stu-id="ca956-162">Set the active authenticator</span></span>  

<span data-ttu-id="ca956-163">Un authentifié nouvellement créé est automatiquement activé.</span><span class="sxs-lookup"><span data-stu-id="ca956-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="ca956-164">Pour utiliser un autre authentifié virtuel, choisissez la **radio active** en côté de l’authentifié.</span><span class="sxs-lookup"><span data-stu-id="ca956-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="ca956-165">DevTools prend en charge un seul authentifié virtuel actif à tout moment.</span><span class="sxs-lookup"><span data-stu-id="ca956-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="ca956-166">Si vous supprimez l’authentifié actif, un autre authentifié n’est pas activé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ca956-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Définir l’authentifié actif" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="ca956-168">Définir l’authentifié actif</span><span class="sxs-lookup"><span data-stu-id="ca956-168">Set active authenticator</span></span>  
:::image-end:::  

## <a name="remove-a-virtual-authenticator"></a><span data-ttu-id="ca956-169">Supprimer un authentifié virtuel</span><span class="sxs-lookup"><span data-stu-id="ca956-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="ca956-170">Pour supprimer un authentifié virtuel, à côté de l’authentifié, choisissez le **bouton** Supprimer.</span><span class="sxs-lookup"><span data-stu-id="ca956-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Supprimer l’authentifié" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="ca956-172">Supprimer l’authentifié</span><span class="sxs-lookup"><span data-stu-id="ca956-172">Remove authenticator</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ca956-173">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ca956-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge devTools | Documents Microsoft"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Démonstration Webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Client to Authenticator Protocol (CTAP) | fido alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Vue d’ensemble du facteur U2F (Universal 2nd Factor) | fido alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Authentification web : API permettant d’accéder aux informations d’identification de clé publique de niveau 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Opération authenticatorGetAssertion - Authentification web : API permettant d’accéder aux informations d’identification de clé publique niveau 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Transport Enumeration (enum AuthenticatorTransport) - Authentification web : UNE API pour accéder aux informations d’identification de clé publique niveau 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Resident Key Requirement Enumeration (enum ResidentKeyRequirement) - Web Authentication: An API for accessing Public Key Credentials Level 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Vérification de l’utilisateur - Authentification web : API permettant d’accéder aux informations d’identification de clé publique de niveau 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential’s [[Create]](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considérations sur le compteur de signature - Authentification web : API permettant d’accéder aux informations d’identification de clé publique niveau 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="ca956-185">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ca956-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ca956-186">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="ca956-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ca956-188">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ca956-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
