# JobBot Comptabilité — Site de présentation

**Site public de présentation uniquement.** Le bot Python, les CV et les clés API restent sur votre Mac, dans un dossier distinct et privé.

## Publication depuis GitHub.com (sans logiciel supplémentaire)

1. Connectez-vous à https://github.com/ et cliquez sur **New repository**.
2. Donnez-lui le nom exact **`jobbot-comptabilite`** (ou choisissez un nom libre). Sélectionnez **Public** et créez le dépôt.
3. Dans le dépôt, choisissez **Add file > Upload files**.
4. Glissez-y les fichiers **`index.html`**, **`.nojekyll`** et **`.gitignore`** de CE dossier (pas l'archive du bot), puis cliquez **Commit changes**.
5. Ouvrez **Settings > Pages**.
6. Sous **Build and deployment**, choisissez **Deploy from a branch** ; branche **main** ; dossier **/(root)** ; puis **Save**.
7. GitHub affichera l'adresse publique de votre site après publication, typiquement :
   `https://VOTRE_PSEUDO.github.io/jobbot-comptabilite/`
8. Ouvrez ce lien dans un navigateur et assurez-vous qu'il fonctionne avant de le transmettre à Adzuna.

> Attention : les dépôts publics sont visibles par tous. Ne téléversez **jamais** `JobBot_Comptabilite_V2_72h.zip`, le dossier complet du bot, vos CV, `.env`, vos clés API ni vos coordonnées personnelles dans ce dépôt.

Guide officiel : https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Inscription Adzuna

Inscription : https://developer.adzuna.com/signup

- **Organisation/Group Name** : `JobBot Comptabilité — Projet personnel`
- **Organisation/Group website** : l'adresse GitHub Pages *réellement publiée*
- **Your application of the Adzuna API** : `Personal job search` (si proposé dans la liste)
- **Average Monthly Visitors** : `0` ou la plus petite catégorie disponible
- **Primary Geographic Market** : `Canada`
- **Primary Industry** : `Technology / Software` (si proposé, champ facultatif)

Adzuna fournit les clés API après inscription, selon ses règles et quotas. Les identifiants `app_id` et `app_key` doivent être stockés **uniquement** dans le fichier `.env` du bot local, jamais sur GitHub.

Dans votre dossier local `jobbot_comptabilite_v2` :

```bash
open -e .env
```

Renseignez les valeurs réelles dans les champs `ADZUNA_APP_ID` et `ADZUNA_APP_KEY`, puis :

```bash
source .venv/bin/activate
python jobbot.py scan
```

Si `.env` n'existe pas encore : `cp .env.example .env`.

## Ce que contient le site

Une page d'information statique, responsive et bilingue (français / résumé anglais), sans cookies, formulaire, service tiers ni stockage de données. Elle **ne fait pas tourner le bot**. Elle sert seulement de présentation publique du projet.

## Version

9 novembre 2026.