# Puissance 4 — Classification supervisée de l’issue d’une position

Projet de machine learning par **Ali Houssenaly et Côme Guillarme**, consacré au [jeu de données UCI Connect-4](https://archive.ics.uci.edu/dataset/26/connect+4).

L’objectif est de prédire **victoire, défaite ou match nul pour le premier joueur** à partir d’une position du plateau. Le dépôt étudie la classification de positions étiquetées ; il n’implémente pas un agent de jeu complet.

## Démarche

- Explorer les positions et le déséquilibre des classes.
- Encoder les caractéristiques du plateau en one-hot et les classes cibles lorsque nécessaire.
- Comparer Random Forest, SVM et XGBoost.
- Optimiser les hyperparamètres avec GridSearchCV et comparer les approches sur données initiales et rééchantillonnées.
- Examiner les matrices de confusion et les rapports de classification, notamment le F1 macro et les classes minoritaires.

Le notebook contient la discussion expérimentale et les sorties enregistrées. Les résultats n’ont pas été reproduits indépendamment à l’occasion de cette mise à jour documentaire.

## Contenu

- [Notebook du projet](HOUSSENALY_GUILLARME_Project.ipynb) — méthode, choix entraînement/chargement et évaluation.
- [Présentation vidéo](HOUSSENALY_GUILLARME_Video.mp4) — présentation associée.
- `models/` — modèles Random Forest, SVM et XGBoost enregistrés, avec leurs variantes rééchantillonnées.

## Prise en main

Installer Git LFS avant de cloner le dépôt. Sous Debian/Ubuntu :

```bash
sudo apt install git-lfs
git lfs install
git clone https://github.com/ali-hou-supaero/ML_Connect4_Project.git
cd ML_Connect4_Project
git lfs pull
```

Sur les autres systèmes, installer Git LFS avec l’installateur adapté, puis exécuter `git lfs install` avant le clonage.

Utiliser Jupyter avec Python, ucimlrepo, pandas, NumPy, matplotlib, seaborn, scikit-learn, XGBoost et joblib. Le notebook récupère le dataset UCI 26 avec `fetch_ucirepo` ; un accès réseau est donc nécessaire.

Lancer le notebook depuis la racine du dépôt. Aux invites, choisir d’entraîner ou de charger un modèle ; charger le modèle enregistré suggéré permet d’éviter de relancer la recherche par grille. Charger uniquement des modèles de confiance. Les modèles enregistrés peuvent nécessiter les versions des bibliothèques utilisées lors de leur création ; aucun environnement verrouillé n’est fourni.

## Reproductibilité et crédits

L’analyse est un travail commun. Le développement des modèles, les conclusions et la présentation doivent être attribués aux deux auteurs. La source des données est indiquée par le lien UCI ci-dessus. Le dépôt conserve les expériences originales et ne revendique pas de benchmark nouvellement validé.
