# Documentation MicrosoftEdge

## Code de réalisation Microsoft Open source

Ce projet a adopté le [Code de réalisation Microsoft Open source](https://opensource.microsoft.com/codeofconduct/).
Pour plus d’informations, consultez le [Forum aux questions](https://opensource.microsoft.com/codeofconduct/faq/) ou contactez [opencode@microsoft.com](mailto:opencode@microsoft.com) pour obtenir d’autres questions ou commentaires.

## Informations légales
Microsoft ainsi que tout contributeur vous octroient une licence sur la documentation de Microsoft et d’autres contenus de ce référentiel en vertu de la [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode), voir le fichier [LICENSE](LICENSE), et vous octroient une licence pour tout code du référentiel, en vertu de la [MIT License](https://opensource.org/licenses/MIT), voir le fichier [LICENSE-CODE](LICENSE-CODE).

Microsoft, Windows, MicrosoftAzure et/ou d’autres produits et services Microsoft référencés dans la présente documentation peuvent être des marques commerciales ou déposées de MicrosoftCorporation aux États-Unis et/ou dans d’autres pays.
Les licences de ce projet ne vous accordent aucun droit d'utilisation des noms, des logos ou des marques de Microsoft.
Les recommandations générales de marque Microsoft sont disponibles à l’adresse https://go.microsoft.com/fwlink/?LinkID=254653 .

Les informations sur la confidentialité se trouvent surhttps://privacy.microsoft.com

Microsoft et tout contributeur se réserve tous les autres droits, en vertu de leurs droits d’auteur, de leurs brevets, ou de leurs marques commerciales respectives, qu'ils soient implicites, par préclusion ou de toute autre manière.

## Cargaison

Il s’agit du référentiel de la **documentation** Microsoft Edge hébergée à l’adresse [https://docs.microsoft.com/microsoft-edge/](https://docs.microsoft.com/microsoft-edge/) .

Si vous souhaitez consulter une nouvelle couverture ou avoir des commentaires, [**veuillez envisager de**](/CONTRIBUTING.md)faire des commentaires.  Vous pouvez modifier le contenu existant, ajouter du contenu ou créer de nouveaux [problèmes](https://github.com/MicrosoftDocs/edge-developer/issues). Nous allons examiner vos suggestions et collaborer pour les incorporer dans les documents.

Recherchez les données pour la [`Status`](https://dev.windows.com/microsoft-edge/platform/status/) page sur: https://github.com/MicrosoftEdge/Status . La `Status` page fournit la dernière version de l’état de l’implémentation et des offres futures pour les fonctionnalités de plateforme Web dans Microsoft Edge.

### Régissant

- Lors de l’ajout d’une page, vous devez ajouter une entrée pour celle-ci dans [toc.MD](microsoft-edge/toc.md) pour qu’elle apparaisse.
- Un dossier peut contenir plus de dossiers ou `readme.md` s
- Les noms de dossiers/répertoires sont séparés par des tirets (par exemple, `f12-tools` et en minuscules). Ils sont utilisés dans les URL du site docs.microsoft.com. N’utilisez pas de tirets ou de PascalCase/camelCase.

### Autres éléments de texte

Il existe d’autres éléments de texte avec un style:

* Listes non ordonnées
* Utiliser des puces normales
   * Vous pouvez également imbriquer des puces.
   * Les listes à puces doivent comporter plusieurs entrées.
* Très standard

1. Listes triées.
2. Utiliser une numérotation de type occidental (Western) standard.
3. Ne doit être utilisé que lorsqu’une liste est réellement commandée.

_________________________

Des règles horizontales sont disponibles. Nous vous suggérons de les utiliser avec parcimonie pour réduire l’encombrement.
Ne pas combiner les règles horizontales et les balises de titre; certains styles de lignes déjà utilisés pour la hiérarchie visuelle.

### Affichage du code

Vous pouvez utiliser `code` la syntaxe de la marque incluse (avec les battements).

Vous pouvez aussi afficher des blocs de code comme suit:

```css
body {
    background: #fff;
}
```

### Contenu

| Vous pouvez     | utiliser les en-têtes | dans des tables    |
|-------------|-------------|-------------:|
| Aligné à gauche| Sauf si un #  | 456          |
| Valeur de texte  | Davantage de texte   | $0,00        |

### Remarques

Utilisez les notes avec parcimonie. Il s’agit de blocs destinés à mettre en évidence les informations «ne pas manquer».

Il existe quatre versions différentes de notes actuellement stylisées:
- REMARQUE
- AVERTISSEMENT
- EXTREM
- IMPORTANT

Il ressemble respectivement aux éléments suivants:

![Modèles de notes](./media/notes.png)

```
> [!WARNING]
> Hello. Yes. I am a warning note that has been automagically created. My text may wrap to more than one line when the Markdown is parsed, but I must include all my information within a single (sometimes very long line) in the Markdown itself.```

For multi-line blockquote notes, use a > in front of each line of the notes as seen in the example below.

```


### Images

Les images doivent être stockées dans un `media` dossier et référencées à l’aide d’un chemin d’accès relatif:

`![Note patterns](media/notes.png)`
