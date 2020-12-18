---
description: Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools.
title: Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3200f22485bfd642a37a7d34ac727b8da4500d06
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231180"
---
# <span data-ttu-id="68db7-104">Émuler les authentificateurs et déboguer webauthn dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="68db7-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="68db7-105">Au lieu de déboguer l’authentification Web de votre site Web ou de votre application à l’aide d’authentificateurs physiques, utilisez l’outil **Webauthn** dans Microsoft Edge devtools pour créer des authentificateurs virtuels logiciels et interagir avec eux.</span><span class="sxs-lookup"><span data-stu-id="68db7-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="68db7-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="68db7-106">Before you begin</span></span>  

<span data-ttu-id="68db7-107">Le bon endroit où vous pouvez commencer à utiliser l’authentification Web est l' [API d’authentification Web][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="68db7-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="68db7-108">Configurer l’outil webauthn</span><span class="sxs-lookup"><span data-stu-id="68db7-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="68db7-109">Accédez à une page Web qui utilise webauthn, comme le site Web de démonstration suivant.</span><span class="sxs-lookup"><span data-stu-id="68db7-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="68db7-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="68db7-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="68db7-111">Connectez-vous au site Web.</span><span class="sxs-lookup"><span data-stu-id="68db7-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="68db7-112">[Ouvrez devtools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="68db7-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="68db7-113">Pour ouvrir l’outil **webauthn** , sélectionnez l’icône **personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **webauth**.</span><span class="sxs-lookup"><span data-stu-id="68db7-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Outil webauthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="68db7-115">Outil **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="68db7-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="68db7-116">Dans l’outil **Webauthn** , activez la case à cocher **activer l’environnement d’authentificateur virtuel** .</span><span class="sxs-lookup"><span data-stu-id="68db7-116">In the **WebAuthn** tool, turn on **Enable virtual authenticator environment** checkbox.</span></span>  
1.  <span data-ttu-id="68db7-117">Après activation, une nouvelle section nommée **nouvel authentificateur** est affichée.</span><span class="sxs-lookup"><span data-stu-id="68db7-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Activer l’environnement d’authentificateur virtuel" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="68db7-119">Activer l’environnement d’authentificateur virtuel</span><span class="sxs-lookup"><span data-stu-id="68db7-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="68db7-120">Dans la section **nouvel authentificateur** , configurez les options suivantes.</span><span class="sxs-lookup"><span data-stu-id="68db7-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="68db7-121">Option</span><span class="sxs-lookup"><span data-stu-id="68db7-121">Option</span></span> | <span data-ttu-id="68db7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="68db7-122">Value</span></span> | <span data-ttu-id="68db7-123">Détails</span><span class="sxs-lookup"><span data-stu-id="68db7-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="68db7-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="68db7-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="68db7-125">Protocole utilisé par l’authentificateur virtuel pour le codage et le décodage</span><span class="sxs-lookup"><span data-stu-id="68db7-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="68db7-126">, `nfc` ,, `ble` ou</span><span class="sxs-lookup"><span data-stu-id="68db7-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="68db7-127">L’authentificateur virtuel simule le transport sélectionné pour communiquer avec les clients afin d’obtenir une assertion pour une information d’identification spécifique.</span><span class="sxs-lookup"><span data-stu-id="68db7-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="68db7-128">Pour plus d’informations, accédez à l' [énumération de transport d’authentificateur][GithubW3cWebauthnEnumTransport] .</span><span class="sxs-lookup"><span data-stu-id="68db7-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="68db7-129">Activez \ (ou désactivez) à l’aide de la case à cocher</span><span class="sxs-lookup"><span data-stu-id="68db7-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="68db7-130">Activez la fonction si votre application Web repose sur les clés résidentes \ (également appelées informations d’identification pour la détection sur le client).</span><span class="sxs-lookup"><span data-stu-id="68db7-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="68db7-131">Pour plus d’informations, accédez à l' [énumération des besoins en clé résidente][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="68db7-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="68db7-132">Activez \ (ou désactivez) à l’aide de la case à cocher</span><span class="sxs-lookup"><span data-stu-id="68db7-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="68db7-133">Activez cette case à costar si votre application Web repose sur une autorisation locale à l’aide de modalités de geste telles que l’interaction tactile, le code confidentiel ou la reconnaissance biométrique.</span><span class="sxs-lookup"><span data-stu-id="68db7-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="68db7-134">Pour plus d’informations, accédez à [vérification utilisateur][GithubW3cWebauthnEnumUserverification] .</span><span class="sxs-lookup"><span data-stu-id="68db7-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="68db7-135">Cliquez sur le bouton **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="68db7-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="68db7-136">Une nouvelle section de votre authentificateur nouvellement créé s’affiche.</span><span class="sxs-lookup"><span data-stu-id="68db7-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authentificateur" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="68db7-138">Authentificateur</span><span class="sxs-lookup"><span data-stu-id="68db7-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="68db7-139">La section **authentificateur** inclut une table **Credentials** .</span><span class="sxs-lookup"><span data-stu-id="68db7-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="68db7-140">Le tableau est vide tant qu’aucune information d’identification n’est inscrite auprès de l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="68db7-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Aucune information d’identification" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="68db7-142">Aucune information d’identification</span><span class="sxs-lookup"><span data-stu-id="68db7-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="68db7-143">Enregistrer une nouvelle information d’identification</span><span class="sxs-lookup"><span data-stu-id="68db7-143">Register a new credential</span></span>  

<span data-ttu-id="68db7-144">Pour enregistrer une nouvelle information d’identification, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="68db7-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="68db7-145">Pour plus d’informations sur ce que fait l' [API d’authentification Web][GithubW3cWebauthn] lors de l’inscription d’une nouvelle information d’identification, accédez à [créer une nouvelle information d’identification][GithubW3cWebauthnSctnCreatecredential].</span><span class="sxs-lookup"><span data-stu-id="68db7-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="68db7-146">Sur le site Web de démonstration, choisissez **enregistrer les nouvelles informations d’identification**.</span><span class="sxs-lookup"><span data-stu-id="68db7-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="68db7-147">Une nouvelle information d’identification est désormais ajoutée à la table **informations d’identification** de l’outil webauthn.</span><span class="sxs-lookup"><span data-stu-id="68db7-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Afficher les informations d’identification" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="68db7-149">Afficher les informations d’identification</span><span class="sxs-lookup"><span data-stu-id="68db7-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="68db7-150">Sur le site Web de démonstration, sélectionnez le bouton **authentifier** .</span><span class="sxs-lookup"><span data-stu-id="68db7-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="68db7-151">Vérifiez que le [nombre de signes][GithubW3cWebauthnSctnSignCounter] d’informations d’identification figurant dans la table **Credentials** augmentait de 1, ce qui marque une opération [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] réussie.</span><span class="sxs-lookup"><span data-stu-id="68db7-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="68db7-152">Exporter et supprimer des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="68db7-152">Export and remove credentials</span></span>  

<span data-ttu-id="68db7-153">Pour exporter ou supprimer des informations d’identification, cliquez sur le bouton **Exporter** ou **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="68db7-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exporter ou supprimer des informations d’identification" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="68db7-155">Exporter ou supprimer des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="68db7-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="68db7-156">Renommer un authentificateur</span><span class="sxs-lookup"><span data-stu-id="68db7-156">Rename an authenticator</span></span>  

<span data-ttu-id="68db7-157">Pour renommer un authentificateur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="68db7-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="68db7-158">En regard du nom de l’authentificateur, sélectionnez le bouton **modifier** .</span><span class="sxs-lookup"><span data-stu-id="68db7-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="68db7-159">Modifiez le nom, puis appuyez sur **entrée** pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="68db7-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Renommer un authentificateur" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="68db7-161">Renommer un authentificateur</span><span class="sxs-lookup"><span data-stu-id="68db7-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="68db7-162">Définir l’authentificateur actif</span><span class="sxs-lookup"><span data-stu-id="68db7-162">Set the active authenticator</span></span>  

<span data-ttu-id="68db7-163">Un authentificateur nouvellement créé est automatiquement activé.</span><span class="sxs-lookup"><span data-stu-id="68db7-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="68db7-164">Pour utiliser un autre authentificateur virtuel, sélectionnez la case d’option **active** en regard de l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="68db7-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="68db7-165">DevTools ne prend en charge qu’un seul authentificateur virtuel actif à tout moment.</span><span class="sxs-lookup"><span data-stu-id="68db7-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="68db7-166">Si vous supprimez l’authentificateur actif, un autre authentificateur n’est pas activé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="68db7-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Définir l’authentificateur actif" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="68db7-168">Définir l’authentificateur actif</span><span class="sxs-lookup"><span data-stu-id="68db7-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="68db7-169">Supprimer un authentificateur virtuel</span><span class="sxs-lookup"><span data-stu-id="68db7-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="68db7-170">Pour supprimer un authentificateur virtuel, en regard de l’authentificateur, cliquez sur le bouton **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="68db7-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Supprimer l’authentificateur" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="68db7-172">Supprimer l’authentificateur</span><span class="sxs-lookup"><span data-stu-id="68db7-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="68db7-173">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="68db7-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

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
> <span data-ttu-id="68db7-185">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68db7-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="68db7-186">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="68db7-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="68db7-188">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="68db7-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
