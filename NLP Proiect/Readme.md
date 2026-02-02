#  Fake News Detection using Natural Language Processing

##  Descriere proiect
Acest proiect implementează o aplicație de **detectare automată a știrilor false** folosind tehnici de Procesare a Limbajului Natural (NLP).

Scopul este clasificarea articolelor de presă în două clase:
- **FAKE** – știri false
- **REAL** – știri reale

Proiectul include două abordări diferite:
- un model clasic de Machine Learning;
- un model neural (Deep Learning).

---

##  Dataset
A fost utilizat datasetul public **Fake and Real News Dataset**, disponibil pe Kaggle, care conține articole de presă etichetate ca fiind reale sau false.

Datasetul include:
- titlul articolului;
- conținutul complet;
- eticheta asociată (FAKE / REAL).

 Sursa datasetului:  
https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset

> Notă: Fișierele CSV nu sunt incluse în repository. Datasetul poate fi descărcat direct de pe Kaggle.

---

##  Preprocesarea textului
Textele au fost preprocesate printr-un pipeline NLP clar și incremental, care include:
- curățarea textului;
- lowercasing;
- tokenizare;
- eliminarea punctuației;
- eliminarea stopwords;
- lematizare;
- combinarea titlului cu textul articolului.

Rezultatul este un text final normalizat, utilizat ca intrare pentru modele.

---

##  Modele implementate

###  Modelul 1 – Abordare clasică
- Reprezentare: **TF-IDF**
- Clasificator: **Logistic Regression**
- Au fost testate:
  - un baseline TF-IDF (parametri default);
  - două configurații TF-IDF personalizate.
- Configurația finală a fost selectată pe baza performanței pe setul de validare.

###  Modelul 2 – Abordare neurală
- Model neural bazat pe rețele neuronale recurente (GRU).
- Reprezentarea textului se face prin embeddings învățate.
- Modelul surprinde ordinea cuvintelor și dependențe pe termen lung.

---

##  Evaluare
Evaluarea modelelor a fost realizată folosind:
- **Macro-F1** (metrică principală);
- Precision / Recall;
- **Confusion Matrix**.

Datele au fost împărțite în:
- Training set;
- Validation set;
- Test set.

---

