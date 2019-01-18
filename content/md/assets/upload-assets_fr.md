---
id: upload-assets
themes: manage-your-assets, import-export-data
title: "**Charger** des ressources numériques"
popular: false
ee-only: true
related: work-with-assets, assets-transformation
---


# Aperçu
Le chargement en masse des ressources numériques est particulièrement utile si vous voulez mettre à jour votre catalogue avec des sources externes: shooting photo, nouvelle collection, etc.

Le PIM utilise le nom du fichier pour savoir pour quelle ressource le fichier doit être utilisé et si cette ressource est localisée ou pas.

**Exemple 1 avec une ressource non-localisable**
Si le nom de fichier est `image_principale_S1263547.jpg`, alors le PIM va vérifier:
- Si la ressource qui porte le code `image_principale_S1263547` existe déjà, le PIM va mettre à jour cette ressource en important le fichier image en tant que fichier de référence (et va regénérer les fichiers de variations correspondants).
- Si la ressource n’existe pas encore, le PIM va créer une nouvelle ressource portant le code `image_principale_S1263547` avec l’image en tant que fichier de référence, de sorte que les fichiers de variations puissent être générés.

**Exemple 2 avec un média localisable**
Si le nom de fichier est « akene-en_US.pdf », alors le PIM va vérifier:
- Si la ressource qui porte le code `akene` existe déjà et si elle est localisable, le PIM va mettre à jour la ressource portant le code `akene` en important le fichier `akene-en_US.pdf` en tant que fichier de référence pour la locale donnée (code de la locale à la fin du nom du fichier: ici `en_US`).
- Si la ressource portant le code `akene` existe déjà mais qu’elle n’est pas localisable, le PIM affichera un message d’erreur en rouge.
- Si la ressource portant le code `akene` n’existe pas encore, le PIM va créer une nouvelle ressource localisable ayant pour code `akene` et pour fichier de référence de la locale donnée, le fichier PDF. (Code de la locale à la fin du nom du fichier: ici `en_US`)

:::warning
Si la locale est désactivée ou n’existe pas dans le PIM, le PIM affichera un message d’erreur en rouge.
:::

# Comment faire?

1. Allez dans le menu des ressources numériques.
1. Cliquez sur le bouton `...` en haut à droite de l’écran, et sélectionnez `Charger des ressources numériques`
1. Glissez et déposez vos fichiers dans cette page ou cliquez sur `Cliquez et déposez vos ressources numériques ou cliquez ici` pour ouvrir la fenêtre de dialogue et sélectionnez les fichiers que vous voulez charger
1. Cliquez sur le bouton `Charger les ressources numériques` pour les charger dans le PIM.
1. Une fois que les fichiers sont chargés, cliquez sur le bouton `Importer` pour créer les ressources numériques dans le PIM.

Le compte rendu de l’import est affiché.

![video](../videos/chargement-ressources-FR.mp4)

::: info
Quand des fichiers sont ajoutés à la liste, vous pouvez les retirer peu importe leur statut.
Pour supprimer le fichier de la liste, cliquez sur le bouton `X` à droite de chaque ligne. Le fichier sera supprimé et ne sera pas importé.

Si vous voulez supprimer tous les fichiers que vous avez ajoutés, cliquez sur le bouton `Supprimer tous les fichiers` en haut de l’écran. ;)
:::