# Classification de signaux ECG (PTB-XL)

Projet académique réalisé en équipe : comparaison de modèles de deep learning pour classer des ECG à 12 dérivations dans cinq grandes catégories diagnostiques.

## Équipe

- [Fatima IBAARAREN](https://github.com/IBAARARENfatima-source)
- [ayanasser53](https://github.com/ayanasser53)

## Contenu

- `classification-ecg-ptb-xl.ipynb` : chargement des données, filtrage et normalisation, entraînement et évaluation des modèles CNN 1D, BiLSTM, CNN-BiLSTM et ResNet1D.
- Comparaison par accuracy, précision, rappel, F1-score et matrices de confusion.

## Données et exécution

Le notebook a été conçu pour un environnement Kaggle. Il recherche `ptbxl_database.csv`, `scp_statements.csv` et les enregistrements ECG sous `/kaggle/input`. Ajoutez le jeu de données [PTB-XL](https://physionet.org/content/ptb-xl/) à votre environnement avant de l'exécuter. Les données, modèles entraînés et sorties d'exécution ne sont pas inclus dans ce dépôt.

Le notebook provient du travail de projet. Les sorties ont été retirées pour alléger le dépôt et une cellule de visualisation a été replacée après la préparation des données ; les résultats ne sont pas recalculés ici.

Ce projet est une démonstration de recherche et ne constitue pas un outil de diagnostic médical.
