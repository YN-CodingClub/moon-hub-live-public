# Automation SEO

Catalogue Streamlit public des outils SEO suivis dans Automation SEO.

## Version live

Cette version est volontairement cloud-safe :

- pas de lancement de processus local ;
- pas de port `localhost` ;
- pas de PID ;
- pas de dependance au poste local.

## Deploiement Streamlit Community Cloud

- Repository : `YN-CodingClub/moon-hub-live-public`
- Branch : `main`
- Main file path : `streamlit_app.py`
- App URL : `automation-seo`

URL cible :

```text
https://automation-seo.streamlit.app/
```

## Mode single URL

Streamlit Community Cloud expose une app par URL. Pour que tous les outils soient disponibles depuis `automation-seo.streamlit.app`, le modele robuste est :

1. `automation-seo.streamlit.app` sert de hub public.
2. Chaque outil metier est publie comme app Streamlit separee.
3. Le hub reference les apps metier via `live_url` dans `projects.json`.

Integrer tout le code dans une seule app est possible seulement apres consolidation des dependances, secrets et chemins locaux outil par outil.

## Ajouter une URL live

Ajouter `live_url` dans `projects.json` sur l'outil concerne :

```json
"live_url": "https://example.streamlit.app"
```
