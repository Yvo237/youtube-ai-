# 🎯 ANALYSEUR D'UTILITÉ DES VIDÉOS YOUTUBE AVEC IA

Un outil intelligent basé sur **l’API YouTube** et **Gemini AI** (modèle Google Generative AI) permettant d’évaluer automatiquement **l’utilité d’une vidéo YouTube** selon un **thème donné**.

L’objectif est de déterminer si une vidéo est **pertinente, crédible et utile** pour un sujet particulier (ex. *intelligence artificielle*), en combinant les **métadonnées YouTube**, les **commentaires des utilisateurs** et une **analyse sémantique IA**.

---

## 🧠 Fonctionnalités principales

- 🔍 Extraction automatique de l’ID à partir d’une URL YouTube.
- 📊 Récupération des informations clés : titre, description, vues, likes, commentaires.
- 💬 Analyse des commentaires populaires pour détecter la perception générale.
- 🤖 Évaluation automatisée de l’utilité via **Gemini 2.5 Flash**.
- 🧾 Génération d’un **rapport clair** incluant :
  - **Verdict** : Très utile / Utile / Moyennement utile / Pas utile
  - **Score sur 10**
  - **Points positifs et négatifs**
  - **Recommandations personnalisées**

---

## ⚙️ Technologies utilisées

| Domaine | Technologie / Librairie |
|----------|--------------------------|
| API IA | `google.generativeai` (Gemini) |
| API YouTube | `googleapiclient.discovery` |
| Authentification | `google.colab.userdata` |
| Langage | Python 3 |
| Environnement conseillé | Google Colab |

---

## 📦 Installation et configuration

### 1️⃣ Cloner ou importer le projet
```bash
git clone https://github.com/<votre-utilisateur>/<votre-repo>.git
cd analyseur-youtube-ia
```

### 2️⃣ Installer les dépendances
```bash
pip install google-generativeai google-api-python-client
```

### 3️⃣ Ajouter vos clés API dans Colab
```python
from google.colab import userdata
userdata.set('GOOGLE_API_KEY', 'votre_cle_gemini')
userdata.set('YOUTUBE_API_KEY', 'votre_cle_youtube')
```

---

## 🚀 Utilisation

### Mode terminal (Colab ou Python classique)
```python
python analyseur_youtube.py
```

### Exemple
```
🎯 ANALYSEUR D'UTILITÉ VIDÉOS YOUTUBE
========================================
🔗 Entrez l'URL de la vidéo YouTube: https://www.youtube.com/watch?v=dQw4w9WgXcQ
🎯 Thème d'intérêt (défaut: intelligence artificielle): éducation

🤖 Analyse avec IA en cours...

**VERDICT:** UTILE  
**SCORE:** 8/10  
**RAISONS:**  
- Contenu clair et pédagogique  
- Commentaires globalement positifs  
- Pas de source citée  

**RECOMMANDATION:**  
Convient pour une première approche du sujet.
```

---

## 🧩 Structure du projet

```
analyseur_youtube/
│
├── analyseur_youtube.py     # Script principal
├── README.md                # Documentation
└── requirements.txt         # (optionnel)
```

---

## 💡 Améliorations possibles

- 🔁 Analyse de playlists entières.
- 📈 Dashboard Streamlit pour visualiser les scores.
- 🧠 Intégration d’un apprentissage progressif pour affiner les critères d’évaluation.
- 🌍 Traduction automatique des commentaires avant analyse.

---

## 👨‍💻 Auteur

Développé par **Yvo Vami Neguem**  
📚 Étudiant en Informatique – Université de Ngoa  
🎯 Passionné par l’intelligence artificielle et l’automatisation des processus cognitifs.

---

## 🪪 Licence

Projet open-source sous licence **MIT** — libre d’utilisation et de modification.
