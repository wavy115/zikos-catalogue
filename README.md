# Catalogue ZIKOS

Ce dépôt contient **un seul fichier qui compte** : [`manifest.json`](manifest.json).
C'est la source du catalogue pour tous les ZIKOS Launcher installés.

## Pourquoi ce dépôt est séparé du code

Le dépôt du code (`zikos-launcher`) est **privé**. Or les launchers installés chez les
utilisateurs doivent pouvoir lire le manifeste **sans authentification** : un dépôt privé
renverrait une erreur 404.

Ce dépôt-ci est donc **public**, mais il ne contient que le catalogue — jamais le code source.

> Si un jour tu rends `zikos-launcher` public, tu pourras fusionner les deux et n'en garder qu'un.

## Le flux

```
ZIKOS Studio  →  Exporter manifest.json (ici)  →  git push
                                                     ↓
                          tous les launchers se mettent à jour tout seuls
```

## La règle d'or

Le Studio **incrémente `catalogVersion` automatiquement** à chaque export. C'est ce numéro
qui déclenche la mise à jour chez les utilisateurs. N'y touche pas à la main.

## Publier une mise à jour

```bash
cd C:\Users\3arcw\Desktop\zikos-catalogue
git add .
git commit -m "catalogue : ajout de ..."
git push
```

L'URL lue par les launchers :
`https://raw.githubusercontent.com/wavy115/zikos-catalogue/main/manifest.json`

## Périmètre

Uniquement du contenu **libre de droits** (open-source, freeware, Creative Commons) ou que tu
**possèdes et distribues légalement**.
