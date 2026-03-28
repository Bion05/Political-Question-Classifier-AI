# Ταξινόμηση Σαφήνειας Πολιτικών Απαντήσεων

Υλοποίηση και σύγκριση NLP classifiers για την ανίχνευση αποφυγής 
απαντήσεων σε πολιτικές συνεντεύξεις, στο πλαίσιο του διεθνούς 
διαγωνισμού SemEval 2026 Task 6 (CLARITY).
Κάθε απάντηση πολιτικού κατηγοριοποιείται σε τρεις κλάσεις:
Clear Reply, Ambivalent και Clear Non-Reply.

## Μοντέλα
- TF-IDF + Logistic Regression (L1 regularization, bigram features)
- Word2Vec + Logistic Regression (Skip-gram, averaged word vectors)

## Πειράματα
11 πειραματικές εκτελέσεις με συστηματική βελτιστοποίηση:
- Class weighting, ngram ranges, vocabulary restrictions
- GridSearchCV με 5-fold cross-validation για C και solver
- Σύγκριση CBOW vs Skip-gram και πολλαπλών vector sizes
- Ανίχνευση overfitting μέσω learning curves

## Αποτελέσματα
| Μοντέλο | F1 (macro) |
|---------|-----------|
| TF-IDF (Run 11) | 0.510 |
| Word2Vec (Run 9) | 0.506 |

## Τεχνολογίες
Python · scikit-learn · gensim · Kaggle · LaTeX

## Αρχεία
- `PQAi.ipynb` — Notebook με όλες τις πειραματικές εκτελέσεις
- `report.pdf` — Αναφορά με ανάλυση αποτελεσμάτων και συμπεράσματα
