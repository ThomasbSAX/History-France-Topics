# History France Topics

Analyse de publications académiques en histoire avec annotation assistée par LLM pour détecter les contenus liés à la France et extraire des sujets thématiques.

## Auteurs
Projet réalisé avec lazar van berchem et Noam Chabot.

## Contexte
Les méthodes de collecte des données ont été réalisées par un ensemble d’étudiants du CPES Sciences des données, art et culture (Lycée Louis-le-Grand et Université PSL).

Les sources étant hétérogènes (sites, formats, structuration des biographies/publications), les fichiers CSV de départ sont de formats différents et ont nécessité des étapes de nettoyage/standardisation spécifiques.

## Contenu du dépôt
- `history.ipynb` : notebook principal (filtrage + annotation + synthèse thématique)
- `data_history.csv` : données initiales
- `data_history_annoted.csv` : données annotées (`Lien_France`, `Sujet_France`)
- `sujets_history.csv` : extraction des sujets
- `themes_france.png` : visualisation thématique
- `Vietnam_projet/` : continuité du travail (version transmise au professeur), incluant ressources OpenAlex, ressources de thèses et documents de cadrage.

## Continuité du projet
Ce dépôt regroupe volontairement deux volets dans le même dossier pour garder la continuité du travail :
- un volet `History France Topics` (annotation/synthèse autour de la France),
- un volet `Vietnam_projet` (ressources et analyses complémentaires envoyées au professeur).

## Workflow
1. Chargement des publications d’historiens
2. Filtrage des colonnes utiles
3. Annotation LLM locale : présence d’un lien avec la France (`Oui/Non`)
4. Extraction du sujet principal des publications liées à la France
5. Agrégation/synthèse thématique

## Exécution
```bash
pip install -r requirements.txt
jupyter notebook history.ipynb
```

## Dépendance LLM locale
Le notebook peut interroger un endpoint local compatible API OpenAI :
- URL par défaut : `http://localhost:1234/v1/chat/completions`
- Modèle par défaut : `mistralai/mistral-7b-instruct-v0.3`

## Remarques
- Les chemins ont été rendus relatifs pour faciliter la réutilisation.
- Les annotations LLM peuvent contenir du bruit: une vérification manuelle est recommandée pour les analyses finales.
