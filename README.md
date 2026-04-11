# Breast Cancer Diagnostic Analysis

Una analisi completa con modelli di machine learning per la diagnostica del cancro al seno utilizzando il dataset Breast Cancer Wisconsin (Diagnostic).

## 📋 Descrizione Progetto

Questo progetto implementa un pipeline completo di machine learning per classificare tumori come maligni o benigni. Il dataset contiene 30 features derivate da immagini digitali di biopsie al seno e include informazioni su pazienti con cancro diagnosticato.

**Obiettivo**: Costruire un modello di classificazione in grado di predire con alta accuratezza se un tumore è maligno (M) o benigno (B).

## 📊 Dataset

- **Fonte**: UCI Machine Learning Repository - Breast Cancer Wisconsin (Diagnostic)
- **Numero di campioni**: 569
- **Numero di features**: 30 (calcolate da 10 caratteristiche di base)
- **Target**: Diagnosi (Malignant/Benign)

### Features principali

Le 30 features sono derivate da 10 misurazioni di base:
- radius (raggio)
- texture (tessitura)
- perimeter (perimetro)
- area (area)
- smoothness (levigatezza)
- compactness (compattezza)
- concavity (concavità)
- concave points (punti concavi)
- symmetry (simmetria)
- fractal dimension (dimensione frattale)

Per ogni caratteristica sono calcolate: mean, standard error, e worst (peggiore).

## 🚀 Quick Start

### Requisiti

- Python 3.8+
- pip

### Installazione

```bash
# Clona il repository
git clone https://github.com/[tuo-username]/breast-cancer-diagnostic-analysis.git
cd breast-cancer-diagnostic-analysis

# Crea un ambiente virtuale (consigliato)
python -m venv venv
source venv/bin/activate  # Su Windows: venv\Scripts\activate

# Installa le dipendenze
pip install -r requirements.txt
```

### Utilizzo

```bash
# Avvia il notebook Jupyter
jupyter notebook Notebook2.ipynb
```

## 📦 Dipendenze

```
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
ucimlrepo>=0.0.1
```

Vedi `requirements.txt` per la lista completa.

## 📈 Struttura del Progetto

```
breast-cancer-diagnostic-analysis/
├── Notebook2.ipynb          # Notebook principale con analisi completa
├── README.md                # Questo file
├── requirements.txt         # Dipendenze del progetto
└── .gitignore              # File da ignorare in Git
```

## 🔍 Analisi nel Notebook

Il progetto include:

1. **Installazione dipendenze**: Setup iniziale con `ucimlrepo`

2. **Caricamento dati**: Importazione del dataset tramite UCI ML Repository
   - Definizione manuale delle 30 feature names
   - Rimozione della colonna ID (non predittiva)

3. **Exploratory Data Analysis (EDA)**:
   - Analisi descrittive e statistiche
   - Visualizzazione della distribuzione dei dati
   - Analisi correlazioni
   - Identificazione di outliers

4. **Preprocessing**:
   - Standardizzazione/Normalizzazione dei dati
   - Gestione di valori mancanti
   - Feature selection/engineering

5. **Modellazione**:
   - Splitting train/test
   - Training di diversi modelli (es: Logistic Regression, Random Forest, SVM, ecc.)
   - Tuning degli iperparametri

6. **Valutazione**:
   - Metriche: Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix
   - ROC-AUC Curve

## 📊 Risultati Attesi

Il modello dovrebbe raggiungere elevate performance di classificazione con accuratezza superiore al 95% sul test set.

## 💡 Note Tecniche

- Il file `wdbc.data` è headless, per questo le feature vengono definite manualmente
- L'ID del paziente viene rimosso poiché non è una feature predittiva
- I dati vengono standardizzati prima del modellamento

## 🤝 Contributi

I contributi sono benvenuti! Se trovi bug o hai suggerimenti:

1. Fork il repository
2. Crea un branch per la tua feature (`git checkout -b feature/AmazingFeature`)
3. Commit i tuoi cambiamenti (`git commit -m 'Add some AmazingFeature'`)
4. Push al branch (`git push origin feature/AmazingFeature`)
5. Apri una Pull Request

## 📄 Licenza

Questo progetto è rilasciato sotto licenza MIT. Vedi il file `LICENSE` per i dettagli.



**Nota**: Questo progetto è a scopo didattico e non deve essere utilizzato per diagnosi mediche reali.

