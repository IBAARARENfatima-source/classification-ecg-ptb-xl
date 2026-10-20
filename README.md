# Analyse de signaux ECG par deep learning

Projet de fin d'année réalisé en binôme à l'ENSIAS (2025-2026). Nous avons étudié la classification de signaux ECG à 12 dérivations de [PTB-XL](https://physionet.org/content/ptb-xl/) en cinq catégories diagnostiques. Ce dépôt réunit le notebook expérimental et le [rapport complet](Rapport_PFA_ECG_DL.pdf).

## Sommaire

- [Données et démarche](#données-et-démarche)
- [Résultats du rapport](#résultats-du-rapport)
- [Contenu du dépôt et exécution](#contenu-du-dépôt-et-exécution)
- [Limites](#limites)
- [Équipe](#équipe)

## Données et démarche

| Étape | Travail réalisé |
| --- | --- |
| Données | ECG à 12 dérivations de PTB-XL ; classification en CD, HYP, MI, NORM et STTC. |
| Prétraitement | Filtre passe-bande Butterworth de 0,5 à 40 Hz et normalisation par dérivation. |
| Découpage | Plis `strat_fold` : 8 pour la validation, 9-10 pour le test ; pondération des classes à l'entraînement. |
| Modèles | CNN 1D, BiLSTM, CNN-BiLSTM, ResNet1D et CNN optimisé. |
| Évaluation | Accuracy, F1-score macro, rapports de classification, courbes d'apprentissage et matrices de confusion. |

## Résultats du rapport

Le [rapport](Rapport_PFA_ECG_DL.pdf) indique **69,48 % d'accuracy** pour le CNN 1D et un **F1 macro de 57,85 %** pour le CNN optimisé. Ces chiffres proviennent des expériences documentées dans le rapport ; les sorties du notebook publié ont été retirées et ne permettent pas de les vérifier sans réexécution.

Le CNN 1D a été retenu pour l'interface Streamlit présentée dans le rapport, tandis que le CNN optimisé donne un meilleur équilibre entre les classes. Les classes minoritaires, notamment HYP, restent difficiles à reconnaître.

## Contenu du dépôt et exécution

- [`classification-ecg-ptb-xl.ipynb`](classification-ecg-ptb-xl.ipynb) : préparation des données, entraînement et comparaison des modèles.
- [`Rapport_PFA_ECG_DL.pdf`](Rapport_PFA_ECG_DL.pdf) : contexte, méthode, résultats détaillés, figures et limites.

Le notebook a été conçu pour Kaggle. Il recherche `ptbxl_database.csv`, `scp_statements.csv` et les enregistrements ECG sous `/kaggle/input`. Ajoutez PTB-XL à cet environnement avant de l'exécuter. Les données, les poids des modèles et le code de l'interface Streamlit ne sont pas inclus dans ce dépôt.

## Limites

Le déséquilibre des classes et les diagnostics potentiellement multiples limitent l'interprétation d'une classification en une seule catégorie. Ce travail est expérimental : il ne constitue ni un dispositif médical ni un outil de diagnostic clinique.

## Équipe

- [Fatima IBAARAREN](https://github.com/IBAARARENfatima-source)
- [Aya Nasser (@ayanasser53)](https://github.com/ayanasser53)
