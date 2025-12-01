# Détection d'Anomalies Industrielles Zero-Shot

![Python](https://img.shields.io/badge/Python-3.10-blue) ![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange) ![CLIP](https://img.shields.io/badge/Model-CLIP-green)

Démonstration technique d'un système de contrôle qualité basé sur l'IA Générative (Vision-Langage).
Ce projet utilise **CLIP (Contrastive Language-Image Pre-training)** pour détecter des défauts sur des objets industriels sans nécessiter d'entraînement sur des exemples de défauts (**Zero-Shot Learning**).

##  Objectif
Identifier automatiquement si une pièce (ici une bouteille) est conforme ou défectueuse en la comparant sémantiquement à des descriptions textuelles.

##  Concepts Clés
* **Zero-Shot Detection :** Capacité à généraliser sur des défauts jamais vus.
* **Prompt Ensembling :** Utilisation de multiples descriptions ("broken", "scratched", "damaged") pour améliorer la robustesse de la détection[cite: 41].
* **Embeddings Multimodaux :** Alignement des espaces vectoriels Image et Texte.

##  Comment lancer la démo
1.  Cloner le repo :
    ```bash
    git clone https://github.com/yanniskouyate/ZeroShot-Anomaly-Demo.git
cd ZeroShot-Anomaly-Demo
    ```
2.  Installer les dépendances :
    ```bash
    pip install -r requirements.txt
    ```
3.  Lancer le Notebook :
    ```bash
    jupyter notebook demo_notebook.ipynb
    ```

##  Résultats
Le modèle calcule une probabilité d'appartenance aux classes "Normale" vs "Anormale".
Sur l'image de test fournie (`assets/bottle_test.png`), le modèle détecte l'anomalie avec une confiance élevée grâce à la compréhension sémantique des fissures/rayures.

---
*Ce projet est une version simplifiée à but pédagogique. Pour l'implémentation complète utilisée en recherche (MVTec AD Benchmark), voir le projet FADE.*
