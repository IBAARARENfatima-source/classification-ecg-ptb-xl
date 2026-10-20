# Classification de signaux ECG (PTB-XL)

Projet académique réalisé en équipe pour classer les enregistrements ECG à 12 dérivations de PTB-XL en cinq catégories diagnostiques. Le dépôt contient le notebook d'entraînement et d'évaluation, sans les données ni les poids des modèles.

## Équipe

- [Fatima IBAARAREN](https://github.com/IBAARARENfatima-source)
- [Aya Nasser (@ayanasser53)](https://github.com/ayanasser53)

## Méthode

- Prétraitement des signaux : filtre passe-bande Butterworth de 0,5 à 40 Hz et normalisation de chaque dérivation.
- Séparation selon les plis `strat_fold` de PTB-XL : pli 8 pour la validation et plis 9-10 pour le test ; pondération des classes pendant l'entraînement.
- Entraînement et comparaison de cinq architectures : CNN 1D, CNN optimisé, BiLSTM, CNN-BiLSTM et ResNet1D.
- Évaluation sur le jeu de test : accuracy, F1-score, rapport de classification, courbes d'apprentissage et matrices de confusion. Le notebook contient les graphiques, mais aucune performance chiffrée n'est annoncée ici sans réexécution.

## Données et exécution

Le fichier `classification-ecg-ptb-xl.ipynb` a été conçu pour Kaggle. Il recherche `ptbxl_database.csv`, `scp_statements.csv` et les enregistrements ECG sous `/kaggle/input`. Ajoutez le jeu de données [PTB-XL](https://physionet.org/content/ptb-xl/) avant de l'exécuter. Les données et les modèles entraînés ne sont pas inclus dans ce dépôt.

Les sorties d'exécution ont été retirées pour alléger le dépôt et une cellule de visualisation a été replacée après la préparation des données. Les résultats ne sont pas recalculés ici ; aucune application Streamlit n'est fournie dans ce dépôt.

Ce projet est une démonstration de recherche et ne constitue pas un outil de diagnostic médical.
