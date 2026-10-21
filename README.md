# Violet Password : versions

Ce dépôt public ne contient que les installateurs **signés** de Violet Password et leur fichier `latest.json`,
lus par la mise à jour automatique de l'application. Le code est dans un dépôt privé.

- Chaque dossier `versions/<version>/` contient l'installateur Windows, sa signature `.sig` et `latest.json`.
- Le workflow `.github/workflows/publier.yml` en fait une release `v<version>` marquée « Latest ».
- L'application ne télécharge que `releases/latest/download/latest.json`, puis l'installateur qu'il désigne, et
  refuse tout fichier qui n'est pas signé par la clé de Violet Password (la clé privée n'est jamais sur GitHub).

Pour installer à la main : page **Releases**, dernière version, fichier `Violet-Password_<version>_x64-setup.exe`.
