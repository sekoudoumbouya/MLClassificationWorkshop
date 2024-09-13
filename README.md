## MLClassificationWorkshop

## Description
Ce projet a été réalisé dans le cadre d'un atelier de formation effectué le 5 février 2022 à la Faculté des Sciences et Techniques (FST) de Tanger. L'atelier portait sur l'initiation au machine learning, plus spécifiquement sur la classification, et s'adressait à des étudiants chercheurs dans le domaine de la maintenance prédictive de l'entreprise **SMART AUTOMATION TECHNOLOGIES**.

L'objectif était d'initier les participants aux techniques de classification en utilisant un exemple concret de prédiction de souscription à un produit bancaire.

## Prérequis
- Python 3.x
- Bibliothèques Python nécessaires :
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `joblib`
  - `matplotlib` et `seaborn`

Installez ces dépendances via pip :

```bash
pip install pandas numpy scikit-learn joblib matplotlib
```

## Installation
1. Clonez ce dépôt GitHub :
   ```bash
   git clone https://github.com/sekoudoumbouya/MLClassificationWorkshop.git
   cd MLClassificationWorkshop
   ```
2. Installez les dépendances listées dans les prérequis.

## Utilisation
1. **Prétraitement des données** :  
   Le notebook contient des fonctions pour le prétraitement, y compris l'encodage et l'imputation des valeurs manquantes.
   ```python
   dataset_impute = imputation(dataset)
   ```

2. **Entraînement du modèle** :  
   Utilisez des algorithmes de machine learning comme RandomForest pour entraîner un modèle prédictif.
   ```python
   model_test_RF = RandomForestClassifier(n_estimators=200)
   model_test_RF.fit(X_train_df, y_train_df)
   ```

3. **Sauvegarde et chargement du modèle** :  
   Vous pouvez sauvegarder le modèle avec `joblib` et le charger pour une utilisation future.
   ```python
   # Sauvegarde
   joblib.dump(model_test_RF, 'model_test_RF')

   # Chargement
   model_charge = joblib.load('model_test_RF')
   ```

4. **Prédiction** :  
   Une fonction de prédiction est incluse pour estimer la souscription d'un client à un produit bancaire.
   ```python
   souscription(model_test_RF, age=30, balance=1000, duration=200, campaign=2)
   ```

## Licence
Ce projet est sous licence MIT.
