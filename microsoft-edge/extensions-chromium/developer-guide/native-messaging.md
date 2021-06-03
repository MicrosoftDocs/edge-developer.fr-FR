---
description: Documentation sur la messagerie native
title: Messagerie native
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: e6233289794bc1c3ef235af46402c23173c09857
ms.sourcegitcommit: e6a4f73be57439149e3cc56491d7364831d0079e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "11475210"
---
# <a name="native-messaging"></a>Messagerie native  

Les extensions communiquent avec une application Win32 native installée sur l’appareil d’un utilisateur à l’aide des API de transmission de message.  L’hôte d’application natif envoie et reçoit des messages avec des extensions à l’aide de l’entrée standard et de la sortie standard.  Les extensions utilisant la messagerie native sont installées dans Microsoft Edge comme n’importe quelle autre extension.  Toutefois, les applications natives ne sont pas installées ou gérées par Microsoft Edge.  

Pour acquérir l’extension et l’hôte d’application native, vous avez deux modèles de distribution.  

*   Rassemblez votre extension et l’hôte.  Lorsqu’un utilisateur installe le package, l’extension et l’hôte sont installés.  
*   Installez votre extension à [l’Microsoft Edge du][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]magasin d’extensions et votre extension invite les utilisateurs à installer l’hôte.  

Pour créer votre extension pour envoyer et recevoir des messages avec des hôtes d’application natifs, complétez les étapes suivantes.  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a>Étape 1 : ajouter des autorisations au manifeste d’extension  

Ajoutez `nativeMessaging` l’autorisation au **manifest.jssur le** fichier de l’extension.  L’extrait de code suivant est un exemple ** d'manifest.jssur**.  

```json
{
    "name": "Native Messaging Example",
    "version": "1.0",
    "manifest_version": 2, 
    "description": "Send a message to a native app.",
    "app": { 
        "launch": { 
            "local_path": "main.html" 
        } 
    }, 
    "icons": { 
        "128": "icon-128.png"
    }, 
    "permissions": ["nativeMessaging"] 
}
```  

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a>Étape 2 : créer votre fichier manifeste d’hôte de messagerie native  

Les applications natives doivent fournir un fichier manifeste d’hôte de messagerie native.  Le fichier manifeste contient les informations suivantes.  

*   Chemin d’accès au runtime de l’hôte de messagerie native.  
*   Méthode de communication avec l’extension.  
*   Liste des extensions autorisées avec lesquelles il communique.  
    
Le navigateur lit et valide le manifeste d’hôte de messagerie native.  Le navigateur n’installe pas ou ne gère pas le fichier manifeste de l’hôte de messagerie native.  

```json
{
    "name": "com.my_company.my_app",
    "description": "My App",
    "path": "C:\\Program Files\\My App\\chrome_native_messaging_host.exe",
    "type": "stdio",
    "allowed_origins": [
        "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

Le fichier manifeste hôte doit être un fichier JSON valide qui contient les clés suivantes.  

:::row:::
   :::column span="1":::
      **Clé**  
   :::column-end:::
   :::column span="3":::
      **Détails**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Spécifie le nom de l’hôte de messagerie natif.  Les clients passent la chaîne à `runtime.connectNative` ou `runtime.sendNativeMessage` .  
      
      *   La valeur ne doit contenir que des caractères alphanumériques en minuscules, des traits de soulignement et des points.  
      *   La valeur ne doit pas commencer ou se terminer par un point et un point ne doit pas être suivi d’un autre point.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Décrit l’application.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Spécifie le chemin d’accès au fichier binaire hôte de messagerie native.  
      
      *   Sur Windows, vous pouvez utiliser des chemins d’accès relatifs au répertoire qui contient le fichier manifeste.  
      *   Sur macOS et Linux, le chemin d’accès doit être absolu.  
          
      Le processus hôte commence par le répertoire actuel qui contient le fichier binaire hôte.  Par exemple, \(Windows\), si le paramètre est paramétrable, le fichier binaire est démarré à l’aide du répertoire `C:\App\nm_host.exe` actuel \( `C:\App\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Spécifie le type de l’interface utilisée pour communiquer avec l’hôte de messagerie natif.  La valeur indique Microsoft Edge utiliser `stdin` et communiquer avec `stdout` l’hôte.  
      La seule valeur acceptable est `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      Spécifie la liste des extensions qui ont accès à l’hôte de messagerie natif.  Pour activer votre application afin d’identifier et de communiquer avec une extension, dans votre fichier manifeste hôte de messagerie native, définissez la valeur suivante.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Chargez une version test de votre extension pour tester la messagerie native avec l’hôte.  
Pour recharger une version de votre extension pendant le développement et `microsoft_catalog_extension_id` récupérer, complétez les actions suivantes.  

1.  Accédez à , puis activer le bouton bascule `edge://extensions` du mode développeur.  
1.  Choisissez **Charger décompressé,** puis choisissez votre package d’extension à charger de côté.  
1.  Choisissez **OK**.  
1.  Accédez à `edge://extensions` la page et vérifiez que votre extension est répertoriée.  
1.  Copiez la clé à partir `microsoft_catalog_extension_id` de \(ID\) à partir de la liste des extensions sur la page.  
    
Lorsque vous êtes prêt à distribuer votre extension aux utilisateurs, publiez-la dans le magasin Microsoft Edge de modules.  L’ID d’extension de l’extension publiée peut différer de l’ID utilisé lors du chargement de votre extension.  Si l’ID a changé, mettez à jour dans le fichier manifeste hôte avec `allowed_origins` l’ID de votre extension publiée.  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a>Étape 3 : copier le fichier manifeste de l’hôte de messagerie native dans votre système  

La dernière étape consiste à copier le fichier manifeste de l’hôte de messagerie native sur votre ordinateur et à s’assurer que le fichier manifeste est correctement configuré.  Pour vous assurer que votre fichier manifeste est placé à l’emplacement attendu, complétez les actions suivantes.  L’emplacement varie selon la plateforme.

> [!NOTE]
> Veillez à fournir des autorisations de lecture sur le fichier manifeste et à exécuter les autorisations sur l’runtime hôte.  

### [<a name="windows"></a>Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

Le fichier manifeste peut se trouver n’importe où dans le système de fichiers.  Le programme d’installation de l’application doit créer une clé de Registre et définir la valeur par défaut de la clé sur le chemin d’accès complet du fichier manifeste.  Les emplacements suivants sont des exemples de clés de Registre.  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

Pour ajouter une clé de Registre au répertoire avec la clé de manifeste, effectuer l’une des actions suivantes.  

*   Exécutez la commande dans l’invite de commandes.  
    
    1.  Exécutez la commande suivante.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   Créez `.reg` un fichier et exécutez-le.  
    
    1.  Copiez la commande suivante dans un `.reg` fichier.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Exécutez le `.reg` fichier.  
        
Microsoft Edge interroge la `HKEY_CURRENT_USER` clé racine suivie de `HKEY_LOCAL_MACHINE` .  Dans les deux clés, le Registre 32 bits est recherché en premier, puis le Registre 64 bits est recherché pour identifier les hôtes de messagerie natifs.  La clé de Registre spécifie l’emplacement du manifeste d’hôte de messagerie native.  Si les entrées de Registre pour Microsoft Edge n’ont pas l’emplacement du manifeste hôte, les emplacements de Registre Chromium et Chrome sont utilisés comme options de base.  Si Microsoft Edge trouve la clé de Registre à l’un des emplacements répertoriés précédemment, il n’interroge pas les emplacements répertoriés dans l’extrait de code suivant.  Si vous exécutez votre fichier créé dans le cadre d’un script de commandes, veillez à l’exécuter à l’aide d’une `.reg` invite de commandes d’administrateur.

La liste suivante est l’ordre de recherche pour les emplacements du Registre.  

```output
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\

HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\
```  
 
> [!NOTE] 
> Si vous avez des extensions sur les extensions Microsoft Edge et chrome Webstore, vous devez ajouter les ID d’extension correspondant aux deux magasins dans le fichier manifeste hôte, car seul le manifeste hôte correspondant au premier emplacement de Registre trouvé est `allowed_origins` lu.  

### [<a name="macos"></a>macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Pour stocker le fichier manifeste, effectuer l’une des actions suivantes.  

*   Les hôtes de messagerie native à l’échelle du système, qui sont disponibles pour tous les utilisateurs, sont stockés dans un emplacement fixe.  Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   Les hôtes de messagerie native spécifiques à l’utilisateur, disponibles uniquement pour l’utilisateur actuel, se trouvent dans le sous-répertoire de `NativeMessagingHosts` l’annuaire de profils utilisateur.  Par exemple, le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    `{Channel_Name}` `Microsoft Edge {Channel_Name}` L’in doit être l’une des valeurs suivantes.  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    Lorsque vous utilisez le canal stable, ` {Channel_Name}` cela n’est pas obligatoire.  
    
### [<a name="linux"></a>Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Pour stocker le fichier manifeste, effectuer l’une des actions suivantes.  

*   Les hôtes de messagerie native à l’échelle du système, qui sont disponibles pour tous les utilisateurs, sont stockés dans un emplacement fixe.  Le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Les hôtes de messagerie native spécifiques à l’utilisateur, disponibles uniquement pour l’utilisateur actuel, se trouvent dans le sous-répertoire de `NativeMessagingHosts` l’annuaire de profils utilisateur.  Le fichier manifeste doit être stocké à l’emplacement suivant.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge Modules de modules"

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/nativeMessaging)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
