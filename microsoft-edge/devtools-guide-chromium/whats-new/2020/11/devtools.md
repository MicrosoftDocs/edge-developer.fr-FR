---
description: Microsoft Edge pour Linux, conseils d’amélioration de webhint dans l’outil problèmes, nouvelles fonctionnalités de débogage de travailleur de service, etc.
title: Nouveautés de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205242"
---
# Nouveautés de DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Le pilote Microsoft Edge et Microsoft Edge est désormais disponible sur Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge dev est désormais pris en charge sur les distributions Ubuntu, Debian, Fedora et openSUSE.  Téléchargez et installez le Microsoft Edge dev `.deb` ou le `.rpm` package directement à partir du [site Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou utilisez les outils de gestion des packages standard de votre distribution Linux.  

Si vous utilisez un environnement Linux dans vos solutions d’intégration et de remise en continu, vous pouvez également utiliser le pilote Microsoft Edge pour Linux.  Pour commencer à automatiser Microsoft Edge dev avec le pilote Microsoft Edge, accédez à la [page téléchargements de pilotes Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Pour obtenir de l’aide sur l’automatisation du développement Microsoft Edge avec le pilote Microsoft Edge, naviguez jusqu’à l' [utilisation de WebDriver (chrome) pour l’automatisation des tests][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools dans Microsoft Edge sur Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools dans Microsoft Edge sur Linux  
:::image-end:::  

## Amélioration de l’astuce et des conseils de plateforme dans l’outil problèmes  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Un outil open source, [webhint][WebhintMain], fournit des commentaires en temps réel sur les sites Web et les pages Web locales.  À partir de la [version 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], consultez les commentaires sur le webhint dans l’outil [problèmes][DevtoolsIssuesIndex] .  Il est désormais plus facile de passer en revue les problèmes qui s’affichent dans l’outil de **problèmes** en ajoutant les catégories suivantes.  

*   [Accessibilité][WebhintUserGuideHintsAccessibility]  
*   [Compatibilité][WebhintUserGuideHintsCompatibility]  
*   [Niveau de performance][WebhintUserGuideHintsPerformance]  
*   [Les pièges][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Sécurité][WebhintUserGuideHintsSecurity]  
    
Vous pouvez à présent filtrer les problèmes tiers à l’aide d’une nouvelle case à cocher.  La fonctionnalité de filtre vous aide à masquer les problèmes liés au code de bibliothèques tierces ou d’autres sources.  

Pour vous aider à passer en revue les problèmes détectés par [webhint][WebhintMain], l’outil **problèmes** affiche désormais les informations suivantes.  

*   Meilleurs extraits de code.  
*   Liens vers d’autres panneaux pertinents.  
*   Liens vers la documentation pour vous aider à résoudre les problèmes rencontrés sur votre site Web.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Outil problèmes" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Outil **problèmes**  
:::image-end:::  

## Les couches composites sont désormais en vue 3D  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

Il est possible que vous souhaitiez visualiser les contenus de **calques** avec les valeurs d’index z et le modèle d’objet document (DOM).  Cette fonctionnalité vous permet de déboguer sans basculer entre les outils d' [affichage 3D][Devtools3dViewIndex] et de **calques** .  Pour une interface de débogage complète, l' [affichage 3D et les couches composites sont désormais combinés][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Volet couches composites" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Volet **couches composites**  
:::image-end:::  

## Définitions des variables CSS dans le volet styles  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

Dans le volet **styles** , les [variables CSS][MdnUsingCssCustomProperties] sont désormais liées directement à chaque définition.  Choisissez la variable pour afficher ou modifier facilement la définition de variables CSS.  Dans l’exemple, DevTools affiche les attributs CSS pour l' `body` élément.  Pour afficher la définition de variable pour la `--theme-body-background` variable CSS, effectuez les actions suivantes.  

1.  Dans le volet **styles** , sélectionnez `var(--theme-body-background)` .  
1.  Le volet **styles** affiche désormais la définition de la `--theme-body-background` variable CSS.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variable CSS liée au style" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Variable CSS liée au style  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variable CSS liée à la cible de style" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Variable CSS liée à la cible de style  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Améliorations du débogage des travailleurs de services  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Les nouvelles fonctionnalités suivantes dans les outils [réseau](#network-tool), [application](#application-tool)et [sources](#sources-tool) vous aident à créer votre [PWA][ProgressiveWebAppsChromiumIndex].  Si vous éprouvez des difficultés à déboguer votre travailleur de service, utilisez les fonctionnalités suivantes.  

Demander le routage affiche `startup` les `fetch` événements et en fonction des requêtes réseau qui s’exécutent par le biais des travailleurs de service.  Les chronologies sont accessibles à partir de l’outil de l' **application** ou du **réseau** .  Les chronologies sont là lorsque vous rencontrez des problèmes avec les travailleurs de service et que vous souhaitez voir s’il y a un problème avec l' `startup` `fetch` événement ou.  

### Outil de l’application  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Affichez les informations de routage de toutes les demandes de service d’appel avec le nouveau lien **demandes réseau** .  Pour afficher un contexte supplémentaire lors du débogage du travailleur de service, procédez comme suit.  

1.  Accédez aux ****  >  **travailleurs de services**d’application.  
1.  Sélectionnez **requêtes réseau**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Ouvrir l’outil réseau via le volet travailleurs de service" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Ouvrir l’outil **réseau** via le volet **travailleurs de service**
    :::image-end:::  
    
1.  L’outil **réseau** s’ouvre dans le **tiroir** et affiche toutes les demandes réseau associées au travailleur du service.  Les requêtes réseau sont filtrées à l’aide de `is:service-worker-intercepted` .  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Outil réseau dans un tiroir" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Outil **réseau** dans un **tiroir**  
    :::image-end:::
    
1. Pour rétablir le panneau supérieur de l’outil **réseau** , fermez le **tiroir**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Fermez le tiroir de votre tiroir pour retourner le panneau de connexion." lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Fermez le **tiroir** de votre tiroir pour retourner le panneau de **connexion** .  
    :::image-end:::  
    
### Outil réseau  

Déboguer les requêtes réseau qui s’exécutent par le biais des travailleurs de service.  Vous pouvez également ouvrir des requêtes réseau à partir de l’outil de l' **application** .  Pour chaque demande, DevTools affiche les informations suivantes dans le volet [minutage][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .  

*   Le début d’une demande et la durée de l’amorce.  
*   Modification apportée à l’inscription des travailleurs de service.  
*   Exécution d’un `fetch` Gestionnaire d’événements.  
*   Exécution de tous les `fetch` événements de chargement d’un client.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Volet minutage" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Volet **minutage**  
:::image-end:::  

### Outil sources  

Dans les versions précédentes de Microsoft Edge, le niveau de profondeur de la pile d’appels était limité au code JavaScript de votre travailleur de service.  Dans Microsoft Edge 88, la pile d’appels affiche désormais l’initiateur de demandes qui s’exécutent par le biais de votre travailleur de service.  

Pour localiser l’initiateur de la requête, utilisez la pile d’appels de votre code JavaScript dans le travailleur de service.  La pile d’appels dans les figures suivantes commence par le code JavaScript de votre travailleur de service et affiche une référence à la demande de page Web d’origine `(index):157` .  Dans la deuxième figure, la référence est choisie et a ouvert l’initiateur qui a créé la demande.  Dans la deuxième figure, l’initiateur est la page Web.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Le fichier service-worker.js et la mise en surbrillance de la pile d’appels" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         L' `service-worker.js` émetteur de la demande de mise en surbrillance des piles de fichiers et d’appels  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La page Web (index) est l’initiateur de la requête" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         La `(index)` page Web est l’initiateur de la requête  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Copier la valeur de la propriété d’une demande réseau  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

Dans l’outil **réseau** , copiez la valeur de la propriété d’une demande réseau à l’aide de la nouvelle option **copier la valeur** .  La valeur de la propriété est copiée en tant que valeur JSON décodée.  Dans les versions précédentes de Microsoft Edge, vous deviez copier une valeur à l’aide de l’une des actions suivantes.  

*   Mettez en surbrillance l’intégralité du texte et copiez-le.  
*   Stockez la valeur en tant que variable globale, le cas échéant, puis copiez-la à partir de la [console][DevtoolsConsoleIndex]devtools.  
    
Pour copier la valeur de la propriété dans le presse-papiers, accédez à [copier la réponse mise en forme JSON dans le presse-papiers][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copier la valeur de la propriété dans DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Copier la valeur de la propriété dans DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Valeur de la propriété Paste dans le code Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Valeur de la propriété Paste dans le code Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Personnaliser les raccourcis clavier à plusieurs pression  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Depuis la version 87 de Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], vous pouvez personnaliser les raccourcis clavier pour n’importe quelle action dans devtools.  Dans la version 88 de Microsoft Edge, vous pouvez désormais créer des raccourcis clavier à plusieurs pression.  Pour définir un raccourci pour une action dans le devtools, accédez à la [section][DevtoolsCustomizeIndexSettings]expériences de paramètres,  >  **** puis cochez la case en regard de activer l' **éditeur de raccourcis clavier**.  Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérience de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Par exemple, la mise en surbrillance rouge affiche un raccourci clavier à plusieurs pression personnalisé pour l’action **commencer l’enregistrement des événements** .  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à l' [#174309 du problème][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Raccourcis clavier de cordes" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Raccourcis clavier à plusieurs pression  
:::image-end:::  

## Annonces du projet de chrome  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nouveaux outils de visualisation d’angle CSS  

DevTools dispose désormais d’une meilleure prise en charge du débogage d’angle CSS.  Lorsqu’un élément HTML de votre page est doté d’un angle CSS appliqué, une icône d’horloge s’affiche à côté de l’angle dans l’outil **styles** .  Pour activer ou désactiver la superposition de l’horloge, sélectionnez l’icône d’horloge.  Pour modifier l’angle, sélectionnez un emplacement quelconque dans l’horloge ou faites glisser l’aiguille.  Pour modifier la valeur de l’angle, vous pouvez également utiliser la souris et les raccourcis clavier.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [1126178][CR1126178] et [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

L’angle CSS suivant est utilisé pour l’exemple.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Angle CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Angle CSS  
:::image-end:::  

### Simuler une taille de quota de stockage dans le volet stockage  

Vous pouvez à présent ignorer la taille de quota de stockage dans le volet **stockage** .  Cette fonctionnalité permet de simuler différents appareils et de tester le comportement de votre site Web ou de votre application dans des scénarios de disponibilité du disque faible.  Pour simuler le quota de stockage, effectuez les actions suivantes.  

1.  Naviguez jusqu’à stockage d' **applications**  >  ****.  
1.  Activez la case à cocher **simuler le quota de stockage personnalisé** .  
1.  Entrez un numéro valide.  
    
Pour plus d’informations sur la façon d’émuler des appareils mobiles et d’autres fonctionnalités dans le DevTools, accédez à la section [émuler des appareils mobiles dans Microsoft Edge devtools ][DevtoolsDeviceModeIndex].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [945786][CR945786] et [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simuler la taille de quota de stockage" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simuler la taille de quota de stockage  
:::image-end:::  

### Signaler les erreurs CORS dans l’outil réseau  

Évaluez cette fonctionnalité en accédant à [démonstration d’erreur cors][GlitchCorsErrors].  Ouvrez l’outil **réseau** , actualisez la page et observez la demande de réseau de l’échec.  La colonne État affiche l' **erreur cors**.  Lorsque vous pointez sur l’erreur, l’info-bulle affiche maintenant le code d’erreur.  Dans la version 87 et les versions antérieures de Microsoft Edge, DevTools affichait uniquement le statut generic **(Failed)** pour les erreurs cors.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erreurs CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Erreurs CORS  
:::image-end:::  

### Mises à jour de l’affichage des détails du cadre  

#### Informations d’isolement sur une origine dans l’affichage des détails du cadre  

Le statut isolé entre l’origine est désormais affiché dans la section **isolement du & de sécurité** .  La nouvelle section disponibilité de l' **API** affiche la disponibilité du `SharedArrayBuffer` s \ (SAB \) et si les mémoires tampons pourraient être partagées en utilisant `postMessage()` .  Un avertissement de dépréciation s’affiche si le SAB et `postMessage()` est actuellement disponible, mais que le contexte n’est pas isolé.  Pour plus d’informations sur l’isolement entre les origines et sur les raisons de leur nécessité `SharedArrayBuffers` , accédez à [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informations sur l’origine" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Informations sur l’origine  
:::image-end:::  

#### Nouvelles informations des travailleurs sur le Web dans l’affichage Détails du cadre  

DevTools organise désormais les travailleurs sur le Web au cadre du cadre parent approprié.  Par exemple, si le `someName` cadre est créé `worker.js` , il `worker.js` apparaît `someName` dans la liste **trames** .  Pour afficher les détails du travailleur Web, effectuez les actions suivantes.  

1.  Ouvrir l’outil de l' **application** .  
1.  Développez un cadre qui contient des travailleurs Web.  
1.  Développez l’arborescence **travailleurs** .  
1.  Choisissez un travailleur.  
    
Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [1122507][CR1122507] et [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informations des travailleurs Web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Informations des travailleurs Web  
:::image-end:::  

#### Afficher les détails d’un cadre ouvrant pour les fenêtres ouvertes  

DevTools organise désormais les [fenêtres][MdnWindowConstructors] ouvertes sous le [Frame][MdnWindowFrames]parent approprié.  Par exemple, si le `top` cadre ouvre a `Window` à `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , la `Window` figure située sous `top` dans la liste des **cadres** .  

Pour afficher le cadre responsable de l’ouverture d’une autre fenêtre dans l’outil **éléments** , effectuez les actions suivantes.  

1.  Ouvrez l’arborescence des **cadres** .  
1.  Développez **fenêtres ouvertes** et choisissez le `Window` cadre parent que vous voulez connaître.  
1.  Cliquez sur le lien d' **encadrement d’ouverture** .  

Les détails sont affichés sur l’image à l’origine de l’ouverture d’une autre `Window` .  Pour afficher l’outil d’ouverture dans l’outil **éléments** , effectuez les actions suivantes.  

1.  Ouvrez l’arborescence des **cadres** .  
1.  Choisissez une fenêtre ouverte pour ouvrir les `Window` Détails.  
1.  Cliquez sur le lien d' **encadrement d’ouverture** .  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Informations de trames ouvertes" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Informations de trames ouvertes  
:::image-end:::  

### Copy StackTrace pour l’initiateur réseau  

Pour copier le StackTrace dans le presse-papiers, effectuez les actions suivantes.  

1.  Ouvrir le menu contextuel \ (cliquez avec le bouton droit sur \).  
1.  Choisissez **copier**le  >  **StackTrace**.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copier StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Copier StackTrace  
:::image-end:::  

### Aperçu de la valeur de la variable WASM sur mouseover  

Utilisez cette fonction pour vérifier la valeur d’une variable webassembly \ (WASM \) lorsque votre code est en pause.  Pour afficher la valeur actuelle d’une variable, pointez sur une variable.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez à problèmes [1058836][CR1058836] et [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Prévisualiser la variable WASM sur mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Prévisualiser la variable WASM sur mouseover  
:::image-end:::  

### Unités de mesure cohérentes pour la taille des fichiers et de la mémoire  

DevTools est désormais toujours utilisé `kB` pour l’affichage des tailles de fichiers et de mémoire.  Auparavant DevTools mélangées `kB` et `KiB` .

*   `kB` ou kilo-octets \ (10 ^ 3 ou 1000 octets \)  
*   `KiB` ou kibibyte \ (2 ^ 10 ou 1024 octets \)  
    
Par exemple, l’outil **réseau** précédemment utilisé `kB` dans les étiquettes, mais utilisé `KiB` dans les calculs.  Votre avis a démontré que cette incohérence a causé une confusion.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de chrome, accédez à la section problème [1035309][CR1035309].  

## Télécharger les canaux Microsoft Edge preview  

Si vous utilisez Windows, Linux ou macOS, envisagez d’utiliser [Microsoft Edge Preview] [MicrosoftEdgePreviewChannels] en tant que navigateur de développement par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Affichage 3D | Documents Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Présentation de la console | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourcis clavier-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activer les couches composites dans l’affichage 3D-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copier la réponse mise en forme JSON dans le presse-papiers-référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Afficher la répartition du temps d’une demande de référence d’analyse du réseau | Documents Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Utiliser le WebDriver (chrome) pour l’automatisation des tests | Documents Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows | Documents Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personnaliser les raccourcis clavier dans les paramètres-nouveautés de DevTools (Microsoft Edge 87) | Documents Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Commentaires sur les webhint dans le volet problèmes-nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger WebDriver | Développeur Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Télécharger les canaux Microsoft Edge Insider"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR174309]: https://crbug.com/174309 "Problème 174309: DevTools: autoriser pour personnaliser les raccourcis clavier/les combinaisons de touches | Bugs du chrome"  
[CR945786]: https://crbug.com/945786 "Problème 945786: DevTools: autoriser le remplacement de Navigator. Storage. Estimate () | Bugs du chrome"  
[CR1029427]: https://crbug.com/1029427 "Problème 1029427: réduisez la surcharge des performances de l’envoi de messages de protocole au premier plan | Bugs du chrome"  
[CR1035309]: https://crbug.com/1035309 "Problème 1035309: DevTools doit utiliser de manière cohérente Mo pour signifier mégaoctets, pas mebibyte | Bugs du chrome"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466: prendre en charge le débogage COOP/COEP dans DevTools | Bugs du chrome"  
[CR1058836]: https://crbug.com/1058836 "Problème 1058836: UX problèmes liés au débogage de WASM Bugs du chrome"  
[CR1071432]: https://crbug.com/1071432 "Problème 1071432: ☂️ WASM basique pour les développeurs | Bugs du chrome"  
[CR1107766]: https://crbug.com/1107766 "Problème 1107766: Affichez des informations sur les trames générées par’Window. Open () 'dans l’arborescence de trames | Bugs du chrome"  
[CR1122507]: https://crbug.com/1122507 "Problème 1122507: informations sur le travailleur de surface dans l’arborescence d’images | Bugs du chrome"  
[CR1126178]: https://crbug.com/1126178 "Problème 1126178: ☂ DevTools: CSS <type> composants | Bugs du chrome"  
[CR1130556]: https://crbug.com/1130556 "Problème 1130556: DevTools: test de substitution d’image (émulation) | Bugs du chrome"  
[CR1132084]: https://crbug.com/1132084 "Problème 1132084: il n’y a pas de moyen simple de copier la charge utile de requête JSON | Bugs du chrome"  
[CR1136394]: https://crbug.com/1136394 "Problème 1136394: outils Flexbox | Bugs du chrome"  
[CR1138633]: https://crbug.com/1138633 "Problème 1138633: DevTools: CSS <angle> le composant doit refléter son apparence de propriété dans l’arrière-plan d’horloge | Bugs du chrome"  
[CR1139615]: https://crbug.com/1139615 "Problème 1139615: l’initiateur réseau doit permettre de copier la trace de pile | Bugs du chrome"  
[CR1139899]: https://crbug.com/1139899 "Problème 1139899: signaler la disponibilité des API contrôlées dans l’affichage Détails de la trame | Bugs du chrome"  
[CR1139945]: https://crbug.com/1139945 "Problème 1139945: icônes pour les propriétés CSS de Flexbox dans le panneau Styles | Bugs du chrome"  
[CR1141824]: https://crbug.com/1141824 "Problème 1141824: améliorer le signalement des erreurs CORS dans DevTools | Bugs du chrome"  
[CR1144090]: https://crbug.com/1144090 "Problème 1144090: ajoutez des ornements de style Flex à l’arborescence des éléments | Bugs du chrome"  
[CR1146985]: https://crbug.com/1146985 "Problème 1146985: le texte supprimé reste affiché dans le champ texte de la section «stockage» de la fenêtre outils de développement | Bugs du chrome"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erreurs CORS | Problème"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Partage de ressources à l’origine (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation de propriétés personnalisées CSS (variables) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructeurs-fenêtre | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Fenêtre. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "Astuce"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accessibilité | Astuce"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilité | Astuce"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Performance | Astuce"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Pièges | Astuce"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | Astuce"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sécurité | Astuce"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/11/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
