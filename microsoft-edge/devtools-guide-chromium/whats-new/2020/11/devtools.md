---
description: Microsoft Edge sur Linux, conseils d’amélioration de webhint dans l’outil problèmes, nouvelles fonctionnalités de débogage du worker du service et plus.
title: Nouveautés de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 7f4f9e2602d26b09a8b52a570c4caaaccc4f04f1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439274"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-88"></a>Nouveautés de DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a>Microsoft Edge et le pilote Microsoft Edge désormais disponible sur Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge dev est désormais pris en charge sur les distributions Ubuntu, Debian, Fedora et openSUSE.  Téléchargez et installez le Microsoft Edge dev `.deb` ou le `.rpm` package directement à partir du [site Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou utilisez les outils de gestion des packages standard de votre distribution Linux.  

Si vous utilisez un environnement Linux dans vos solutions \(CI/CD\) d’intégration et de remise en continu, vous pouvez également utiliser le pilote Microsoft Edge sur Linux.  Pour commencer à automatiser Microsoft Edge Dev avec le pilote Microsoft Edge, accédez à la [page de téléchargements de pilotes Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Pour obtenir de l’aide sur l’automatisation de Microsoft Edge Dev avec le pilote Microsoft Edge, accédez à [utilisation de WebDriver (chrome) pour l’automatisation des tests][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools dans Microsoft Edge sur Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools dans Microsoft Edge sur Linux  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a>Amélioration des conseils de webhint et de plateforme dans l’outil des problèmes  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Un outil open source, [webhint][WebhintMain], fournit des commentaires en temps réel sur les sites web et les pages web locales.  À partir de la [version 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], consultez les commentaires sur le webhint dans l’outil des [problèmes][DevtoolsIssuesIndex].  Il est désormais plus facile de passer en revue les problèmes qui s’affichent dans l’outil de **problèmes** en ajoutant ces catégories.  

*   [Accessibilité][WebhintUserGuideHintsAccessibility]  
*   [Compatibilité][WebhintUserGuideHintsCompatibility]  
*   [Niveau de performance][WebhintUserGuideHintsPerformance]  
*   [Les pièges][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Sécurité][WebhintUserGuideHintsSecurity]  
    
Vous pouvez à présent filtrer les problèmes tiers à l’aide d’une nouvelle case à cocher.  La fonctionnalité de filtre vous aide à masquer les problèmes liés au code de bibliothèques tierces ou d’autres sources.  

Pour vous aider à passer en revue les problèmes détectés par [webhint][WebhintMain], l’outil des**problèmes** affiche désormais ces informations.  

*   Meilleurs extraits de code.  
*   Liens vers d’autres panneaux pertinents.  
*   Liens vers la documentation pour vous aider à résoudre les problèmes rencontrés sur votre site Web.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Outil des problèmes" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Outil des **problèmes**  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a>Les couches composites sont désormais en affichage 3D  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Vous avez désormais la possibilité de visualiser les contenus de **calques** avec les valeurs d’index z et le modèle d’objet du document (DOM).  Cette fonctionnalité vous permet de déboguer sans basculer entre les outils d’[affichage 3D][Devtools3dViewIndex] et de **calques** .  Pour une expérience complète de débogage, [l’affichage 3D et les couches composites sont désormais combinés][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Volet des couches composites" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Volet des **couches composites**  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a>Définitions des variables CSS dans le volet styles  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

Dans le volet **styles** , les [variables CSS][MdnUsingCssCustomProperties] sont désormais liées directement à chaque définition.  Choisissez la variable pour afficher ou modifier facilement la définition de variables CSS.  Dans l’exemple, DevTools affiche les attributs CSS pour `body` l’élément.  Pour afficher la définition de variable pour la `--theme-body-background` variable CSS, effectuez ces actions.  

1.  Dans le volet **styles** , choisissez `var(--theme-body-background)` .  
1.  Le volet **styles** affiche désormais la définition de la variable CSS `--theme-body-background`.  
    
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

## <a name="service-worker-debugging-improvements"></a>Améliorations du débogage du worker du service  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Ces nouvelles fonctionnalités dans les outils [réseau](#network-tool), [application](#application-tool)et [sources](#sources-tool) vous aident à créer votre [PWA][ProgressiveWebAppsIndex].  Si vous éprouvez des difficultés à déboguer votre worker du service, utilisez ces fonctionnalités.  

Le routage de demande affiche les événements de `startup` et de `fetch` basés sur les requêtes réseau exécutées par le biais des workers du service.  Les chronologies sont accessibles à partir de l'outil **Application** ou **Réseau**.  Les chronologies sont utiles lorsque vous avez des problèmes avec les travailleurs de service et que vous voulez afficher si quelque chose ne va pas avec`startup` l'événement`fetch`.  

### <a name="application-tool"></a>Outil de l’application  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Affichez les informations de routage de demande des workers du service avec le nouveau lien **demandes de réseau**.  Pour afficher un contexte supplémentaire lors du débogage du worker du service, procédez comme suit.  

1.  Accédez aux **workers du service**  >  **de l’application**.  
1.  Sélectionnez **demandes de réseau**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Ouvrir l’outil réseau à partir du volet workers du service" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Ouvrir l’outil **réseau** à partir du volet **workers du service**
    :::image-end:::  
    
1.  L’outil **réseau** s’ouvre dans le **tiroir** et affiche toutes les demandes réseau associées au worker du service.  Les requêtes réseau sont filtrées à l’aide de `is:service-worker-intercepted`.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Outil réseau dans un tiroir" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Outil **réseau** dans un **tiroir**  
    :::image-end:::
    
1. Pour rétablir le panneau supérieur de l’outil **réseau** , fermez le **tiroir**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Fermer le tiroir pour renvoyer l’outil réseau" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Fermez le **tiroir** pour renvoyer l’outil **réseau**.  
    :::image-end:::  
    
### <a name="network-tool"></a>Outil réseau  

Déboguer les requêtes réseau qui s’exécutent par le biais des workersdu service.  Vous pouvez également ouvrir des requêtes réseau à partir de l’outil de **l’application**.  Pour chaque demande, DevTools affiche ces informations dans le volet [chronométrage][DevtoolsNetworkReferenceViewTimingBreakdownRequest].  

*   Le début d’une demande et la durée du démarrage.  
*   Modification apportée à l’inscription du worker du service.  
*   Exécution d’un gestionnaire d’événements `fetch`.  
*   Exécution de tous les événements `fetch` de chargement d’un client.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Volet chronométrage" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Volet **chronométrage**  
:::image-end:::  

### <a name="sources-tool"></a>Outil sources  

Dans les versions précédentes de Microsoft Edge, le niveau de profondeur de la pile d’appels était limité au code JavaScript de votre worker du service.  Dans Microsoft Edge 88, la pile d’appels affiche désormais l’initiateur de demandes qui s’exécutent par le biais de votre worker du service.  

Pour localiser l’initiateur de la requête, utilisez la pile d’appels de votre code JavaScript dans le worker du service.  La pile d’appels dans ces illustrations commence par le code JavaScript de votre worker du service et affiche une référence à la demande de page Web d’origine en tant que `(index):157`.  Dans la deuxième illustration, la référence est choisie et a ouvert l’initiateur qui a créé la demande.  Dans la deuxième illustration, l’initiateur est la page web.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Le fichier service-worker.js et la mise en surbrillance de la pile d’appels nécessitent un émetteur." lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         Le fichier `service-worker.js` et la mise en surbrillance de la pile d’appels nécessitent un émetteur.   
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La page web (index) est l’initiateur de la requête" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         La page web `(index)` est l’initiateur de la requête  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a>Copier la valeur de la propriété d’une demande réseau  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

Dans l’outil **réseau** , copiez la valeur de la propriété d’une demande réseau à l’aide de la nouvelle option **copier la valeur**.  La valeur de la propriété est copiée en tant que valeur JSON décodée.  Dans les versions précédentes de Microsoft Edge, vous deviez copier une valeur à l’aide de l’une de ces actions.  

*   Mettez en surbrillance l’intégralité du texte et copiez-le.  
*   Stockez la valeur en tant que variable globale, le cas échéant, puis copiez-la à partir de la [console][DevtoolsConsoleIndex]DevTools.  
    
Pour copier la valeur de la propriété dans le presse-papiers, accédez à [copier la valeur JSON de la réponse mise en forme dans le presse-papiers][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source Chromium, accédez à la section problème [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copier la valeur de la propriété dans DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Copier la valeur d'une propriété dans DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Coller la valeur d'une propriété dans Microsoft Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Coller la valeur d'une propriété dans Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a>Personnaliser les raccourcis clavier multi-presses  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Depuis la version 87 de Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], vous pouvez personnaliser les raccourcis clavier pour n’importe quelle action dans DevTools.  Dans la version 88 de Microsoft Edge, vous pouvez désormais créer des raccourcis clavier à plusieurs clics.  Pour définir un raccourci vers une action dans la DevTools, accédez à [paramètres][DevtoolsCustomizeIndexSettings] > **expérimentations** et cochez la case en regard de **activer l’éditeur de raccourcis clavier**.  Pour plus d’informations sur la personnalisation et la modification des raccourcis, accédez à [activer la fonctionnalité expérimentale de l’éditeur de raccourcis clavier][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Par exemple, la mise en surbrillance rouge affiche un raccourci clavier à plusieurs clics personnalisé pour l’action **commencer l’enregistrement des événements**.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez à [problème #174309][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Raccourcis clavier des cordes" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Raccourcis clavier à plusieurs clics  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a>DevTools correspond désormais à la langue du navigateur  

Dans Microsoft Edge version 87, si vous activiez le paramètre **respecter la langue du navigateur** dans [paramètres DevTools][DevtoolsCustomizeIndexSettings], DevTools ne correspondait pas à la langue du navigateur.  Dans Microsoft Edge version 88, DevTools correspond désormais à la langue du navigateur si vous activez le paramètre **respecter la langue du navigateur**.  Pour plus d’informations sur le paramètre **respecter la langue du navigateur** DevTools, accédez à [modifier les paramètres de langue DevTools][DevtoolsCustomizeLocalization].  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Faire correspondre le paramètre DevTools de la langue du navigateur au japonais" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   **Faire correspondre la langue du navigateur**relative au paramètre DevTools au japonais  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a>Annonces du projet de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a>Nouveaux outils de visualisation d’angle CSS  

DevTools dispose désormais d’une meilleure prise en charge du débogage d’angle CSS.  Lorsqu’un élément HTML de votre page est doté d’un angle CSS appliqué, une icône d’horloge s’affiche à côté de l’angle dans l’outil **styles**.  Pour activer ou désactiver la superposition de l’horloge, sélectionnez l’icône d’horloge.  Pour modifier l’angle, sélectionnez un emplacement quelconque dans l’horloge ou faites glisser l’aiguille.  Pour modifier la valeur de l’angle, vous pouvez également utiliser la souris et les raccourcis clavier.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [1126178][CR1126178] et [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

Cet angle CSS est utilisé pour l’exemple.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Angle CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Angle CSS  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a>Simuler une taille de quota de stockage dans le volet stockage  

Vous pouvez à présent remplacer la taille de quota de stockage dans le volet **stockage**.  Cette fonctionnalité permet de simuler différents appareils et de tester le comportement de votre site web ou de votre application dans des scénarios de disponibilité du disque faible.  Pour simuler le quota de stockage, effectuez ces actions.  

1.  Accédez au **stockage** > **de l’application**.  
1.  Activez la case à cocher **simuler le quota de stockage personnalisé**.  
1.  Entrez un numéro valide.  
    
Pour plus d’informations sur la façon d’émuler des appareils mobiles et d’autres fonctionnalités dans le DevTools, accédez à la section [émuler des appareils mobiles dans Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [945786][CR945786] et [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simuler la taille de quota de stockage" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simuler la taille de quota de stockage  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a>Signaler les erreurs CORS dans l’outil réseau  

Évaluez cette fonctionnalité en accédant à [version de démonstration d’erreur CORS][GlitchCorsErrors].  Ouvrez l’outil de **réseau** , actualisez la page et observez la requête de réseau CORS ayant échoué.  La colonne état affiche **l’erreur CORS**.  Lorsque vous placer le curseur sur l’erreur, l’info-bulle affiche maintenant le code d’erreur.  Dans la version 87 et les versions antérieures de Microsoft Edge, DevTools affichait uniquement le statut générique **(échec)** pour les erreurs CORS.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de chrome, accédez au problème [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erreurs CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Erreurs CORS  
:::image-end:::  

### <a name="frame-details-view-updates"></a>Mises à jour de l’affichage des détails du cadre  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a>Informations d’isolation de l’origine croisée dans l’affichage des détails du cadre  

L’état isolé de l’origine croisée s’affiche désormais sous la section **sécurité & isolation**.  La nouvelle section **disponibilité de l’API** affiche la disponibilité de (SAB \) `SharedArrayBuffer` et si les mémoires tampons pourraient être partagées en utilisant `postMessage()`.  Un avertissement de dépréciation s’affiche si le SAB et `postMessage()` sont actuellement disponibles, mais que le contexte n’est pas isolé par origine croisée.  Pour plus d’informations sur l’isolement entre les origines et sur les raisons de leur nécessité comme `SharedArrayBuffers` , accédez à [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informations sur l’origine croisée" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Informations sur l’origine croisée  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a>Nouvelles informations des travailleurs web dans l’affichage des détails du cadre  

DevTools organise désormais les travailleurs web sous le cadre du parent approprié.  Par exemple, si le cadre `someName` crée `worker.js` , `worker.js` s’affiche sous `someName` dans la liste des **cadres**.  Pour afficher les détails du travailleur web, effectuez ces actions.  

1.  Ouvrir l’outil de **l’application**.  
1.  Développer un cadre qui contient des travailleurs web.  
1.  Développer l’arborescence **travailleurs**.  
1.  Choisir un travailleur.  
    
Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [1122507][CR1122507] et [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informations sur les travailleurs web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Informations sur les travailleurs web  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a>Afficher les détails d’un cadre ouvrant pour les fenêtres ouvertes  

DevTools organise désormais les [fenêtres][MdnWindowConstructors] ouvertes sous le [cadre][MdnWindowFrames]parent approprié.  Par exemple, si le cadre `top` ouvre une `Window` à `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , la `Window` s’affiche sous `top` dans la liste des **cadres** .  

Pour afficher le cadre responsable de l’ouverture d’une autre fenêtre dans l’outil des **éléments** , effectuez ces actions.  

1.  Ouvrez l’arborescence des **cadres**.  
1.  Développez les**fenêtres ouvertes** et choisissez le `Window` pour le cadre parent que vous voulez connaître.  
1.  Sélectionnez le lien du **cadre d’ouverture**.  

Les détails sur le cadre à l’origine de l’ouverture d’une autre `Window` sont affichés.  Pour afficher la l’élément responsable de l’ouverture dans l’outil **éléments** , effectuez ces actions..  

1.  Ouvrez l’arborescence des **cadres**.  
1.  Choisissez une fenêtre ouverte pour ouvrir les détails de `Window`.  
1.  Sélectionnez le lien du **cadre d’ouverture**.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Informations de cadre ouvert" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Informations de cadre ouvert  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a>Copier le StackTrace pour l’initiateur réseau  

Pour copier le StackTrace dans le presse-papiers, effectuez ces actions.  

1.  Ouvrez le menu contextuel \(cliquez avec le bouton droit\).  
1.  Choisissez **copier**le  >  **StackTrace**.  
    
Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copier le StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Copier le StackTrace  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a>Afficher un aperçu de la valeur de la variable WASM sur mouseover  

Utilisez cette fonction pour afficher un aperçu de la valeur d’une variable webassembly \(WASM \) lorsque votre code est en pause.  Pour afficher la valeur actuelle d’une variable, pointez sur une variable.  Pour consulter les mises à jour en temps réel de cette fonctionnalité dans le projet open-source de Chromium, accédez aux problèmes [1058836][CR1058836] et [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Afficher un aperçu de la variable WASM sur mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Afficher un aperçu de la variable WASM sur mouseover  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a>Unités de mesure cohérentes pour la taille des fichiers et de la mémoire  

Désormais DevTools utilise `kB` pour l’affichage des tailles de fichiers et de mémoire.  Auparavant DevTools combinait `kB` et `KiB` .

*   `kB` ou kilo-octets \(10^3 ou 1000 octets \)  
*   `KiB` ou kibibyte \(2^10 ou 1024 octets \)  
    
Par exemple, l’outil **réseau** utilisait `kB` dans les étiquettes, mais utilisait `KiB` dans les calculs.  Votre commentaire a démontré que cette incohérence a causé une confusion.  Pour passer en revue l’historique de cette fonctionnalité dans le projet open-source de Chromium, accédez au problème [1035309][CR1035309].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Téléchargez les canaux de l'aperçu de Microsoft Edge  

Si vous êtes sous Windows, Linux ou macOS, envisagez d'utiliser les [canaux d'aperçu de Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.  Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Affichage 3D | Documents Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Présentation de la console | Documents Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Modifier les paramètres de langue de DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Activer l’éditeur de raccourcis clavier-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activer les couches composites dans l’affichage 3D - fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copier la valeur JSON de la réponse mise en forme dans le presse-papiers - référence d’analyse du réseau | Documents Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Afficher la répartition du chronométrage d’une demande - référence d’analyse du réseau | Documents Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Utiliser le WebDriver (Chromium) pour l’automatisation des tests | Documents Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Applications web progressives sur Windows | Documents Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: ../10/devtools.md#customize-keyboard-shortcuts-in-settings "Personnaliser les raccourcis clavier dans les paramètres - nouveautés de DevTools (Microsoft Edge 87) | Documents Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: ../06/devtools.md#webhint-feedback-in-the-issues-panel "Commentaires sur les webhint dans le panneau des problèmes - nouveautés de DevTools (Microsoft Edge 85) | Documents Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Télécharger WebDriver | Développeur Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Télécharger les canaux Microsoft Edge Insider"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canaux d’aperçu Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Code Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR174309]: https://crbug.com/174309 "Problème 174309: DevTools: Autoriser la personnalisation des raccourcis clavier/les combinaisons de touches | Bogues Chromium"  
[CR945786]: https://crbug.com/945786 "Problème 945786: DevTools: Autoriser le remplacement de navigator.storage.estimate() | Bogues Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problème 1029427: Réduire la surcharge des performances de l’envoi de messages de protocole frontal | Bogues Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problème 1035309: DevTools doit utiliser de manière cohérente Mo pour signifier mégaoctets, pas mebibyte | Bogues Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problème 1051466: Prendre en charge le débogage COOP/COEP dans DevTools | Bogues Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problème 1058836: Problèmes UX liés au débogage de WASM | Bogues Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problème 1071432: ☂️ Experience de développeur de base WASM | Bogues Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problème 1107766: Affichez des informations sur les cadres générées par ’window.open()' dans l’arborescence de cadre | Bogues Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problème 1122507: Informations sur le travailleur de surface dans l’affichage de l’arborescence de cadre | Bogues Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problème 1126178: ☂ DevTools: CSS <type> composants | Bogues Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problème 1130556: DevTools: tester l’image de retour (émulation) | Bogues Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problème 1132084: il n’y a pas de moyen simple de copier la charge utile de la requête JSON | Bogues Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problème 1136394: outils Flexbox | Bogues Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problème 1138633: DevTools: CSS <angle> le composant doit refléter son apparence de propriété dans l’arrière-plan d’horloge | Bogues Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problème 1139615: L’initiateur réseau doit permettre de copier le rapport des appels de procédure | Bogues Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problème 1139899: Signaler la disponibilité des API contrôlées dans l’affichage des détails du cadre | Bogues Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problème 1139945: icônes des propriétés CSS de Flexbox dans le panneau styles | Bogues Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problème 1141824: améliorer le signalement des erreurs CORS dans DevTools | Bogues Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problème 1144090: Ajouter des ornements de style flex à l’arborescence des éléments | Bogues Chromium"  
[CR1146985]: https://crbug.com/1146985 "Problème 1146985: le texte supprimé reste affiché dans le champ de texte de la section «stockage» de la fenêtre « outils de développement » | Bogues Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erreurs CORS | Problème"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Partage de ressources d’origine croisée (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Utilisation des propriétés personnalisées CSS (variables) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructeurs - fenêtre | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accessibilité | Webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilité | Webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Performance | Webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Pièges | Webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | Webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sécurité | Webhint"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/11/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
