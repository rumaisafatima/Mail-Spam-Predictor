<div style="background: linear-gradient(135deg, #0f172a 0%, #1a1f3a 50%, #0f172a 100%); border: 1px solid #1e293b; padding: 60px 40px; border-radius: 8px; text-align: center;">
  <h1 style="color: #60a5fa; margin-bottom: 10px;">📬 Mail Spam Predictor</h1>
  <p style="color: #cbd5e1; max-width: 600px; margin: 0 auto; line-height: 1.8;">></p>
</div>

## I. Introduction

Every message carries a shape.

> Some are conversational fragments.  
> Some are transactions.  
> Some attempt persuasion.  
> Some are quiet traps wrapped in promises.

This project studies that shape.

The notebook <code>Mail_Spam_Predictor.ipynb</code> captures thousands of raw messages, strips them down to their linguistic spine, converts them to weighted vectors, and trains a model to draw a boundary between the authentic and the unwanted.

It is machine learning reduced to its most essential motion:
<br>
<kbd>observe → transform → learn → decide.</kbd>

---

## II. The Concept

Text is not random.<br>
Spam has a signature — urgency, reward cues, compressed intent.<br>
Ham has rhythm, natural phrasing, and context.

- **TF-IDF** reveals these signatures.<br>
- **Logistic Regression** interprets them.<br>
- **Accuracy** validates the interpretation.

What begins as unstructured language becomes a geometric space where classification is simply geometry.

---

## III. Repository Structure

```
Mail-Spam-Predictor/
│
├── Mail_Spam_Predictor.ipynb     # The full workflow
├── mail_data.csv                 # Dataset (if included)
│
└── model/
    ├── model.pkl                 # Learned decision boundary
    └── vect.pkl                  # TF-IDF transformation rules
```

This is a minimal, committed architecture.<br>
Everything in the project exists for a reason.

---

## IV. Workflow Overview

### 1. Acquisition

Messages are loaded into a clean DataFrame and stripped of nulls to create uniformity.

### 2. Normalization

Labels are brought into numeric clarity:
- <code>ham  → 0</code>
- <code>spam → 1</code>

### 3. Division

The dataset is partitioned:<br>
one part for learning, one for proving.

### 4. Transformation

TF-IDF translates words into weighted signals — a vocabulary turned into vectors.

### 5. Learning

Logistic Regression absorbs the signals and builds a boundary, a quiet algorithm with quiet strength.

### 6. Evaluation

The results form a near-perfect mirror:
- Training accuracy : <b>~96.7%</b>
- Testing accuracy  : <b>~96.8%</b>

A model that doesn’t memorize, but genuinely understands pattern.

### 7. Preservation

Both the classifier and the vectorizer are exported.<br>
Knowledge becomes a reusable artifact.

---

## V. Using the Model

```python
import joblib

model = joblib.load("model/model.pkl")
vect  = joblib.load("model/vect.pkl")

text = ["Congratulations! You won a reward."]
features = vect.transform(text)

model.predict(features)   # → 1   (spam)
```

Minimal input.  
Clear decision.

---

## VI. Why This Project Works

This notebook is intentionally restrained.
- No excessive preprocessing.
- No deep neural networks.
- No ceremony.

It demonstrates the fundamental craft of NLP:

- **define the problem**
- **respect the data**
- **transform appropriately**
- **model with clarity**
- **validate with discipline**

What remains is a clean, conceptual, well-executed blueprint of text classification.

---

## VII. Aesthetic Identity

This repository is designed with a particular tone:

- Restrained typography
- Soft geometric alignment
- Quiet color palette (in banner & visual identity)
- Minimal structural clutter
- Emphasis on conceptual flow rather than ornament

It presents machine learning not as machinery, but as a form of analytical composition.

---

## VIII. Closing Perspective

Spam detection is a practical task, but beneath it lies a deeper idea:

> **Language has patterns.**  
> **Meaning has boundaries.**  
> **Data has shape.**  
> **Models merely reveal what has always been there.**

This repository is a study of that shape — curated, distilled and presented with precision.

<hr />

<p align="center">
  <img src="https://img.shields.io/badge/LANGUAGE-Python-blue.svg?style=flat-square&logo=python&logoColor=white">
  &nbsp;
  <img src="https://img.shields.io/badge/ML-Logistic%20Regression-green.svg?style=flat-square">
  &nbsp;
  <img src="https://img.shields.io/badge/VECTOR-TF--IDF-9cf.svg?style=flat-square">
</p>

<p align="center" style="margin-top:16px;">
  <img src="https://raw.githubusercontent.com/rumaisafatima/Mail-Spam-Predictor/assets/footer_art.svg" alt="Footer Art" width="280px">
</p>

<p align="center">
  <sup>
    <b>Mail Spam Predictor</b> | made with <img height="14" src="https://img.icons8.com/color/48/like--v1.png" style="transform:translateY(2px);" /> by <a href="https://github.com/rumaisafatima">rumaisafatima</a>
  </sup>
</p>
<svg width="240" height="32" viewBox="0 0 240 32" fill="none" xmlns="http://www.w3.org/2000/svg">
  <rect width="240" height="32" rx="16" fill="url(#ftr-grad)" />
  <g opacity="0.23">
    <ellipse cx="54" cy="24" rx="25" ry="6" fill="#2e83af"/>
    <ellipse cx="186" cy="8" rx="29" ry="10" fill="#7eb6df"/>
  </g>
  <text x="120" y="23" text-anchor="middle" font-family="'Fira Mono', monospace" font-size="13" fill="#2e83af" opacity="0.85">
    — observe  ·  transform  ·  decide —
  </text>
  <defs>
    <linearGradient id="ftr-grad" x1="0" y1="0" x2="240" y2="32" gradientUnits="userSpaceOnUse">
      <stop stop-color="#e3effa"/>
      <stop offset="1" stop-color="#b8d5ef"/>
    </linearGradient>
  </defs>
</svg>
